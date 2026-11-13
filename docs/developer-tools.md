# Developer Tools and Assets

Source: "Developer Tools and Assets" page on the Junction platform. Condensed, keeping credits, codes and links.

## Credits at a glance

| Partner | What we get |
|---|---|
| Verda | 200 EUR credits (GPU compute + inference API). Sign up to Verda Console, claim via their form, share with team via their docs |
| OpenAI | 100 USD Codex credits per participant |
| Anthropic | 20 USD Claude API credits per participant |
| Google DeepMind | Gemini API credits for eligible participants |
| Modal | 100 USD per participant, CPUs and GPUs (T4 up to B300) |
| Exa | 50 USD credits per participant, full API |
| Aiven | 50 USD free credits |
| Featherless | 50 USD API credits via a dedicated Junction coupon; GPU credits (bare metal) for selected teams |
| CRACI | 1000 EUR credits per team (CI/CD and compute) |
| Context.dev | 50,000 API credits per team, no expiry, no card needed, 50 concurrent requests |
| Oxylabs | Code `JUNCTION2026`: first month free on the 500 USD Flexible plan. Card required, cancel afterwards |
| Cloudinary | Generous free tier |
| MariaDB | Open to every team, mention it in the submission |

## Partners

### Verda: AI compute
Full-stack AI cloud (GPU compute, inference API). Claim 200 EUR credits through their form after signing up to the console.

### OpenAI: Codex credits
100 USD per participant for Codex and OpenAI developer tools: prototyping, agents, dev workflow.

### MariaDB: database
Open to every team. They look for the most interesting use of the database itself (schema, queries, features). Visit their booth or mention MariaDB in the submission. Projects are published and credited on mariadb.org.

### Google DeepMind: Gemini API
Gemini API credits for eligible participants.

### Anthropic: Claude credits
20 USD of Claude API credits per participant.

### Aiven
50 USD free credits. Docs, runtime templates for popular open-source frameworks, mentors on site all days.

### Arduino: App Lab and hardware
- Borrow Arduino UNO Q kits from the Arduino Hardware Lab (5th floor). Booking instructions: https://2026.hackjunction.com/hardware
- Kit: UNO Q (2 GB RAM, 16 GB eMMC), USB-C cable, USB-C hub (8 in 1), 45 W power supply, USB camera, Modulino Buzzer, Knob and Thermo sensors.
- Software: Arduino App Lab (https://www.arduino.cc/en/software/#app-lab-section). Bring a laptop with it installed.

### CRACI: CI/CD platform
- 1000 EUR credits per team. GitHub Actions compatible runners, build-time CycloneDX SBOMs, AI vulnerability fixes, API.
- Setup (~10 min, one person per team):
  1. Get the Junction invite code (Discord `#craci` channel or the CRACI booth, 3rd next to the stage).
  2. Sign up at platform.craci.com and create an organization with the invite code.
  3. Settings > Builds > Install GitHub, grant repo access.
  4. In workflows use `runs-on: craci` (default 2 vCPU / 6 GB). For more: `uses: cracicorp/setup@v1` with `size: "8"` (1-32 units, each 1 vCPU + 3 GB).
  5. API token under Settings > API tokens (shown once). API at https://api.craci.com, `Authorization: Bearer $CRACI_API_TOKEN`, spec at api.craci.com/openapi.json.
- Docs: https://docs.craci.com/ · migration skill for agents: https://docs.craci.com/skills/craci/SKILL.md

### Cloudinary: image and video API
Upload, transform, optimize and deliver media. Tools to use: https://cld.media/hackathons. To submit to their challenge, fill https://cld.media/hackathon-survey.

### Modal: GPUs and CPUs
- 100 USD per participant, per-second billing, scales to zero. GPUs: T4, L4, A10, L40S, A100, RTX PRO 6000, H100, H200, B200, B300.
- `pip install modal`, `modal run`, `modal deploy` (autoscaling web endpoint with public URL). Sandboxes, Volumes, Dicts, Queues, Modal Dojo for fine-tuning and RL.
- Junction starter kit with examples (vLLM, SGLang, STT, TTS, vision, RAG, agents, RL). Kick-off workshop at their booth. "Best use of Modal" is a tech challenge you enter on top of your main one.

### Oxylabs: Web API
`/search` and `/scrape` endpoints returning Markdown, HTML, JSON or screenshots; handles proxies, JS rendering and bot checks. MCP server and agent skills available. Code `JUNCTION2026` (see table).

### Context.dev: API credits
50,000 free credits per team. Search and scrape, structured extraction with your own schema, company/brand data, monitors and webhooks. SDKs: TypeScript/Node, Python, Ruby, Go, plus an MCP server.

### IronShard: datasets and storage
- S3-compatible and MCP-accessible object storage. Challenge datasets are preloaded in read-only buckets; fork one with a click into a writable bucket (zero-copy).
- Use it for large artifacts (models, datasets) that do not fit in GitHub (100 MiB per file limit). Put bucket and object references in the submission; judges get read access.

### Junction Hardware Lab
Devices to borrow on the 5th floor.

### Wendy
Run apps on Jetson, Raspberry Pi, ESP32 or Arduino with `wendy run` (Python, Swift, Rust, ROS). Simulator available if there is no hardware.

### Qualia: robot data platform
Upload demonstration datasets (SO-101 arms or Rokoko mocap), automatic quality checks per episode, curate and version the set, export for training (e.g. pi0.5 with LeRobot).

### Featherless
- GPU credits (bare-metal, Featherless Cloud) for selected teams.
- API: dedicated Junction coupon for 50 USD of credits, open-weight model catalog.

### Scailab: Scaipipe
Computer vision pipeline in the browser: annotate images, generate labelled synthetic data from 3D scenes, train and evaluate detection/segmentation/tracking models. Built-in MCP server so agents like Claude can drive it.

### Exa: credits
50 USD per participant. Search API (fast, balanced, deep research modes), Contents API, Websets, Monitors, hosted MCP server, Python and JS SDKs. Demo gallery: demos.exa.ai. Engineers on site and a Discord for async help.
