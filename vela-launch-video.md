# Vela: launch video, five variations

*Draft 1, 13 November 2026. Builds on `vela-product-vision.md` §10.*

Five ways to make the film, each with structure, script, scenes and where every shot comes from. They share one cast and one bank of shots, so we can shoot once and decide in the edit.

Source tags used in the tables:

| Tag | Meaning |
|---|---|
| `OWN` | Shot by us. POV on a phone at eye level, or on the glasses' own camera |
| `REAL` | The real prototype running: glasses + Vela app, unedited |
| `SCREEN` | Screen recording of the Vela family app |
| `STOCK` | Stock footage |
| `RENDER` | 3D or generated shots (glasses hero, firefly in a space) |
| `GFX` | 2D motion graphics: lens overlay, figures, wordmark |

---

## 1. Rules for all five

### Limits

- Junction: video pitch **strictly 2:00 or less**, public on YouTube or Vimeo, linked in the final submission before **Sun 15.11 10:00**. Aim for 1:30 to 1:50; never export anything over 1:55.
- English, subtitles burned in.
- Judges score Innovation, Impact and Implementation. The Meta track also asks for: a clear problem and audience, a real benefit from the first-person view, a working prototype that copes with errors and lost connection, inclusive design, consent and safe data, and a plausible path to a pilot. The comparison in section 8 shows which variation covers what.

### Honesty

The vision doc's warning about Humane and Rabbit applies to every frame.

- Real prototype shots carry a small corner tag: `Real prototype · unedited`.
- Anything not built carries `Concept`. Steps (gait, hazard outline) and "always on" are always concept.
- If our glasses have no display, every lens overlay is recreated in post. Say so once: "Display shown as concept. Vela also works by voice alone."
- Staged scenes are fine; it's a film. End card: "Dramatised. Real prototype footage is marked."
- Wording: Vela "points out", "confirms", "reminds". Never "prevents falls", "manages medication", "elderly".
- Skip the vision doc's Opening A (the "Mum, I've had an accident" phone call) unless live call audio actually works. It sets up a scam Vela can't catch on camera.

### Cast

The same cast in every variation, so footage moves freely between cuts.

| Character | Who | How we film them |
|---|---|---|
| Elena, 78 | Lives alone in her flat; the wearer | Mostly the camera itself (POV). When we see her: stock hands, back or silhouette, or an older volunteer with a signed release |
| Ana, 52 | Her daughter, lives in another city | Stock, plus her phone showing the family app |
| Mikko | Neighbour from 4B, enrolled face | Teammate |
| Dr. Laine | Elena's GP | Teammate |
| The "water company" man | Doorstep scammer | Teammate in a hi-vis vest with a lanyard |
| Vela | The firefly and the voice | `GFX` + the same TTS voice the app uses |

- Continuity anchor for Elena: one amber cardigan sleeve and one ring, worn in our POV shots and matched when choosing stock hands.
- Pick Ana's and Elena's stock from a single creator who shot a series with the same model, so each looks like one person.
- Stock never carries our dialogue on a visible mouth. Use backs, hands, profiles, or put the line on a phone call.

### Vela's voice and look

- Voice: calm, unhurried, short sentences, never "you forgot". Generate every line with the app's own TTS voice, so the film and the product sound the same.
- Firefly: a soft amber dot at the top right of the view. It breathes when idle and glows when Vela speaks.
- Lens text: one line, large, amber, **no box** (on the lens, dark shows as transparent). Never a menu.
- Font for lens text and subtitles: Atkinson Hyperlegible, designed for low-vision readers. It's also an inclusive-design point to mention. Wordmark in a humanist serif.
- Colours (proposal): amber `#FFB54A`, near-black `#0D0B09`, cream `#F3EBDD`.
- Subtitles: full sentences, sentence case, cream; Vela's lines in amber so viewers learn her colour.

### Shooting

- **POV before the glasses work:** a phone at eye level (0.5x lens, head strap or held against the forehead), slow head movements. Save the glasses for the `REAL` shots.
- **POV aspect:** Ray-Ban Meta records portrait video by default; check our model. In the 16:9 master, show POV as a centred lens-shaped window on near-black, which also tells the viewer "this is through her glasses". Use the full frame in 9:16 cuts.
- **A home at the venue:** POV only shows what is in front of the hands, so a dressed table reads as a home: tablecloth, mug, plant, warm 2700 K lamp, a radio, a key hook.
- **Stock:** Pexels, Pixabay and Mixkit are free; Artgrid and Storyblocks are paid. Search for details rather than faces: hands, objects, windows, doorways, light. No smiling pensioners, no medical blue, no hospital corridors.
- **Renders:** use existing assets rather than building our own. A Ray-Ban Meta 3D model from Sketchfab or CGTrader (check the licence) or Meta press images for hero shots. The firefly is a glow particle in After Effects or DaVinci Fusion.
- **AI video** (Veo with `GEMINI_API_KEY`, Sora with `OPENAI_API_KEY`): only for backgrounds nobody can film, like a city at dusk or a block of flats at night. Keep it short, cap it at about 10 generations, and never use it for people or the product.

---

## 2. Shared shot bank

Shoot these once and every variation draws from them.

| ID | Shot | Source | Used in |
|---|---|---|---|
| A1 | Glasses lifted from the bedside table and put on; POV fades in. Also reversed for night (glasses off, firefly dims) | `OWN` + `GFX` | 1, 2, 5 |
| A2 | Pill organiser; hand takes the blue pill. Take 1: puts it back after Vela speaks. Take 2: swallows it (for V4) | `OWN` | 1, 2, 4, 5 |
| A3 | Scam letter opened at the kitchen table: "Your account has been suspended. Call 0800 ... within 24 hours." Invented bank, no real logos | `OWN` / `REAL` | all |
| A4 | Doorbell, door opens: Mikko with a parcel | `OWN` | 1, 2, 5 |
| A5 | Doorstep: man in hi-vis, "Water company, I need to check your pipes." Take 1: she lets him in. Take 2: she doesn't | `OWN` | 4 |
| A6 | GP visit. Dr. Laine: "Is it OK if Vela listens?" Elena: "Please." Then he explains one change | `OWN` | 1, 2, 4, 5 |
| A7 | After the visit: street, tram or metro | `STOCK` or `OWN` (Espoo metro) | 1, 4 |
| A8 | Night hallway, a step down in poor light; amber line traces the edge | `OWN` + `GFX`, `Concept` | 1, 4, 5 |
| A9 | Family app: "Today: all fine." and the list of moments; Ana's thumb scrolling | `SCREEN` (edge to edge on black) + `STOCK` hand | all |
| A10 | Ana in her city: commute, office, kitchen at night, glancing at her phone | `STOCK` | 1, 2, 5 |
| A11 | Elena b-roll: hands on a mug, window light, keys on a hook, family photos, a radio | `STOCK` + `OWN` | all |
| P | Proof block (below) | `REAL` + `SCREEN` | all |

### The proof block (15 to 20 s)

Every variation includes it, either embedded in the story or as its own section.

- One real interaction, end to end, no cut in the middle.
- Left half: what the glasses see (the app's camera stream or native capture). Right half: the phone app, screen-recorded at the same moment. A running clock in a corner so judges see the real latency. Don't speed it up.
- Suggested take: the scam letter (A3). Elena looks at it. Vela: "This isn't from your bank. Shall I call Ana?" Elena: "Yes." The phone dials Ana.
- Optional 5 s robustness take, which Meta asks for: Wi-Fi off. Vela: "I've lost the connection. I'll tell you when I'm back." Wi-Fi on. Vela: "I'm back."
- Shoot ten or more takes and keep the cleanest.

---

## 3. Variation 1: "A day with Vela"

**Logline.** One day of Elena's life, through her glasses. Vela steps in four times and stays quiet the rest. The film ends on Ana's phone: "Today: all fine."

- **Speaks to:** wearer and family equally.
- **Tone:** warm, quiet, documentary.
- **Length:** 1:45.
- **Music:** soft piano from 0:06; swells under the tagline.
- **Mix:** 20% stock, 10% render/GFX, 70% own/real.

| # | Time | Picture | Source | Sound and words |
|---|---|---|---|---|
| 1 | 0:00–0:06 | Black. An amber dot fades in and breathes. A hand lifts the glasses towards camera; POV fades in on a morning bedroom | `GFX`, A1 | Birdsong, a kettle far off. VELA: "Good morning, Elena." |
| 2 | 0:06–0:18 | Kitchen, pill organiser. Her hand takes the blue pill. Lens: *Blue: done today. White: now.* She puts the blue back and takes the white | A2 + `GFX` | VELA: "The blue one is done for today. The white one is next." ELENA, softly: "Thank you." |
| 3 | 0:18–0:40 | Envelope on the doormat; she opens it at the table. Firefly glows. Lens: *Not your bank.* A tap on the frame. Cut: a phone rings on a desk in another city; Ana answers | A3 `REAL` (tagged), A10 | VELA: "This isn't from your bank. They never ask you to call a new number. Shall I call Ana?" ELENA: "Yes, please." ANA: "Mum? I've got the photo. Bin it, it's a scam." |
| 4 | 0:40–0:52 | Doorbell. Door opens: Mikko with a parcel. Lens: *Mikko · 4B · fixed your radiator in October.* Small note at the bottom: *Faces: only people who chose to be recognised* | A4 + `GFX` (`Concept` if not built) | ELENA: "Mikko! Come in, I'll make coffee." |
| 5 | 0:52–1:08 | Dr. Laine's office, the consent line. Then the tram. Lens: *White pill → evening* | A6, A7 | DR. LAINE: "Is it OK if Vela listens?" ELENA: "Please." His voice fades under the music. On the tram, VELA: "Dr. Laine changed one thing. The white pill moves to the evening. I've sent Ana the summary." |
| 6 | 1:08–1:22 | Evening, Ana's kitchen. Her phone: *Today: all fine.* Below it: *08:12 pill confirmed · 10:40 letter flagged, you were called · 15:30 visit summary.* She calls her mum | A10 + A9 | ANA: "Hi Mum. Nothing's wrong. Tell me about your day." |
| 7 | 1:22–1:32 | Night hallway: the step is outlined (`Concept`). Bedroom: glasses back on the table; the firefly dims to a dot | A8, A1 reversed | VELA: "Step down here." Then: "Good night, Elena." |
| 8 | 1:32–1:45 | Black. *99 million Europeans are over 65.* / *4 in 10 women over 65 live alone.* Wordmark *Vela*. *Live alone. Never on your own.* Small: *Built at Junction 2026 on Ray-Ban Meta. Dramatised; real prototype footage is marked.* | `GFX` | Music resolves. |

- **Why it works:** all five watches appear as one product, never as a feature list. Strongest on real-world impact and on what the first-person view adds day to day.
- **Weak spot:** it says nothing about how Vela is built or how it reaches people. The deck has to carry that.
- **Prototype must do:** the scam letter flow.

---

## 4. Variation 2: "Two cities"

**Logline.** Split screen. Left: Ana's day in her city, phone always face up. Right: Elena's day in her flat. The film is about what Ana *doesn't* get told.

- **Speaks to:** the buyer, the adult child.
- **Tone:** tender, a little wry.
- **Length:** 1:40, or 1:55 with the proof block.
- **Music:** sparse piano; a ticking clock under the cold open.
- **Mix:** 45% stock (Ana), 45% own/real (Elena), 10% screen/GFX.
- **Format bonus:** a portrait POV clip fills half of a 16:9 frame almost exactly.

| # | Time | Picture | Source | Sound and words |
|---|---|---|---|---|
| 1 | 0:00–0:10 | Cold open, before Vela, full frame. Ana in a meeting, phone buzzes: *Mum.* She hurries out and takes the call in the corridor, back to camera | `STOCK` | ANA: "Mum? Are you OK?" ELENA, on the phone: "Yes, love. I just can't find my keys." Ana leans against the wall and exhales. |
| 2 | 0:10–0:16 | Ana alone in the corridor. The frame splits: left Ana, right Elena's kitchen | `STOCK` + `OWN` | ANA, voice-over: "Every time it rings, I think it's the call." |
| 3 | 0:16–0:28 | Right: the pill, with Vela's line. Left: Ana on the train; she glances at her phone. The screen stays dark | A2, A10 | VELA: "The blue one is done for today." Left side: train noise only. |
| 4 | 0:28–0:40 | Right: Elena in the hallway, looking around. Lens: *Shelf by the radio.* Left: Ana in a meeting, phone dark | `OWN` + `GFX` (`Concept` if not built), A10 | ELENA: "Vela, where are my keys?" VELA: "On the shelf by the radio. You put them there at 9:40." |
| 5 | 0:40–0:58 | Right: the scam letter. Left: Ana's phone lights up: *Vela: Mum has a letter that looks like a scam. Calling you.* She answers, calm this time | A3 `REAL`, A9 | VELA: "This isn't from your bank. Shall I call Ana?" ELENA: "Yes." ANA: "Bin it, Mum. Good catch." ELENA: "Vela's catch." |
| 6 | 0:58–1:10 | Right: Dr. Laine and the consent line. Left: the summary arrives: *Dr. Laine: white pill moves to the evening. Next check-up 12 Dec.* Ana adds it to her calendar | A6, A9 | DR. LAINE: "Is it OK if Vela listens?" ELENA: "Please." |
| 7 | 1:10–1:20 | Left, full height: Ana's app. One line on it: *Vela never shows you what Elena sees. Only the moments she stepped in.* Right: Elena watering plants, unobserved | A9, A11 | Quiet. Music returns. |
| 8 | 1:20–1:32 | Evening. The split closes into one frame: Ana on her sofa, calling | A10 | ANA: "Hi Mum. Nothing's wrong. I just wanted to hear your voice." ELENA: "Then let me tell you about Mikko's radiator." |
| 9 | 1:32–1:40 | Black. *Your home, not a home.* Wordmark *Vela*. End-card small print as in V1 | `GFX` | |
| opt | +15 s | Proof block before the end card | P | |

- **Why it works:** it talks to the person who pays. The restraint (Ana hears about the letter, not the pill) is the product insight, and it doubles as the privacy and consent answer.
- **Weak spot:** most of Ana is stock, so lip-sync limits the shots. A split screen is also more work in the edit.
- **Prototype must do:** the scam letter flow and the call to Ana.

---

## 5. Variation 3: "The keynote"

**Logline.** One presenter, a dark room, one light, the glasses in hand. Problem, product, live demo, vision, plan, in that order, with nothing faked.

- **Speaks to:** judges and investors.
- **Tone:** calm, confident, modest.
- **Length:** 1:55 (at the cap; trim scene 5 first).
- **Music:** a low pulse, almost nothing under speech.
- **Mix:** 50% presenter, 25% real/screen, 15% render/GFX, 10% stock.

| # | Time | Picture | Source | Sound and words (P = presenter) |
|---|---|---|---|---|
| 1 | 0:00–0:07 | Dark. The glasses on a black plinth under one key light. A hand picks them up | `OWN` | P: "What ends living alone is rarely one big fall." |
| 2 | 0:07–0:25 | P to camera. Figures appear beside him one at a time: *1 in 3* fall each year (WHO). *40–80%* of what the doctor says is forgotten (Kessels). *1 in 12* defrauded in a year (UK, Age UK). One-second cutaways: a pill box, a letter, a dark step | `OWN`, `GFX`, `STOCK` | P: "It's a run of small ones. A pill taken twice. A letter that looks like the bank. A step you didn't see. Each one brings the family closer to saying: it's not safe any more." |
| 3 | 0:25–0:40 | The glasses turn slowly in a render; the firefly lights at the corner of the lens. A three-step diagram: glasses → phone → one line in the ear | `RENDER`, `GFX` | P, voice-over: "This is Vela, a guardian that lives in the glasses you already wear. She sees what you see, hears what you hear, and speaks only when it matters. The glasses are the eyes and ears, the phone does the thinking, and Vela answers in one line." |
| 4 | 0:40–1:05 | P puts the glasses on. Proof block, tagged `Live · unedited`: the pill check, the scam letter, the Wi-Fi drop | P | P: "Everything you just saw runs on Ray-Ban Meta today, through Meta's Device Access Toolkit." |
| 5 | 1:05–1:22 | Vision, tagged `Concept`: Mikko's name on the lens (with the consent note), the doctor summary going to the family, the outlined step | A4, A6, A8 | P, voice-over: "Next: the names of people who have chosen to be recognised. A plain summary after the doctor. A light on the step at night. Today she starts when you ask. Next, she's always there." |
| 6 | 1:22–1:40 | The family app. Then an optician's wall of glasses | A9, `STOCK` | P: "Families set it up once. They get one line a day, 'all fine', and a call when it matters. Never a camera feed. We start where people already buy glasses: opticians. First pilot: one optician chain and one city's home-care service." |
| 7 | 1:40–1:55 | P takes the glasses off and looks at them. Black. Wordmark. *Live alone. Never on your own.* | `OWN`, `GFX` | P: "Ninety-nine million Europeans are over 65. Most want to stay at home. Vela helps them do it." |

- **Shoot:** black backdrop (dark room plus black cloth), one key light at 45° and a faint rim light, two phones on tripods (wide and close, 4K 25 fps), a lav mic into one phone, a teleprompter app on a laptop under the lens. About an hour.
- **Personal line:** an opening like "my grandmother..." is the strongest hook, but only if it's true for someone on the team.
- **Why it works:** it maps one-to-one onto Innovation / Impact / Implementation and onto Meta's list (problem, audience, working prototype, robustness, consent, pilot). It's also the easiest to shoot at the venue.
- **Weak spot:** the least emotional, and it looks like every other pitch. The Humane comparison is right there. Keep the presenter modest and let the real latency show.
- **Prototype must do:** pill check, scam letter, and recovery from a dropped connection.

---

## 6. Variation 4: "Rewind"

**Logline.** Four small moments that end independence. Each plays out going wrong, then the tape rewinds and it plays again with Vela.

- **Speaks to:** everyone. The clearest problem → solution of the five.
- **Tone:** tense, then relief.
- **Length:** 1:50.
- **Music:** none in the "without" takes (room tone only). A warm theme returns with each "with Vela" take.
- **Look:** "without" is desaturated, cool grey (not blue) and slightly handheld. "With" is warm, with the amber firefly. The rewind is an 8x reverse scrub with a tape-rewind sound.
- **Mix:** 70% own (each scene shot twice, same setup), 15% stock, 15% GFX.

| # | Time | Picture | Source | Sound and words |
|---|---|---|---|---|
| 1 | 0:00–0:16 | Grey: her hand takes the blue pill and swallows it; the stove clock reads 08:12. Freeze. *Almost 200,000 deaths a year in the EU are linked to medicines not taken as prescribed (est.).* Rewind. Warm: she puts it back | A2 (both takes), `GFX` | Room tone, a clock ticking. After the rewind, VELA: "The blue one is done for today." |
| 2 | 0:16–0:40 | Grey: the man in hi-vis at the door. She lets him in; the camera passes her handbag on the hall table and he glances at it. Freeze. *About 1 in 12 older people in England and Wales were defrauded in a year (Age UK).* Rewind. Warm: the firefly glows; he leaves | A5 (both takes), `GFX` | MAN: "Water company. There's a leak in the building, I need to check your pipes." After the rewind, VELA, in her ear only: "The water company writes first. He has no appointment. Shall I call Ana?" ELENA, to the man: "My daughter will ring your office first." |
| 3 | 0:40–1:02 | Grey: on the tram she studies the prescription slip; on the phone with Ana. Freeze. *40–80% of what the doctor says is forgotten straight away (Kessels, 2003).* Rewind into Dr. Laine's office, then the tram again, warm | A6, A7, `GFX` | ANA: "So what did he change?" ELENA: "Something about... the white one?" After the rewind, DR. LAINE: "Is it OK if Vela listens?" ELENA: "Please." VELA: "One change: the white pill moves to the evening. Ana has the summary." |
| 4 | 1:02–1:18 | Grey: dark hallway at night. Her foot reaches for a step that isn't where she thinks; the frame tips; cut to black (never show the fall). *1 in 3 people over 65 fall each year (WHO).* Rewind. Warm: amber line along the step edge. Tag `Concept` | A8, `GFX` | A thud in the dark. After the rewind, VELA: "Step down here." |
| 5 | 1:18–1:35 | Proof block. Opening line: *Two of these work today.* | P | Real audio. |
| 6 | 1:35–1:50 | Black. *What ends living alone is rarely one big event.* / *It's a run of small ones.* / *Vela is there for the small ones.* Wordmark. *Live alone. Never on your own.* End-card small print | `GFX` | Theme resolves. |

- **Why it works:** problem and solution sit in the same shot, and each watch arrives with its number, so impact lands without a lecture. The rewind is a known device and works in 9:16 too.
- **Weak spot:** the "without" takes must not make Elena look foolish. The scammer is convincing and the hallway is truly dark. Scenes take two takes each, though it's the same setup.
- **Prototype must do:** pill check and scam detection (letter in the proof block; doorstep audio if it works).

---

## 7. Variation 5: "Firefly"

**Logline.** A brand film. In Spanish, *velar por alguien* means to watch over someone, and a *vela* is a candle. A small amber light moves through Elena's flat and her day, and shows up only when it's needed.

- **Speaks to:** everyone, social first. The film that would play in an optician's window.
- **Tone:** poetic, slow, almost wordless.
- **Length:** 1:48 with the proof block.
- **Music:** one ambient piece, no beat.
- **Mix:** 40% render/GFX, 30% stock, 30% own/real.

| # | Time | Picture | Source | Sound and words |
|---|---|---|---|---|
| 1 | 0:00–0:10 | Black. A match strikes; a candle flame in macro. The flame lifts off the wick and becomes a firefly | `STOCK` + `RENDER` | VELA, as narrator: "In Spanish, when you watch over someone, you say *velar*." |
| 2 | 0:10–0:30 | The firefly drifts through a sleeping flat: past the pill organiser, the letters on the doormat, the hallway step, a wall of family photos. Each object gets a thin amber outline for a moment: the five watches, without the word "feature" | `STOCK` / `OWN` locked-off night plates + `RENDER` + `GFX` | Only the music and a fridge hum. |
| 3 | 0:30–0:38 | It lands on the corner of a pair of glasses on the bedside table. Dawn. A hand picks them up | `RENDER` or `OWN` macro + `GFX` | VELA: "Good morning, Elena." |
| 4 | 0:38–1:05 | Day in POV, about 7 s per moment, no explanations: pill, letter, Mikko at the door (lens: *Mikko · 4B*), the doctor | A2, A3, A4, A6 + `GFX` | VELA: "The blue one is done for today." / "This isn't from your bank." / (lens only for Mikko) / "One change: the white pill, now in the evening." |
| 5 | 1:05–1:22 | Proof block. Opening line: *This part is real.* | P | Real audio. |
| 6 | 1:22–1:38 | Night. The glasses go back on the table and the firefly dims to a resting dot. In another city a phone lights up on a dark nightstand: *Today: all fine.* | A1 reversed, A10, A9 | VELA: "Good night, Elena." |
| 7 | 1:38–1:48 | The wordmark *Vela* appears in the firefly's light. *Live alone. Never on your own.* End-card small print | `GFX` | Music ends. |

- **Hardest shot:** the flame turning into a firefly. Cheapest version: a stock flame cross-dissolving into a glow sprite that moves along a path, about two hours in After Effects or Fusion. Night plates are tripod shots of real rooms with the firefly composited in, never AI interiors.
- **Why it works:** the most memorable, and it makes the name mean something. Best for social and for the brand.
- **Weak spot:** the least information for judges. It lives or dies on compositing; a cheap firefly reads as AI slop at once.
- **Prototype must do:** whatever the proof block shows.

---

## 8. Comparison

| | 1 Day with Vela | 2 Two cities | 3 Keynote | 4 Rewind | 5 Firefly |
|---|---|---|---|---|---|
| Speaks to | wearer + family | buyer | judges | everyone | everyone, social |
| Problem clarity | Medium | Medium | High | High | Low |
| Proof it works | Medium | Medium | High | Medium | Medium |
| Emotion | High | High | Low | High | High |
| Adoption path | None | Low | High | None | None |
| Shoot effort | Medium | Medium (split) | Low | Medium (2 takes each) | High (renders) |
| Stock / render+GFX / own | 20 / 10 / 70 | 45 / 10 / 45 | 10 / 15 / 75 | 15 / 15 / 70 | 30 / 40 / 30 |
| Biggest risk | young hands, fake-looking home | stock lip-sync | looks like every pitch | "without" takes feel patronising | compositing looks cheap |

## 9. Recommendation

**Junction submission: Variation 4 (Rewind) with the close from Variation 3.**

- Order: Rewind scenes 1, 2 and 4, then the proof block, then V3 scene 6 (setup by the family, opticians, the pilot), then the end card. About 1:50.
- Rewind gives the problem, the solution and the impact figures in the same shots. The keynote close covers implementation and adoption, which judges score and Rewind lacks.
- The doctor scene (V4 scene 3) is cut for time. Mention it in the close or keep it for the social cut.

**After the hackathon:** a 30 s 9:16 cut of V1 or V5 for social.

**Why it fits our time:** the A shots are filmed once, at the venue, on a phone, before the glasses work. The proof block is filmed as soon as the prototype runs. Everything else is stock and GFX.

## 10. Production plan

Deadline: Sun 15.11 10:00.

| When | What |
|---|---|
| Fri night | Pick the variation. Print the scam letter. Build the lens-overlay and firefly templates. Generate every Vela line with the app's TTS. Download stock. |
| Sat morning | Shoot the A shots at a dressed table at the venue (about 3 h). Keynote parts if needed (about 1 h). |
| Sat afternoon | Proof block as soon as the prototype works, ten or more takes. |
| Sat evening | Rough cut, check the length (1:55 or less), lock the picture. |
| Sat night | GFX, grade, subtitles, music, mix. |
| Sun 08:00 | Export and upload to YouTube as **public**. Watch it once on a phone. |
| Sun 09:00 | Paste the link into the submission and set the project to FINAL. |

## 11. Props and kit

- Scam letter from an invented bank (e.g. "Kestrel Savings"; check it doesn't resemble a real one).
- Pill organiser with blue and white "pills" (mints).
- Hi-vis vest and a "Water Services" lanyard. A parcel for Mikko.
- Amber cardigan, a ring.
- Tablecloth, mug, plant, warm lamp, radio, key hook with keys.
- Release forms for everyone on camera, including people in the background at the venue.
- Lav mic, two tripods, a black cloth (for V3), a phone head strap for POV.
