# Vela: product vision

*Draft 1, 13 November 2026. Hackathon concept.*

**One line:** Vela is the guardian in your glasses that lets you live on your own without being on your own.

**Taglines to test:** "Live alone. Never on your own." / "Your home, not a home."

---

## 1. What it is

Vela is an AI guardian for older people that runs on Meta smart glasses. She sees what the wearer sees, hears what they hear, and steps in only when it matters. She speaks in a calm voice, in the wearer's ear. The firefly is her visual identity (brand, family app, launch film), not something drawn on a lens.

Vela is one product, not five tools. The wearer never opens a "scam feature" or a "pill feature". They wear their glasses and Vela watches over the day.

## 2. The problem

Most older people want to stay in their own home. What ends that is rarely one big event. It is a run of small failures: a missed pill, a fall on a step, a scam call, a forgotten name that makes them stop going out. Each one pushes the family closer to deciding that living alone is no longer safe.

Today's answers arrive after the damage. An alarm pendant calls for help once someone is on the floor. A bank flags fraud once the money has gone. Nothing sits with the person in the moment before.

## 3. Who it is for

| | Who | What they want |
|---|---|---|
| **Wearer, who pays** | 70+, living alone or with a partner, still independent, starting to have slips | To keep their home and their pride. Not to be monitored or talked down to. |
| **Family** | Their adult children, often in another city. They don't pay, and the wearer chooses what they are told | To stop worrying, without calling five times a day. |
| **Later** | Insurers, home-care providers, municipal telecare services | Fewer falls, hospital stays and care-home admissions. They may subsidise Vela, as many already do for personal alarms. |

Not for: people with advanced dementia or people who need hands-on care.

**Who pays: the wearer.** Vela works for the person wearing it, not for their children, so the wearer buys it, the way they already buy their glasses and hearing aids.
- **What they pay:** the glasses once, at the optician, plus a monthly Vela subscription. The price is not set yet; a first anchor is what a personal alarm subscription costs today.
- **Why they pay:** more years in their own home, on their own terms. The alternative the family is drifting towards, moving into care, costs thousands a month and costs them their home.
- **Why it helps the product:** the wearer owns the account and decides who is told what. The family gets "all fine" and the moments the wearer chose to share, never a feed. Privacy becomes part of the business model, not just a policy.
- **Gifts:** family can still buy it as a present, but ads and the pitch speak to the wearer.

**Answer to the judges' "who pays?"** (about 15 s): "The wearer. Older people already pay for their glasses and hearing aids at the optician. Vela is sold the same way: the glasses once, plus a small monthly subscription. What they buy is more years in their own home, which is what most of them want and far cheaper than care. Later, insurers and municipal telecare services can subsidise it, as they already do with alarm pendants."

## 4. How it works

Vela has five watches. The wearer never asks for anything. Vela keeps watch on her own, notices when something needs attention, and steps in before the problem happens. All of them run through the same loop: the glasses sense, Vela's app on the phone understands, and when something matters Vela speaks one short line in the ear. When nothing matters she stays silent.

| Watch | What Vela does | Uses | Buildable for the hackathon? |
|---|---|---|---|
| **Scams** | **She notices:** a letter in the wearer's hands that demands money, a text on a screen that looks like fraud, or a stranger at the door pushing for entry or payment.<br>**She steps in before the harm:** on her own, before the wearer pays, answers or opens the door. She compares what she sees and hears with known fraud patterns (urgent payment, "your account is blocked", a relative "in trouble", a prize).<br>**The wearer hears:** a calm warning and one suggestion, e.g. "This letter asks you to pay today. Banks don't do that. Shall I call Marta?" If the wearer says yes, she calls the trusted relative. | Camera, mic | Yes for letters, texts and doorstep. Live phone-call audio is likely hard to reach from a third-party app; verify. |
| **Second look** | **She notices:** the wearer picks up a pill bottle or blister pack at the usual medication time, or about to take a pill that is not on today's list, or has already taken today's.<br>**She steps in before the mistake:** she checks what is in the hand against the schedule the family entered, and speaks before the pill is swallowed. She also notices when the medication time has passed and the pills have not been touched, and reminds gently.<br>**The wearer hears:** "The blue one is done for today." or "It's time for the white one." Never a reproach. Leaving the house without keys, or the stove on, are later additions: they need a memory of past photos. | Camera | Yes. Photo to a vision model, spoken answer. Start with the pill; keys and stove come later. |
| **Appointments** | **She notices:** the wearer arrives at a medical appointment (known from the family calendar, the doctor's office in view, or a doctor speaking in a consultation).<br>**She steps in:** offers to listen, and starts only once the doctor agrees to be recorded. Otherwise she stays silent.<br>**The wearer hears:** a short spoken recap right after the visit: what changed in the medication, what to do next, the next appointment. The family gets a written version in their app. | Mic | Yes. Needs the doctor's consent to record. |
| **Faces** | **She notices:** someone enrolled comes into view and the wearer seems to hesitate or not greet them.<br>**She steps in before an awkward moment:** quietly, so the wearer can greet them by name.<br>**The wearer hears:** a whisper such as "This is Pedro, your neighbour from the second floor." Only people who gave explicit consent are ever recognised. | Camera | Technically yes. Legally sensitive, see section 11. |
| **Steps** | **She notices:** over weeks, a change in how the wearer walks (slower pace, shorter steps, more sway). In the moment, a step, loose rug or dark patch ahead.<br>**She steps in before the fall:** with a short warning just ahead of the hazard. The slow change over weeks goes to the family as a trend, not a medical judgement.<br>**The wearer hears:** "Careful, a step ahead." | Motion sensors, camera | Vision only. Show it, do not build it. |

**What the platform allows today**

- Meta's Wearables Device Access Toolkit reached a stable 1.0 on 30 September 2026. It gives a phone app the glasses' camera stream, photo capture, microphone, audio and motion sensors.
- The app runs on the phone. The glasses are the eyes, ears and screen.
- The toolkit can also draw on the lens of Meta Ray-Ban Display, but the wearer has to start each display session. Vela does not use it (see "Hardware decision").
- Store publishing is not open yet. Developer Mode is enough for a hackathon.
- In Europe, Meta Ray-Ban Display is sold only in the UK, France, Italy and Germany, at about €899. Full toolkit access is limited to Meta's supported countries.

**Hardware decision.** Vela targets **Meta Ray-Ban Gen2** (camera, microphones, open-ear speakers, no display). Vela only ever talks to the wearer by voice, so a lens adds nothing the product needs. Reasons:
- The five watches need camera, mic and audio only, all available on Gen2 through the toolkit.
- Gen2 is sold and supported in more countries than Ray-Ban Display, so less risk with accounts and toolkit access.
- Glasses are barely intrusive. They look like ordinary glasses, so there is no pendant, bracelet or box that marks the wearer as "someone who needs watching". Gen2 keeps that, and a lens display would make them more noticeable.
- Voice suits the user: no screen to read, nothing new to learn, works for people with poor eyesight.
- Display stays a possible later extension, for example a short line for people who are hard of hearing.

**Development without glasses (digital twin).** All of Vela is built against a small glasses interface: get a frame, get audio, say a line. Today the phone implements it (rear camera, microphone, speaker). When the glasses arrive, the toolkit implements it. Meta's Mock Device Kit is used to test that integration before the hardware is in hand. Keep the same limits as the glasses from day one: single photos rather than continuous video, mono Bluetooth audio, one short spoken line per answer.

**Gap between demo and vision.** A real guardian is always on. Today a session has to be started by the wearer and the battery lasts around six hours of mixed use. The hackathon build should show Vela stepping in at chosen moments. The pitch should say plainly that always-on is where it is going.

## 5. Why it is useful

- **For the wearer:** more years at home, fewer frightening moments, no new device to learn, and nothing that looks like a care gadget. They already wear glasses.
- **For the family:** a short daily "all fine" instead of constant worry, and a call when something needs them.
- **For health and care systems:** a fall or a missed prescription avoided is far cheaper than a hospital bed.

## 6. Motivation in numbers (Europe)

| Fact | Figure | Source |
|---|---|---|
| People aged 65+ in the EU, 1 January 2025 | 22.0% of 450.6 million, about 99 million | Eurostat |
| Share aged 65+ by 2050 | Almost one in three | Eurostat / JRC |
| Share aged 80+ | Doubles, 6.2% to 13.3%, by 2050 | Eurostat / JRC |
| Older people living alone (EU-27, 2018) | 40.2% of women 65+, 21.8% of men | Eurostat |
| People 65+ who fall each year | 28 to 35% | WHO |
| People with dementia, EU-27 | 9.1 million in 2025, 14.3 million by 2050 (+58%) | Alzheimer Europe |
| Deaths linked to not taking medication as prescribed | Almost 200,000 a year in the EU | European Commission estimate, 2011 |
| Cost of that non-adherence | €80 to 125 billion a year | Same |
| Medical information a patient forgets straight after a visit | 40 to 80% | Kessels, 2003 |
| Older people in England and Wales who were fraud victims in a year | About 1 in 12 | Age UK |

**Weak spot:** there is no clean EU-wide figure for fraud against older people. The numbers found are national (UK, Switzerland, Spain). Find one before the pitch or use a national one and say so. The medication figures are from 2011 and still widely quoted; say "estimated".

## 7. Brand

- **Name:** Vela. In Spanish, *velar por alguien* means to watch over someone, and a *vela* is a candle.
- **Character:** a firefly. She is a light, not a toy. No cartoon face, no childish voice.
- **Personality:** calm, brief, respectful. She never says "you forgot". She says "the blue one is done for today".
- **Voice:** warm, unhurried, short sentences. Never alarmed, even when warning.
- **Colour:** warm amber on near-black, with soft cream for print and web. Amber on dark is used for the family app, the website and the launch film.
- **Type:** a humanist serif for the wordmark, a large clear sans for everything the wearer reads.
- **Avoid:** medical blue, stock photos of smiling pensioners, the word "elderly", anything that looks like a hospital product.

## 8. How it looks

- **In the ear:** Vela speaks one short line when something matters, and is silent otherwise. One line, never a menu. A soft chime can precede it.
- **No screen on the glasses.** The firefly lives in the brand, the family app and the film, where it glows when Vela steps in.
- **Phone app for the family:** a single screen. "Today: all fine." Below it, the few moments Vela stepped in. No live camera feed of the parent.
- **Setup:** done once at the optician when the glasses are fitted, or with the family. The wearer chooses who gets the family app. After that, the wearer's part is to put the glasses on.

## 9. Advertising

**After the hackathon:**
- The wearer pays, so ads speak to the wearer first, through places they already trust.
- Opticians are the obvious channel. Older people already buy their glasses there, and the optician can set Vela up at the fitting.
- Pharmacies, family doctors and insurers are the next ones.
- Main ad: the wearer and independence. Secondary ad: the family, as a gift and for peace of mind.

## 10. Launch video

No style is locked yet. Shoot one shared body and three openings, then choose in the edit.

**Shared body: "A day with Vela" (45 to 60 s).** One person, one day, filmed through the glasses where possible. Vela steps in a few times: the morning pill, a letter that is a scam, a neighbour's name at the door, the summary after the doctor. This is how all five watches fit in one film without it becoming a feature list.

**Opening A, the pain.** A phone rings in a quiet flat. A voice says "Mum, it's me, I've had an accident, I need you to send money." Cut to black. Then the numbers.

**Opening B, the numbers.** White figures on black, one at a time: 99 million, one in three falls, 200,000 deaths. Then "Nobody is watching. Until now."

**Opening C, the keynote.** One presenter, dark stage, the glasses in hand, in the style of the Rabbit R1 and Humane AI Pin launch films.

**A warning about C.** Those two films were well made and both products were badly reviewed once people used them; Humane stopped selling the Pin in 2025. Borrow their clarity and design discipline. Do not borrow the overpromise: show only what works on camera and label the rest as vision.

**Practical:** 60 to 90 seconds, English, subtitles burned in, real footage from the glasses for at least one moment.

## 11. Risks

- **Privacy.** A camera that is always on, in a home, pointed at other people. The family app must never be a surveillance feed.
- **Face recognition.** Faces are biometric data under EU privacy law and need explicit consent from each enrolled person. Check Meta's developer policy too.
- **Medical claims.** Say "points out" and "confirms". "Prevents falls" or "manages medication" would make Vela a medical device.
- **Trust.** One false scam alarm or one wrong pill confirmation costs more than ten correct ones earn.
- **Adoption.** The wearer has to accept the glasses, charge them and wear them.
- **Platform.** Vela depends on Meta's hardware, rules and country list.

## 12. Still to decide

- Confirm the Gen2 loan is secured (2 of 10 were free at last check).
- Whether the team's country is on Meta's supported list.
- Which two watches are built for real and which are shown as vision.
- The hackathon's judging criteria, date and video length limit.
- Which video opening wins.
- A trademark check on "Vela".
- The monthly price, and whether the glasses are sold bundled with the subscription.

---

## Sources

- [Population structure and ageing (Eurostat)](https://ec.europa.eu/eurostat/statistics-explained/index.php/Population_structure_and_ageing)
- [EU population to decline from 2029 (bne IntelliNews, on the JRC/Eurostat report)](https://www.intellinews.com/eu-population-to-decline-from-2029-east-west-demographic-divide-widens-454611/)
- [EU Perspectives on the 2050 projections](https://euperspectives.eu/?p=24201)
- [Ageing Europe: housing and living conditions (Eurostat)](https://ec.europa.eu/eurostat/statistics-explained/index.php/Ageing_Europe_-_statistics_on_housing_and_living_conditions)
- [WHO global report on falls prevention in older age](https://www.who.int/publications/i/item/9789241563536)
- [The Prevalence of Dementia in Europe 2025 (Alzheimer Europe)](https://www.alzheimer-europe.org/news/new-alzheimer-europe-report-projects-64-increase-dementia-across-europe-2050)
- [Medication non-adherence in the EU (PMC, citing European Commission/MEDI-VOICE 2011)](https://pmc.ncbi.nlm.nih.gov/articles/PMC8544003)
- [Patients' memory for medical information (Kessels, 2003)](https://pmc.ncbi.nlm.nih.gov/articles/PMC539473)
- [Older person becomes fraud victim every 40 seconds (Age UK)](https://www.ageuk.org.uk/latest-press/articles/2019/july/older-person-becomes-fraud-victim-every-40-seconds/)
- [Meta Wearables developer FAQ](https://developers.meta.com/wearables/faq/)
- [Display access overview (Meta developer docs)](https://wearables.developer.meta.com/docs/develop/dat/display-overview/)
- [Meta Ray-Ban Display: new features and international launch (UploadVR)](https://www.uploadvr.com/meta-ray-ban-display-gets-new-features-online-ordering-international-launch/)
- [Meta unveils Ray-Ban Display and Ray-Ban Meta Gen 2 (GSMArena)](https://m.gsmarena.com/meta_rayban_display_and_rayban_meta_gen_2_smart_glasses_debut-amp-69560.php)
