# Junction 2025 finals: what happened and what to learn

Junction 2025: 14-16 Nov 2025, Hype Areena, Espoo. About 1,500 hackers, 111 nationalities, 291 projects, 40+ partners, prize pool 50k+ EUR, Grand Prize 10k EUR. Theme "Utopia & Dystopia". Main partner: Sensofusion (counter-drone).

## Sources

No single "closing ceremony" or livestream video exists on the official channel (searched YouTube for finals, closing ceremony, livestream, winners). What exists is five separate videos from the official "Junction" channel, one per top-5 finalist, each cut to the pitch plus Q&A. They were uploaded 19-23 Dec 2025. The ceremony, MC, judge introductions and winner announcement are NOT in them.

| Team | URL | Title | Duration |
|---|---|---|---|
| Drone Stalker | https://www.youtube.com/watch?v=5x4mQtjzQB0 | Junction 2025 \| Top 5 Finalist Pitch - Drone stalker | 8:34 |
| Walkthrough | https://www.youtube.com/watch?v=9KT34TKEBJ0 | Junction 2025 \| Top 5 Finalist Pitch - Walkthrough | 8:46 |
| Lambda Pump ("pump") | https://www.youtube.com/watch?v=8yl6ji8T0lc | Junction 2025 \| Top 5 Finalist Pitch - pump | 8:08 |
| LoreDash | https://www.youtube.com/watch?v=43uQE6cZGXU | Junction 2025 \| Top 5 Finalist Pitch - LoreDash | 8:15 |
| Wavelet | https://www.youtube.com/watch?v=Uh3yPQuee1g | Junction 2025 \| Top 5 Finalist Pitch - Wavelet | 9:15 |

Also on the channel: Junction 2025 Aftermovie (https://www.youtube.com/watch?v=o8kTKi4xi6w, 1:44, not transcribed).

Transcripts are YouTube auto-captions (English), cleaned and deduped. Quality is decent. Caveats: the Walkthrough captions have gaps (several sentences missing, especially in the demo), and the Wavelet captions are sparse during the demo. Timestamps are in the form [m:ss].

Other links used:
- Wikipedia, Junction (hackathon): https://en.wikipedia.org/wiki/Junction_(hackathon). Says the main prize was won by WAVELET (Rudrrayan Manna, Arjun Juneja, Keanu Czirjak, Akshith Alluri).
- Wavelet repo: https://github.com/ron0studios/WAVELET. README says "we won both the sensofusion track for radio city, and the entire hackathon".
- Arjun Juneja LinkedIn post (reposted on Yacer Saffar's page, found via search). Says "Ironically our project had no AI involved" and that each member won a DJI Mini 3 via the Sensofusion Radio City track.
- Official event page: https://hackjunction.app/hackathons/junction-2025. Gives the schedule and prize info.
- Drone Stalker member's portfolio: https://codya.dev/project/2511-junction. Says they placed top 5 out of about 300 and were later invited to Google Legends Day.
- Junction 2026 site (same format described): https://2026.hackjunction.com/
- Aalto news (track winner ApprenticeCircle+): https://www.aalto.fi/en/news/aalto-students-and-researchers-shape-together-how-we-age-with-ai-at-junction-hackathon-2025

## Format of the final as actually run

Confirmed by sources:
- Selection: top 5 chosen from hundreds via the Junction platform and peer-to-peer Gavel voting. Teams are judged face to face by other participants, not by a jury, at that stage.
- Sunday 16 Nov schedule (official page): 14:00 Closing Ceremony and Top 5 Pitching, 14:40 Award Ceremony.
- A "Grand Jury" picks the overall winner after the pitches (official info deck as quoted in search results, and the 2026 site). The 2025 page only says "peer review" and live pitches.
- Challenge-track winners are picked by the sponsoring companies.

Seen in the videos:
- 5 teams, one after another, on a big stage screen with a projector. An MC introduced each ("Our next team coming to present is...").
- Pitch length was about 5 minutes, not 3. Drone Stalker says "we're only meant to have five minutes". Walkthrough was cut off with "Times up" at about 5:00. Pitch then Q&A took about 8-9 minutes per team in total. Q&A was about 3 minutes. This year's format (3 min pitch plus 3 min Q&A) is tighter, so be ready to cut hard.
- Q&A was done by 2-4 different people with a mic, apparently the jury and/or Junction staff. They are not named in the videos and I could not find the 2025 judge list. Their voices sound like partner and organiser staff, e.g. one questioner says "Ryan here" and one refers to "Hugo from Junction". This is my reading, not confirmed.
- Technical problems were common. Sound did not work for LoreDash (the speaker held the mic up to the speakers), Drone Stalker lost time to sound issues, the on-stage countdown timer did not run for LoreDash, and the Wavelet demo stalled while the GPU loaded.
- Winner announcement is not in the footage. I know the result only from Wikipedia, the team's repo and the team's LinkedIn post.

## Result

- Winner (Junction 2025 main prize, 10k EUR): Wavelet (also won the Sensofusion "Radio City" track).
- The other 4 finalists: Drone Stalker, Walkthrough, Lambda Pump, LoreDash. I found no source for 2nd to 5th placing or any runner-up ranking. Presumably only the winner was announced as such (inference).
- Other winners found: Aalto "Aging with AI" track won by ApprenticeCircle+ (team Tommin Teekkarit: Alex Kozorenko, Risto Hartikainen, Juuso Syrjala), a voice-first platform pairing seniors and young adults around shared learning. This is the only elderly-care or health project I found a result for. I did not find the other track winners, so I cannot say whether any hardware, wearable, smart-glasses or health project won beyond that.

## Finalists

### 1. Wavelet (WINNER). Track: Sensofusion "Radio City"
Team name on stage: "ARM Hampton". 4 people, 2 spoke plus a friend holding the mic.
What it is: a physically accurate real-time radio-wave simulator (FDTD / Maxwell equations) on a 3D model of Hong Kong. Pure C++, OpenGL, OpenMP, NVIDIA GPU, millions of vertices. Editor lets you drop transmitter nodes with frequencies. Waves diffract and interfere.

Pitch structure:
- No story hook. Opens with thanks to the sponsor's speaker and "we haven't slept in two days, most fun we've had in hackathons" [0:06].
- Why the challenge: hard simulation problems, educational value, cool tech [0:38].
- A short physics explanation, then a live demo of the real thing on a laptop GPU. The demo was the pitch: about 2:10 to 4:20. The GPU was slow to start ("give it a second"), then it worked. The crowd applauded when the simulation appeared [2:51].
- Differentiator stated plainly: "there is no lightweight tool that can do this... commercial options from massive companies or MATLAB" [4:21].
- Ended with "thanks for voting for us I guess" (note: peer voting framing).

Key lines:
- "We did not do this because we were masochists but more so because there was no other pre-existing solution" [0:38]
- "It's entirely GPU dependent but it can run on a tiny laptop GPU... quite scalable" [3:21]
- "Diffracts around the edges and does interference with each other as you'd expect... we thought it looked cool, so we made it" [3:51]

Q&A (about 4 min, 3 questioners):
- Who did what and how did you make decisions? Answered by each person: algorithm research and parallelisation, rendering many vertices, Mapbox satellite texturing (which failed due to earth curvature, and they said so openly), video editing.
- Real-world applications? Wi-Fi router placement in dense cities, noise and speaker placement, education (shareable pre-built scenes for school physics).
- What would you do with 48 more hours? Automatic placement planner that finds the best transmitter locations for a target coverage region, plus real materials (concrete, glass) instead of grey buildings.

What went wrong: slow GPU start, texturing did not work (admitted), the projector made visuals look worse than on the laptop ("we do have better visualizations than this").

Inference on why it won: it was a working, visually striking, technically hard demo that looked magical on stage and needed no explanation, and there was no AI (the team notes this ironically). Honest about limitations.

### 2. Drone Stalker. Track: Sensofusion "sensor fusion" (event-camera drone detection)
Team "West Europe": Jordan Legg and Jacob Kenney (UK), Mikus Sturmanis (Ireland), Cody Adam (France). 4 speakers in turn.
What it is: YOLO (v5 to 11 to 12, chose 12) drone detection on an event-camera dataset (FRED), plus a tiny LSTM (about 300k params) predicting the drone trajectory. Their LSTM beat the FRED paper's CNN and transformer models by about 50% on pixel error across 12 predicted frames. Wrapped in a gamified web app on Vercel with a Gemini "Commander" chatbot that talks (ElevenLabs voice) and unlocks features only when you follow its orders.

Pitch structure:
- Opened with a scripted audio skit: the Commander voice roasting the user ("don't pixelate yourself, noob"), with laughter [0:00]. Strong hook, but it also ate time.
- Handed off between 4 people, each owning one part: demo and Gemini, UI and graphics, YOLO and dataset, trajectory model.
- Open-source contribution: they re-uploaded the 200 GB FRED dataset to Hugging Face (takara-ai/fredconverted) because Google Drive limited downloads [2:34].
- Live link on Vercel for the audience to try it, which they said "does talk, as long as our ElevenLabs credits last" [5:06].
- Over time (about 5:00 of pitch).

Key lines:
- "Everything you see in here actually works, real time" [0:31]
- "We've made a model which beats all of the ones in the FRED dataset over a weekend. Considerably smaller, just a single LSTM" [4:06]

Q&A:
- On-device inference for war scenarios? YOLO 12 needs GPU attention, the LSTM is tiny so it is far more deployable.
- Which framework and why? PyTorch, honestly "we're here for hackathons, for fun and to learn new things".
- How are you using Gemini? The chatbot drives the whole web app.
- GPUs used? Zero, CPU only.

What went wrong: sound issues, migraine, over time.
Result: top 5 only. A team member later claimed "winner" on their portfolio, but that appears to mean finalist.

### 3. Walkthrough. Track: not stated in the video (uses Snap Spectacles; I could not confirm the challenge)
Two speakers (storyteller and a coder), three backend people in the audience.
What it is: an AR grocery assistant on Snapchat Spectacles. You say "I would like a bolognese", glasses show a shopping list, you pick items by pointing and scanning, they are added to the cart and you pay on leaving. Backend is Go on Google Cloud, AI image classification. They built a mock grocery store in a room upstairs for the live demo.

Pitch structure:
- Problem first with numbers: people spend 1.5-2 hours a week wandering aisles, a trip takes about 30 min, and the three time sinks are finding, choosing, paying [0:33].
- Market insight: under 10% of Europeans order groceries online, in-store dominates [1:03].
- Vision slide: "a 20 to 40 minute store trip could take 4 to 9 minutes with optimized routing and visual guidance", "building for a future where this might be the next mobile" [2:11], "the ChatGPT moment for AR is coming soon" [4:25].
- Demo was a recorded video of a concept (they admitted "we were a bit lying, that was not exactly our product") plus a description of the real working demo in the mock store [3:24].
- Ran out of time ("Times up") before finishing the thesis, then rushed it.

Q&A:
- What was built this weekend? Everything from scratch, including measuring the mock store by hand because there was no mapping system.
- Grocery owners will not like shorter store time. What else could the glasses show (ads, contextual content)? Answer: partner with stores, promoted products recommended in the experience.
- Who did what? Storyteller and video, one coder, "three backend guys sitting in the audience, they did most of the work". The judge's reply, "on stage", was a gentle jab that the builders were not on stage.

What went wrong: admitted that the shown AR video was not the real product (hurts trust), hard-to-hear Q&A, over time, builders not on stage.

Relevance for us: this is the only smart-glasses entry. It reached the top 5 but did not win. A judge immediately attacked the business model (store owners lose from faster shopping) and a hardware-in-a-fake-environment demo had to be explained by video.

### 4. Lambda Pump. Track: appears to be the Valmet industrial-automation challenge (speaker says "Valmouth", and HSY Blominmaki wastewater plant in Espoo as first customer; challenge name is my inference)
Team of 5 (4 present; one was in an English exam). Maths and systems science students plus data science and software. One main speaker.
What it is: wastewater pumping optimisation. MILP (mixed-integer linear programming) decides how many pumps run and when, based on electricity price (Europe moved to 15-minute pricing the month before) and weather and rainfall, and an LLM explains why the decision is best. Next.js UI, simulator for prices and rain. They also wrote a paper.

Pitch structure:
- Hook: "Right now, beneath our feet, an entire system is handling everything we flush away" [0:04]. Then a character, "Jamie", the plant manager, used as a running story: "Jamie is not very happy" [1:37].
- Concrete numbers: one pumping station uses the energy of 500+ households, unoptimised ops can lose over 100,000 [1:37].
- Quick UI walk-through (recorded or screen), then the scaling story: Valmet partnership, HSY facility, Finland then Europe and the world [4:13].
- Calm, polished, finished in about 5 min.

Q&A:
- Team split of roles (asked twice in different wording; the answer was shaky).
- What stack and what did you build the front end in? "Just Next.js", and judges pushed twice for more technical depth. Answer: MILP first for the hard optimisation, AI second to explain.
- Why pumps? "Real problem, mathematical, we like the hardest problems; we did a hard technical problem last year at Junction too."

What went wrong: the judges seemed unsatisfied with vague answers on the tech stack and on who did what.

### 5. LoreDash. Track: Supercell challenge
Solo hacker (Frank, turning 32). Slept at 4 am, up at 6, finished slides that morning.
What it is: "Curiosity Sparks Games". Takes a random Wikipedia article, Gemini 2.5 Flash makes a JSON game plan (rules, assets, sound effects), assets generated in parallel (OpenAI for transparent sprites, Gemini otherwise), Gemini 2.5 Pro writes the JavaScript canvas game loop, ElevenLabs makes retro music, and Gemini Live API gives a live voice experience. Output looks like Game Boy-style mini games. Public URL plus a "dash cache" of premade games.

Pitch structure:
- Hook: the Wikipedia "random article" button and how you end up from a Ford Fiesta to quantum chromodynamics [0:34].
- Problem: does any of it stick? Then gamified-learning examples (Kahoot, Duolingo, Minecraft Edu, GeoGuessr) and "could we turn random articles into games".
- Demo started slowly and was cut by the timer, then shown only at the end of the Q&A [7:36]. The live generation worked.

Key lines:
- "This could easily take on the likes of GeoGuessr and Duolingo" [4:26]
- "I was going to show it but I guess I'm out of time" [5:34]

Q&A:
- Which models and why? Flash for planning, Pro for code after Flash gave runtime crashes, OpenAI for transparency.
- Hardest part as a solo hacker? Crunch before the 10 am deadline.
- Is the shown generation live or recorded? Live.

What went wrong: no sound for the pitch, timer not working, ran out of time before showing the live demo, the jury did not see the main feature until the Q&A.

## Patterns (evidence first, inference marked)

What Wavelet did that others did not:
1. It was a live demo of the real artifact, and the artifact was the pitch. Others mostly narrated slides, skits or videos.
2. Hard, original technical work with no AI wrapper. The jury had seen many LLM apps (3 of the 5 finalists used Gemini or an LLM somewhere); a from-scratch GPU physics simulator stood out (inference).
3. A clear gap statement: "no lightweight tool exists, only MATLAB or big-company tools".
4. Plain honesty about what failed (texturing), which made the rest credible.
5. It won the sponsor's own track, which signals fit to a challenge (inference: this likely helped).

What the judges kept asking about:
- Who actually built what, and what was built this weekend (asked of Wavelet, Walkthrough and Lambda Pump). Have each speaker state their part, and put builders on stage.
- Real-world application and next steps (Wavelet: 2 questions; Walkthrough: business model and who pays).
- Technical specifics: framework, models, why this one, GPUs, on-device vs cloud (Drone Stalker, LoreDash, Lambda Pump).
- Whether the demo is live or recorded and real.

Mistakes to avoid:
- Overrunning the time. 3 of 5 hit the cutoff (Walkthrough "times up", LoreDash, Drone Stalker). This year the pitch is 3 min, so rehearse to 2:45.
- Skits and long intros, and saving the demo for last (LoreDash never showed it in the pitch).
- Showing a concept video and saying it is the product (Walkthrough admitted it).
- Vague answers on roles and stack (Lambda Pump).
- Depending on sound, internet or a heavy GPU on stage without a backup. Test the stage audio and projector early, since 3 of 5 had AV trouble.
- Business-model blind spots in the Q&A, such as store owners not wanting faster shopping. Prepare the "who pays and why" answer.
- Not having the builders on stage.

Relevance to Vela (smart-glasses concept, my inference): the one wearable/AR team finalised but did not win, its demo was a video of a concept, and it got questioned on incentives. A glasses pitch likely needs a real on-device or live demo and a clear answer to "who pays".

Caveats: no judge list, no placement beyond winner, and no video of the ceremony. Nothing above about 2nd to 5th placing is known.

## Transcripts (clean, timestamped about every 30 s)

From YouTube auto-captions, in `research/transcripts/`:
- `transcripts/transcript_Wavelet_Uh3yPQuee1g.txt`
- `transcripts/transcript_Drone_Stalker_5x4mQtjzQB0.txt`
- `transcripts/transcript_Walkthrough_9KT34TKEBJ0.txt`
- `transcripts/transcript_Lambda_Pump_8yl6ji8T0lc.txt`
- `transcripts/transcript_LoreDash_43uQE6cZGXU.txt`
