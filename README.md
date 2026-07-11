<div align="center">

# Easy Starter Messaging Bot

**A multi-channel bot foundation for Telegram, Bale, WhatsApp, and other messaging platforms using adapter-based architecture.**

[![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?logo=github&logoColor=white)](https://github.com/easy-starter/easy-starter-messaging-bot/generate) [![CI](https://github.com/easy-starter/easy-starter-messaging-bot/actions/workflows/ci.yml/badge.svg)](https://github.com/easy-starter/easy-starter-messaging-bot/actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) ![Status: foundation](https://img.shields.io/badge/status-foundation-orange) ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) ![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white) ![Multi-channel](https://img.shields.io/badge/Multi--channel-1f6feb) ![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)

[فارسی](README.fa.md) · [Documentation](https://github.com/easy-starter/easy-starter-docs) · [Report an issue](https://github.com/easy-starter/easy-starter-messaging-bot/issues/new/choose)

</div>

> “What do we build for, if not to lessen each other’s hardship?”

> [!IMPORTANT]
> This repository is currently in the **foundation stage**. Do not treat it as production-ready until the first stable release.

## What it solves

Separates conversation and business logic from platform APIs so one bot product can support multiple channels without duplicating its core.

## Use this template for

- Command and workflow bots
- Customer support and human-handoff bots
- Notification and content-delivery bots
- AI assistants and transactional bots
- Telegram, Bale, and WhatsApp channel adapters

**Not intended for:** A platform-specific codebase duplicated for every messenger or an unofficial API bypass.

## Baseline

- Channel-neutral message and conversation models
- Adapter interfaces for inbound updates and outbound messages
- Webhook, polling, state, command, and middleware boundaries
- Rate-limit, retry, deduplication, and observability conventions
- Admin, tests, Docker, CI, and deployment profiles

Detailed architecture, conventions, deployment profiles, and extension guides belong in [`docs/`](docs/). Feature work starts from [`specs/`](specs/), and agent rules live in [`AGENTS.md`](AGENTS.md).

## Quick start

1. Click **Use this template** or run:

   ```bash
   gh repo create my-project --template easy-starter/easy-starter-messaging-bot --private --clone
   cd my-project
   ```

2. Set the project name, package metadata, and environment values.
3. Start the project:

   ```bash
   cp .env.example .env
   make setup
   make dev
   make check
   ```

4. Write the first feature specification under `specs/`.
5. Implement the feature and keep `make check` green.

## Working agreement

- Read `AGENTS.md` and the relevant specification before changing code.
- Reuse existing patterns before adding abstractions or dependencies.
- Never commit credentials or production data.
- Run the repository quality checks before opening a pull request.
- Record architecture-changing decisions in `docs/decisions/`.

## Documentation

Start with `docs/getting-started.md`. Broader AI-first development guidance is maintained in [Easy Starter Docs](https://github.com/easy-starter/easy-starter-docs).

## Contributing and support

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for contribution rules and [`SUPPORT.md`](SUPPORT.md) for help. Security issues must follow [`SECURITY.md`](SECURITY.md).

## License

Released under the [MIT License](LICENSE).
