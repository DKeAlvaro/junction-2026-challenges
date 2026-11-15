# Vela: submission text

## Project name
Vela

## Punchline
Vela is the AI companion for elderly people. Through Ray-Ban Meta glasses she whispers the name of the person in front of you, so forgetting a name never stops you from living on your own.

## Description
Vela is the AI companion for elderly people.

Many people over 70 or 80 want to keep living on their own, but some abilities are not what they used to be. The first thing to go is often names. People with early signs of Alzheimer's start to forget the names of the people they love the most. Forgetting a granddaughter's name in front of her is painful, so they stop going out, stop answering the door, and slowly stop living the way they want to.

**What Vela does.** Vela lives inside your Meta glasses and reminds you who you are seeing. A niece, an uncle, a neighbour, a doctor, any person you know. When someone you know comes into view, she says it softly in your ear: *"That's Diego, your grandson."* When she doesn't know the person, she stays silent.

**Teaching her takes one sentence.** Look at the person and say who they are: *"Vela, this is Pedro, my neighbour."* She asks how Pedro is related to you, repeats it back, you say yes, and she remembers. No forms, no screens to read, no new device to learn: it works by voice, in English or Spanish, and the wearer already wears glasses.

**How it works.**
- The glasses are the eyes, ears and speaker. A photo is taken every few seconds, and more often while a face is in view.
- The Vela app on the phone finds and compares faces on the device (Human, BlazeFace + FaceRes). Photos and faces never leave the phone.
- Speech goes to Whisper (Groq) for transcription, and a small language model (gpt-oss-20b) extracts the name and the relationship. Only text and sound go online, never images.
- Vela's calm voice is generated with ElevenLabs and cached. She speaks once per person every 10 minutes, so she never nags.
- A "For family" page shows the people she knows (edit or remove them) and today's moments.
- Voice commands: "remember this person", "who is this?", start/stop, "what can you do?", "repeat".

**Privacy and consent.** Vela only recognises people who have been introduced to her, and the wearer decides who is in her memory. Face data stays on the phone and can be deleted at any time. Recognition is designed for family, friends and neighbours who agree to be remembered.

**Built for the hackathon.** A working PWA plus an Android shell that connects to Ray-Ban Meta glasses through Meta's Wearables Device Access Toolkit, with the phone as a fallback "digital twin" of the glasses. Face matching was tuned on a test set (threshold 0.52, see `eval/`).

**Where it goes next.** Names are the first thing Vela watches over, not the last. The same loop (glasses sense, the app understands, Vela speaks one short line) can also catch scams before the wearer pays, double-check a pill against the schedule, record a doctor's visit with consent and give a short recap, and warn about a step ahead. We show these as vision, not as built.

**Who pays.** The wearer: the glasses once, plus a small monthly subscription. What they buy is more years in their own home, which is what most of them want and far cheaper than care. Later, insurers and municipal telecare services can subsidise it, as they already do with alarm pendants.

*I'm Vela. I'll help you remember the people you love.*
