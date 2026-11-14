# Vela launch video: local re-edit (from 2026-11-14)

Álvaro is re-editing the Vela launch video from scratch on this laptop. Everything from the VPS edit job
(`/root/video-jobs/20261114-190824-980e`, "Borrador 20:49" on the upload web) is copied here, using the job's folder
layout so its scripts still run.

## STYLE: do NOT use his usual video style
- Do not apply `media/video/style.md` or the default recipe in `media/video/edit.md` (pocket-vault memory). That means
  no one-word Luckiest Guy subtitles, no gold key words, no pitched voice, no FAH, no meme sounds, emojis or stickers,
  no home-made TikTok look, and no 1.3x talk speed by default.
- This is a product launch film for Junction 2026. It must be clean, cinematic and professional, in Vela's brand:
  - canvas: warm near-black `#13110F`;
  - one amber accent;
  - Fraunces for the wordmark and Vela's lines, Atkinson Hyperlegible Next for captions (`vela_cap/fonts/`);
  - Vela's voice in amber with the firefly.
- The tools in `edit.md` are fine to use: gaps/frag/env, cutting in real troughs, `check`. Only its style rules are off.
- If he gives directions, follow him. Ask him what is wrong before you guess at a new style.
- `assets/` still holds the TikTok fonts and `fah.mp3` from the old pipeline. Don't use them.

## His feedback so far (still valid)
- Voice:
  - his English has pauses and hesitations, and the result must sound fluent;
  - cut only in real troughs (<= -50 dB, >= 30 ms away from speech) and never clip a word;
  - re-ASR the result against the script.
- Music:
  - no hard cuts to digital silence and no re-entry in the middle of a sustained chord;
  - when the music stops, it stops on a beat with a reverb tail;
  - it comes back on a real attack.
- v4: no hook at the start; the film opens on the Vela logo.
- He wants:
  - more examples of Vela recognising different people (niece, uncle, daughter, neighbour, doctor), so it looks professional;
  - a closing voice-over in Vela's voice ("I'm Vela. I'll help you remember the people you love.").
- Iterate fast with short previews; render the full video only at the end.

## What is here
| Path | What |
|---|---|
| `raw/` | iPhone clips (1920x1080, rotation -90) and the glasses clip, see the clip list below |
| `mic/` | separate mic recordings (clean voice) for 0530, 0532, 0533 and 0535 |
| `wav48/<id>.wav` | **synced voice per clip, in clip time**: the mic where it covers the clip, camera audio elsewhere, gain-matched. Use it as the voice source. `<id>cam.wav` = the camera's own audio |
| `wav/` | 16 kHz copies, plus Whisper JSONs with word times: `<id>.v3.json`, `<id>.turbo.json`, and `m<id>.v3.json` for the mic files |
| `assets/song.mp3` | Hans Zimmer, "Time" (copyrighted: a YouTube Content ID claim is near certain) |
| `assets/vela_g1.mp3`, `vela_g2.mp3` | ElevenLabs line "This is Diego, your grandson." (two takes; g1 is the one in use). `vela_line_a/b` = the old "your cousin or whatever" takes, dropped |
| `vela_cap/clips/` | captures of the real Vela app UI: talk, recog, people, family, setup, watching, sting (logo), intro (v4 opening logo), end/end2 (end card), plus the v4 example cards. `contact.jpg` = contact sheet |
| `vela_cap/scripts/` | Playwright capture and brand-card renderers. The Linux Playwright browsers were not copied: run `playwright install chromium` before re-capturing |
| `dl/vela/` | the app build used for the captures. The current app is `../vela/` |
| `pre/` | slow-motion interpolated shots: `slow_open` (grandpa alone), `slow_cb` (hands on head), `slow_scene` ("With Vela." opening), plus `pov_slow2.mp4` (glasses POV reframed) and the firefly, mask and shade PNGs |
| `sfx/` | the sounds the edits used (from the VPS `/root/video-assets/sfx/`) |
| `versions/v1-v3.mp4`, `out.mp4` | previous renders. `out.mp4` = v4 (48.8 s, 9:16), the latest; `resumen.md` describes it |

ElevenLabs settings for Vela's voice:
- voice "Lily", id `pFZP5JQG7iQjIQuC4Bku`, model `eleven_multilingual_v2`;
- stability 0.55, similarity_boost 0.8, style 0.15, use_speaker_boost true;
- key: `ELEVENLABS_API_KEY` in `pocket-vault-2/.env`.

## The footage (raw clip seconds)
- **0530** (sofa, explanation):
  - 4.18-8.06 "We built Vela, the AI companion for elderly people."
  - 12.90-31.17 "People over 70 or 80 might still want to live alone, but they might have some abilities that are not as good as they used to be. For example, remembering names."
  - 33.00-41.76 "People with early signs of Alzheimer's will start to forget the names of the people that they love the most."
- **0532** (explains the glasses):
  - 1.66-12.50 "Vela lives inside your Meta glasses and it reminds you who you're seeing. Either it's your niece, your uncle, or any person that you might know."
  - ~12.5-18 "...and you won't remember" (unused)
  - 27.98-30.06 "Let me show you an example situation."
- **0533** (skit "Without Vela"):
  - 3.55-5.95 "Grandpa? What are you doing here?"
  - 6.82-8.40 "Who are you? Who is this guy?"
  - 8.40-9.75 hands on head
- **0535** (skit "With Vela", phone angle):
  - 3.30-5.56 "Grandpa? What are you doing here?"
  - 5.58-8.47 "Oh, Diego! I'm so happy to see you!" / "Me too!"
  - 8.47-10.40 the hug
  - 10.65-12.45 "Vela. Your AI companion." (the clean audio for this line is META at 18.12)
- **META** (the same "With Vela" take from the Ray-Ban Meta glasses, same audio as 0535; mic offset = 0535's - 0.237 + 7.471):
  - the take runs ~10.9-19.3
  - a second partial take starts ~44.5

## Reusable work (to go faster)
- **Cuts**:
  - `cfg.py` `P` = the v4 pieces in raw clip seconds: `(clip, start, end, speed, kind, pitch, opt)`;
  - `say()` splits a sentence span at safe troughs and shrinks each pause (`WITHIN`/`BETWEEN`);
  - `tools/islands.py` (`env`, `pauses`) is the trough analysis;
  - `t/islands.txt` + `t/island_asr.log` = every speech island of his explanations with its ASR (v4 pass): a word-level map of what he says and where.
- **Captions**:
  - `cfg.py` `CAPS` = phrase captions as (audio id, raw time of the first word, text); they survive any re-cut;
  - `subs.ass` = the v4 captions on the v4 timeline.
- **Sync**: `tools/build_sync.py` (offsets: clip time = mic time + offset).
  - 0530 1.657, 0532 -1.355, 0533 1.551, 0535 -0.237, META -0.237 + 7.471.
  - Already applied in `wav48/`.
- **Song map**: `SONG_AT` / `MUSIC` in `cfg.py` and `tools/song_map.py`. Sections of "Time":
  - 98.85 attack of the build;
  - 152.7 climax entrance;
  - 205.43 phrase change;
  - 209.37 last climax chord.
- **Render**:
  - `film.py` (reads `cfg.py`) + `edit.py check`.
  - Written for the VPS: point the sfx path `S` in `cfg.py` at `./sfx/` and check the ffmpeg paths before running here.
- `../vela-launch-video.md` is the old stock-footage plan, outdated. Its submission rules may still apply (public YouTube link, English, burned-in subtitles, max 2:00, deadline Sun 15.11 10:00). Confirm them with him.
