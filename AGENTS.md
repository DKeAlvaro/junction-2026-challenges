# AGENTS.md

Junction 2026 hackathon workspace. Challenge texts are in `docs/` (one file per track; sponsor tooling in `docs/developer-tools.md`).

## API keys

All keys live in `.env` at the repo root (gitignored, never commit or print them). Load with `set -a; source .env; set +a` or your framework's dotenv.

| Variable(s) | Service | Use it for | Credits |
|---|---|---|---|
| `ANTHROPIC_API_KEY` | Anthropic | Claude models (reasoning, agents, tool use) | 20 USD |
| `OPENAI_API_KEY` | OpenAI | GPT models, embeddings, Whisper, TTS, Codex | 100 USD |
| `GEMINI_API_KEY` | Google DeepMind | Gemini models, multimodal (image/video/audio) | eligible-participant credits |
| `FEATHERLESS_API_KEY` | Featherless | Open-weight LLMs through an OpenAI-compatible API | 50 USD |
| `EXA_API_KEY` | Exa | Web search, contents, Websets, research mode | 50 USD |
| `CONTEXT_DEV_API_KEY` | Context.dev | Web search/scrape, structured extraction, company/brand data | 50,000 credits per team |
| `MODAL_TOKEN_ID`, `MODAL_TOKEN_SECRET` | Modal | GPUs/CPUs, `modal run` / `modal deploy`, vLLM, fine-tuning | 100 USD |
| `AIVEN_API_TOKEN` | Aiven | Managed databases/services (Postgres, Kafka, etc.) | 50 USD |
| `CLOUDINARY_CLOUD_NAME`, `CLOUDINARY_API_KEY`, `CLOUDINARY_API_SECRET` | Cloudinary | Image/video upload, transform, delivery | free tier |
| `CODEX_REDEEM_LINK` | OpenAI Codex | Link to redeem the Codex credits (not an API key) | 100 USD |

## Rules

- Budgets are small: prefer cheap models for bulk work, and don't loop paid calls without a cap.
- Keep Modal jobs short and scale-to-zero; stop anything left running.
- Never hardcode keys in code, docs or commits; read them from the environment.
- Not available here (no key): Oxylabs, CRACI, IronShard, MariaDB, Qualia, Scailab, Wendy.
