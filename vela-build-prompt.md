# Prompt: build Vela end to end (phone first, glasses as a plug-in)

Paste everything below the line into a fresh agent session opened in `C:\Users\Alvaro\Desktop\7-hackunction`.

---

You are building **Vela**, the hackathon prototype described in `vela-product-vision.md`. Read that file first, especially section 4 ("How it works": the five watches, what triggers each one, what the wearer hears) and sections 7–8 (voice and look). Also read `AGENTS.md` (keys, budgets) and the Meta part of `docs/hardware-track.md` (judging criteria: functional prototype that handles permissions, errors, performance trade-offs, connectivity, device state changes; consent and safe data handling).

## Goal

A working Vela that Álvaro can try **on his phone today**: the phone camera and mic stand in for the glasses, Vela watches on her own, and when one of the five triggers fires she says one short line in a calm ElevenLabs voice. Switching from phone to Meta Ray-Ban Gen2 glasses must later be a **plug-in**: one new device adapter, no changes to the watch logic, prompts or UI.

Work from start to finish without waiting for him: research, build, deploy, test it yourself, then hand him a URL and a short test script, and iterate on his feedback until it works on his phone.

## Architecture (verify, then commit to it)

1. **Web app (PWA) is the product.** All logic and UI live in one web app opened in the phone browser (Android Chrome is his main phone; an iPhone 12 mini exists as a fallback). It needs HTTPS for camera/mic. Keep the frontend dependency-light.
2. **Small backend proxy** holds the API keys (never ship keys to the browser): Gemini vision/audio calls, ElevenLabs TTS, optional STT, plus a `/log` endpoint. Pick the fastest path to a stable HTTPS URL: a Cloudflare Worker with static assets (`npx wrangler`, check if he is logged in) or his VPS (see the vault `infra/` area). Say which you picked and why in one line.
3. **Device interface, the plug-in point.** Everything above it talks to one interface, e.g.
   ```ts
   interface VelaDevice {
     start(): Promise<void>; stop(): Promise<void>;
     getFrame(): Promise<Blob>;          // one still photo, not a video feed
     audio(): MediaStream | AsyncIterable<Int16Array>; // mono mic
     say(audio: Blob | string): Promise<void>; // one short line, chime first
     state: 'idle'|'connecting'|'ready'|'error'; onStateChange(cb): void;
   }
   ```
   `PhoneDevice` implements it now (rear camera via `getUserMedia`, mic, speaker). `GlassesDevice` implements it later. Apply the glasses' limits from day one: single photos at a modest cadence, mono audio, one short spoken line per intervention.
4. **Glasses plug-in path (to confirm by research).** What I found so far: Meta's **Web Apps** run only on Ray-Ban Display and are display-only; the **camera stream/photo capture is only available through the native Wearables Device Access Toolkit (DAT) 1.0** for Android/iOS, which goes through the Meta AI app. Vela targets Gen2 (no display). So the likely plug-in is a **thin Android shell app** (Kotlin + DAT SDK) that loads the same web app in a WebView and exposes glasses photos/frames to JS through a bridge (`window.VelaNative.getFrame()`), so `GlassesDevice` is a few lines of JS. Audio may route through the glasses as a normal Bluetooth headset with no SDK at all; check whether that holds for mic input inside a WebView, or whether DAT's mic stream is needed. Test the shell with Meta's **Mock Device Kit** before any hardware. If research shows a better path, take it and explain why.

## The five watches

One simple main screen: a big Start/Stop for Vela and **five large on/off toggles** (Scams, Second look, Appointments, Faces, Steps), each with a one-line description and persisted in localStorage. Disabled watches cost nothing: they are left out of the prompt and skip their processing.

Pipeline: every ~2–3 s while running, grab a frame, skip it if it barely changed from the last one sent (cheap canvas diff), send it to **one** cheap Gemini vision call that returns strict JSON for the enabled watches only. Watch logic then decides whether to speak. Silence is the default. Add per-watch cooldowns and dedupe so she never repeats herself, a priority order when two fire together (Steps > Scams > Second look > Faces > Appointments), and a hard cap on paid calls per minute and per session.

| Watch | Trigger | What she says / does |
|---|---|---|
| **Scams** | A letter or screen in view that demands money, urgency, "account blocked", a relative "in trouble", a prize. Also doorstep or room speech in the mic transcript with the same patterns. | Calm warning plus one suggestion: "This letter asks you to pay today. Banks don't do that. Shall I call Marta?" Listen for yes/no. On yes, open a call to the trusted contact from settings (`tel:`; if the browser blocks it without a tap, show one huge "Call Marta" button). |
| **Second look** | A pill bottle or blister in hand. Check it against the schedule entered in settings and today's log: already taken, not due, or due now. Also time-based: due time passed and nothing seen, so remind once. | "The blue one is done for today." / "It's time for the white one." Never a reproach. Log what she confirmed. |
| **Appointments** | A medical setting or a doctor in view, or an appointment due now in the simple calendar from settings. | Ask aloud: "Shall I listen to this visit? Only if the doctor agrees." Record only after a spoken yes. A visible red recording state and a stop button. When it ends (stop, long silence, or leaving the setting), transcribe and summarise: medication changes, next steps, next appointment. Say a short spoken recap and keep a written version in the family log. |
| **Faces** | An enrolled person comes into view and hasn't been greeted by Vela in the last N minutes. | Whisper: "This is Pedro, your neighbour from the second floor." Enrollment in settings: photo, name, relation, and a required consent checkbox. Do the matching **on device** (face embeddings in the browser, e.g. face-api.js / MediaPipe / Human). Don't send faces to an LLM for identification: it's unreliable and a privacy problem. |
| **Steps** | A step, stairs, a loose rug, an obstacle or a dark patch just ahead in the frame. | "Careful, a step ahead." Latency matters most here, so measure it. Gait trends over weeks stay as vision (one honest line in the UI). |

Voice rules for every line: one sentence, at most about 12 words, calm, warm, never alarmed, never "you forgot". Use "points out" and "confirms" language, never medical claims.

## Speech and listening

- **TTS: ElevenLabs.** `ELEVENLABS_API_KEY` is **not** in `.env` yet. Ask Álvaro for it at the very start, and meanwhile use the browser's `speechSynthesis` so nothing blocks. Research the lowest-latency model and streaming endpoint, and pick a warm, unhurried, adult voice (not childish, not robotic). Cache fixed lines (chime, prompts, confirmations) so they don't cost a call each time. Play a soft chime before each line.
- **Listening** (yes/no replies, doorstep scams, appointments): on Android Chrome, `SpeechRecognition` and `getUserMedia` may fight over the mic. Test that early. If they conflict, record chunks with MediaRecorder and transcribe server-side (Gemini audio, OpenAI Whisper/gpt-4o-transcribe, or ElevenLabs Scribe; pick the cheapest that works).
- **Models:** list the models available on the Gemini key and choose the cheapest fast vision model for triage. Use a stronger one only for the appointment summary. Look at the Gemini Live API for streaming, but default to photo-by-photo, since that matches the glasses' limits. Keep spend visible: show a running call/cost counter in the debug panel.

## Settings and family view (keep both tiny)

- **Settings** (done once "with the family"): trusted contact (name + phone), pill schedule (name, colour/description, times, optional photo), enrolled faces with consent, appointments (date, time, place). localStorage is enough for the demo. Pre-fill a demo profile (Marta as the contact, a blue pill and a white pill, Pedro as the neighbour) so it works out of the box.
- **Family view:** "Today: all fine" plus the few moments Vela stepped in (time, watch, what she said, the appointment recap). Never a camera feed.

## Robustness the judges will check

Permission denied or revoked, camera/mic busy, offline or slow network (back off and say so once, quietly), the tab hidden or the screen locking (use the Wake Lock API; explain the limit), API errors and rate limits, device state changes (glasses disconnect later: fall back to the phone or pause with a clear status). Show a single status line on the main screen: Watching / Paused / No camera / Offline.

## Testing and iteration (do this before handing over)

1. **Remote logging:** the client posts events, triage JSON, latencies and errors to `/log`. Make it readable by you (a `GET /log?since=` behind a token, or a file on the VPS), so you can debug his phone sessions without asking him what happened.
2. **Fixtures:** build a small set of test images/clips: a scam letter, a phishing SMS on a screen, a pill bottle and blister, a doctor's office, a hallway with a step, a face to enrol, and a doorstep scam audio clip (you can generate it with ElevenLabs TTS). Delegate fixture generation to Sonnet subagents.
3. **Self-test:** a debug panel (hidden behind a long-press) with "inject image/audio" that runs the real pipeline, plus headless Chrome with fake media (`--use-fake-device-for-media-stream --use-file-for-fake-video-capture=...y4m`) or the Chrome MCP. Every watch must fire on its fixture and stay silent on neutral frames (a plain room, a normal letter). Track false alarms: one wrong scam alarm or one wrong pill confirmation is worse than silence.
4. **Hand-off:** deploy, then send Álvaro the URL, a QR code, and a test script of 6–8 lines ("point at the letter on screen X, expect Y"). Then read `/log` after his run, fix the problems, redeploy, repeat until he says it works on his phone.

## Then the glasses plug-in

Once the phone version works: research DAT 1.0 for Android in detail (SDK install, Developer Mode in the Meta AI app, permissions, photo vs stream API, the Mock Device Kit, country limits), build the thin shell APK with the WebView bridge, test it against the Mock Device Kit, and write `vela/GLASSES.md`: the exact steps to switch from the phone to real Gen2 glasses. There is no JDK, Android SDK or adb on the laptop's PATH right now. Check the vault (`devices/phone/termhome.md` covers building APKs without adb) for how he has built APKs before, then pick the least painful setup.

## Research deliverables

Keep them short, in `vela/research/`: `meta-dat.md`, `meta-web-apps.md`, `gemini.md`, `elevenlabs.md`, each with facts, links, and what it means for Vela. Run the independent research tracks as parallel Sonnet subagents and keep the decisions for yourself.

## Done means

- [ ] A URL that works on his Android phone: Start, five toggles, Vela speaks with the ElevenLabs voice when a trigger fires and is silent otherwise.
- [ ] All five watches fire on their fixtures, with no false alarms on the neutral set.
- [ ] Spend capped, latency per watch measured and written down.
- [ ] Remote logs work. He has tested it and confirmed.
- [ ] `VelaDevice` interface in place. The glasses shell is built and tested against the mock, and `vela/GLASSES.md` is written.
- [ ] Code in `vela/`, `README` with run/deploy steps, committed and pushed (no keys, no AI attribution).
