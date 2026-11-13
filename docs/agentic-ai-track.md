# Agentic AI Track

## Hostinger — Decode the Noise

### Summary
Build an AI-powered tool that detects propaganda, bots and bad actors online – and deploy it live on Hostinger's infrastructure.

### Description

**Introduction**

The internet was built to connect people, but it has also become the world's most powerful manipulation machine. Propaganda spreads faster than facts, bot networks shape public opinion at scale, and bad actors exploit the open web with growing sophistication. At Hostinger we host millions of websites, so we see this noise up close – and we believe the same technology that powers the web can also protect it. We're bringing this challenge to Junction because the best detection ideas won't come from one company; they'll come from builders who can go from idea to a live tool in 48 hours.

**The challenge**

Build a tool that analyses text, social content or web-traffic patterns to detect signs of coordinated propaganda, bot-driven amplification or bad-actor behaviour online. Solutions can take many forms: an API, a dashboard, a classifier with an explainable verdict, or a monitoring service for site owners. Whatever you build, it must be deployed and running live on Hostinger's infrastructure by the end of the hackathon, with a public URL the judges can open. We care more about the strength and honesty of your detection logic – including how you handle false positives – than a polished front end.

### Prizes
- All three winning teams: All three winning teams will also receive **one year of Hostinger hosting and a domain** to keep their project live, **Hostinger swag**, and a **spotlight on Hostinger's social media channels**.
- 1st Place: 2000 €
- 2nd Place: 1000 €

## Tieto — Earned Trust in AI Code

### Summary
How does AI code review keep pace with AI-written code, while humans stay accountable for every change?

### Description

**Introduction**

It is Friday afternoon. A pull request lands from an agent. Two hundred lines, and your name is on the approval. Usually you would open the diff and start digging. But what if the change opened with its own explanation? What it does, why it was made, what else it touches, and how sure the AI is about each part. Suddenly you are not hunting for problems. You are checking a story, and questioning the parts that do not add up. Pick Earned Trust in AI Code, and help define how code explains itself now and in the future.

**Background**

Agent tokens passed human tokens in February 2026 and reached 7.3 trillion by August (OpenRouter data, a16z chart). Reviewing every change by hand does not scale, yet engineers need a sound basis to trust AI-reviewed code.

**The challenge**

Design an AI code review concept, then show it works. Define the concept, principles, reference implementation and technology considerations, across frontend, backend and security. Challenge the traditional model: is line-by-line review still the right way to ensure quality? Balance risk, hallucination, transparency, confidence and quality in AI review. The result is a reference implementation that illustrates the concept – it is not a product.

**What we expect from each team**

- Define the concept: what your team recommends the "PR review" factory should follow. State its key principles, including how it balances risk, hallucination, transparency, confidence and quality.
- Illustrate it as a reference, on one sample agent-written change with its requirement ID. Show what the AI found, what it refused to decide, and why.
- Show how the evidence lets a named human accept the change without a full read.
- Name the failure modes you saw, and keep a short log of decisions.
- Use synthetic or cleared sample data only.

**Deliverables**

- Concept card: recommendation, principles, trade-offs, limits
- Live walkthrough showing where the trust comes from
- Lessons log and a demo video/presentation

Out of scope: a finished product, model training and vendor selection.

Expected outcome: a concept with explicit trade-offs that humans can trust and be accountable for.

### Prizes
- 1st Place: €2,000 cash prize for the winning team.
- 2nd Place: €1,000 cash prize for the runner-up team.
- 3rd Place: €500 cash prize for the third-place team.

## Bahn Express — Spread

### Summary
Spread: run a car transport company for a week

### Description

Bahn moves cars for car dealers, and a freelance driver drives each car on its own wheels. Spread is that work as a simulated world: a whole week in Finland, with its dealers, its cars, its deadlines and its drivers. Your team builds the system that runs the company for that week.

A dealer asks you for a price, and asks a competitor too. Quote too high and you lose the car. Win it, and you post the drive as a gig in our drivers' app and choose the fee. Pay too little and no driver takes it in time, and the car arrives late.

Every team runs the same week, and you all stand on the same leaderboard. You make as much money as you can: your score is your gross margin, what the dealers pay you less what you pay the drivers. At least 90% of your cars must arrive by their deadline. The most money takes you to the top.

**Start**

Create your team at spread.bahnexpress.com/join with the event code spread-kmu9z6. Everything is on the site: the handbook, the rules, the API reference, the TypeScript and Python kits, and the leaderboard. Give your agent spread.bahnexpress.com/llms.txt .

**How you win**

Ranking rounds open from Friday 19:30. Every team plays the same secret weeks, so the leaderboard shows you where you stand. Our own best system plays every round. Beat it.

The final is on Sunday at 08:00. Every team plays its own copy of one secret week, which runs by itself for about 34 minutes. Registration closes at 07:30. The 10 ranked teams with the highest margin present to our jury, in 5 to 10 slides or a short video. The jury judges how elegant, clear, creative and robust your system is. Reaching the top 10 is enough. After that, your margin no longer counts.

Find us at the Bahn booth. Ask us anything about the rules, the world or real dispatch, or ask for a hint.

### Prizes
- 1st Place: 2000€
- 2nd Place: 1000€
- 3rd Place: 500€

## AfterQuery — Break the Agent

### Summary
Build a reinforcement learning environment that challenges today's best AI agents, demonstrate real failure modes, and show that its rewards reflect real progress.

### Description

**Introduction**

Today's cutting-edge AI systems can solve Millennium Problems, discover new drugs, and create entire production apps with a few lines of prompting. But they still struggle in a wide variety of novel situations, ranging from everyday use cases to niche, highly technical workflows. We ask: what should AI agents be able to do that they still struggle with today?

At AfterQuery, we build environments for training and testing agents. The work starts with choosing a problem worth learning, defining an action and observation space, and defining a reward function that defines what success looks like. Getting those pieces right is a heavy research and engineering problem in itself. For this challenge, we want to see your take on it. Build a world with something interesting to learn. Find out where strong agents struggle, and whether your reward actually encourages the behavior you intended.

**The challenge**

Choose a setting you find interesting and build an environment an agent can interact with. It could be a game, a scientific simulation, a software task, a real-world process, or something we haven't thought of. Explain why you chose it and what an agent could learn there. Your environment should have a clear goal, actions the agent can take, and a reward you can check.

Run a frontier agent in it and compare the results with a stronger reference run your team can demonstrate and reproduce. We'll provide the agent harness and model credits. Show where the agent falls short and why. The challenge should come from the decisions it needs to make, with access to the information and tools needed to succeed. We'll also try to find shortcuts that earn a high score without completing the task: reward hacking.

The setting and approach are yours to choose. We care about what makes the environment useful for learning and what your experiments reveal.

**Optional stretch goal**

Train a smaller model using experience from your environment and show whether it improves.

**Prizes**

The top three teams receive €3,000, €1,500 and €500 in cash. Members of the winning teams can go straight to the final stage of AfterQuery's interview process: a work trial with our environments team, when they're ready. Finalists also receive AfterQuery gear.

**How we judge**

We'll look at four things: how much room there is for the agent to improve, whether its mistakes come from meaningful challenges, how well the reward holds up to exploits, and how well the environment is built and the results can be reproduced.

**Judging rubric**

- The gap (30 p) – Full points: the frontier agent consistently scores below a stronger reference run your team demonstrates; both results can be reproduced across repeated runs. Zero points: no measurable gap, or the claimed gap cannot be reproduced or checked against a demonstrated reference run.
- Meaningful difficulty (30 p) – Full points: you can explain the agent's main mistakes and connect them to decisions in the task; the information and tools needed to do better are available to it. Zero points: the gap comes from unfairly withheld information, trick wording, impossible timing, or broken tools.
- Reward integrity (25 p) – Full points: the reward measures success at the task and holds up when judges try to exploit it; doing nothing or stopping early earns little or no credit; completing the task well remains the best way to score. Zero points: an exploit, scoring loophole, or strategy that avoids the task earns a better score than successful play.
- Craft (15 p) – Full points: the environment's rules and behavior make sense for the setting; judges can run the evaluation from your README with one command and reproduce your reported results. Zero points: the environment only works in your demo, or judges cannot reproduce the evaluation.

**How judging runs**

Each team gets a 10-minute demo. Judges then rerun the evaluation with the standard harness: your reference run, three agent runs, a do-nothing baseline, and a stop-early baseline. They also spend 15 minutes looking for reward exploits. Scores are based on these runs.

**Tiebreaker**

If point totals are close, we'll favor a team that shows a smaller model improving after training on experience from its environment.

### Judging
We'll look at four things: how much room there is for the agent to improve, whether its mistakes come from meaningful challenges, how well the reward holds up to exploits, and how well the environment is built and the results can be reproduced. Rubric: The gap (30 p), Meaningful difficulty (30 p), Reward integrity (25 p), Craft (15 p) – see full rubric, "How judging runs" and tiebreaker in the Description above.

### Prizes
- 1st Place: 3,000€ + A work trial at AfterQuery + Merch
- 2nd Place: 1,500€ + Merch
- 3rd Place: 500€

## Valio Aimo — Trusted Trade Agents

### Summary
How can a food-service wholesaler let autonomous purchasing agents place an order – finding products, comparing offers and getting the right approval in a fraction of the time it takes today – without exposing real systems, confidential data or the marketplace roadmap?

### Description

**Introduction**

Valio Aimo® serves 20,000+ professional kitchens and is planning to build a digital B2B marketplace connecting foodservice buyers and suppliers. As ordering shifts from people clicking through a catalog to AI agents making autonomous purchasing decisions, the question of how a wholesaler exposes itself to those agents – what they can see, decide and be trusted with – becomes existential for data ownership, trust, and who owns the customer relationship.

The Digital B2B Marketplace is a future step in this direction; for Junction 2026 we are mocking today's webshop and backend systems, not the marketplace itself. We want you to prototype the interface and operating model that would let an external purchasing agent interact with Valio Aimo's systems, built on open, verifiable standards rather than a single platform's black box.

**The challenge**

B2B ordering in foodservice and wholesale is still largely manual or menu-driven: a buyer logs into today's Valio Aimo webshop and searches a catalog. The step we want to explore is external purchasing agents that find, compare, order and handle exceptions on the buyer's behalf, working with Valio Aimo directly – not by building a whole marketplace, but by defining the interface and operating model through which an external agent could interact with Valio Aimo's systems at all.

**Core – your solution must enable**

- Product, price & availability lookup: a structured way for an external agent to search for and retrieve what's available and at what price.
- Requesting price & availability, then placing an order: a defined interaction for moving from inquiry to commitment, based on fixed prices rather than a negotiated quote.
- Permission & human-approval management: what the agent may decide on its own, and what must go to a human for sign-off.

**Optional – open directions (not required to win)**

- Delivery time & sustainability comparison: not just price, but delivery reliability and the certificates/sustainability labels already shown in the webshop. (Category-level carbon-footprint ranges are a stretch goal.)
- Substitution and other exception handling: what happens when the exact request can't be met. (Last year's Zero-Fail Logistics challenge covered failed deliveries in depth, so this isn't scored as core.)
- Traceability and explainability: a human-readable record of what the agent did and why.

**Example request**

"I need 1,000 litres of lactose-free milk by Monday. Find an option that meets our requirements based on price and availability."

A hotel chain's agent sends this request. Your solution returns products, prices and availability in structured form; the agent places the order within its authority or sends it to a human for approval.

**Impact**

This is not about replacing today's e-commerce UI with a chatbot. It is about defining how a European food-service wholesaler can be safely and openly readable by autonomous agents – before that interface gets defined by someone else's platform.

**Valio Aimo®**

Valio Aimo® was created in 2021 as a bold leap forward by Valio, transforming traditional wholesale into a next-generation foodservice powerhouse. We are more than a distributor: Aimo is where the breadth and agility of wholesale meet the deep product expertise, R&D capability, and brand-building strength of a global food innovator.

- 20,000 professional customers across restaurants, foodservice operators, and industrial customers rely on us to keep their business running every single day.
- 25,000 product names sourced from 700 trusted suppliers, forming one of the most comprehensive foodservice assortments in Finland.
- 350 specialists are committed to delivering excellence in logistics, service, and digital transformation.

Part of Valio, Finland's leading dairy and food company, with:
- €2.4B in revenue
- Operations in 60 export markets
- A pioneering sustainability mission: carbon-neutral milk by 2035

As part of Valio, Aimo represents the cutting edge of how foodservice can be reinvented for the AI-driven age. Valio Aimo® is not just serving today's kitchens; we are shaping the future of foodservice.

### Prizes
- 1st place: 4 000€
- 2nd place: 2 000€
- 3rd place: 1 000€

## Exa — The Internet Butler / Your Personal Assistant

### Summary
Build an agent that takes tedious tasks in people’s lives off their hands.

### Description

**Introduction**

Everyone has pain points in their day to day which require hours of digging and research like checking whether a rent increase is legal, or finding out which benefits a family qualifies for, which vegan restaurant to pick for an anniversary date, and more. The answers exist, but they are buried across the web. Exa is the search engine built for AI. It can find, read and compare information from across the web and pull it back as structured data, so your agent can do the digging and the task can be handed off completely.

**The challenge**

Develop a personal agent that helps people get stuff done. Your agent should find what matters across the web, work out what needs to happen and get the task as close to done as it can, leaving the final approval to the user if needed. Demo on a real case.

**Areas of interest**

General tasks. Examples: planning special occasions, handling daily living errands, rent, missed benefits, business information, travel disruption, etc.

**How we judge**

We will judge projects on how well they use Exa to get information that could not have come from a model's training data alone, how useful they are to a specific group of real people, and how clearly they show their sources. We will also look at originality and at whether the demo works on live queries, including ones the judges try themselves.

The winning team will receive [cash amount] and [Exa API credits per member], and the two runner-up teams will receive [amounts]. Every team that submits a working project built on Exa will receive [API credits] to keep building after the event. [Consider a mentoring session or visibility on Exa's channels for the winners.]

**About Exa**

Exa is a search engine built for AI. We index the web by meaning, so AI applications can find information by describing what they need, and we return clean, structured content that models can use directly. Companies such as Cursor, Cognition, HubSpot and AWS use Exa to connect their products to the web. We are joining Junction to meet builders, see new ideas for what AI can do with access to the whole web, and keep supporting promising teams after the event.

### Judging
We will judge projects on how well they use Exa to get information that could not have come from a model's training data alone, how useful they are to a specific group of real people, and how clearly they show their sources. We will also look at originality and at whether the demo works on live queries, including ones the judges try themselves.

### Prizes
- 1st Place: $2,500 Cash, $5,000 in Exa credits, Exa hoodie per person & Exa branded TRMNL dashboard
- 2nd Place: $1500 cash, $3,000 in Exa credits, Exa hoodie per person & Exa branded macropad
- 3rd Place: $500 Cash, $1k Exa credits & Exa hoodie per person
