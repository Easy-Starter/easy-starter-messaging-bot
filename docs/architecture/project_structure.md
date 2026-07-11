## Project Structure

easy-starter-messenger-bot/
├── .github/
│ ├── workflows/
│ │ ├── ci.yml
│ │ └── security.yml
│ └── pull_request_template.md
│
├── docs/
│ ├── architecture/
│ ├── channels/
│ ├── deployment/
│ └── development/
│
├── specs/
│ └── README.md
│
├── src/
│ └── easy_starter_messenger_bot/
│ ├── api/
│ │ ├── dependencies.py
│ │ ├── errors.py
│ │ ├── router.py
│ │ └── routes/
│ │ ├── health.py
│ │ ├── internal.py
│ │ └── webhooks/
│ │ ├── telegram.py
│ │ ├── bale.py
│ │ └── whatsapp.py
│ │
│ ├── application/
│ │ ├── dispatcher.py
│ │ ├── handlers/
│ │ │ ├── start.py
│ │ │ ├── help.py
│ │ │ └── fallback.py
│ │ └── use_cases/
│ │ ├── process_inbound_event.py
│ │ └── send_outbound_message.py
│ │
│ ├── channels/
│ │ ├── registry.py
│ │ ├── telegram/
│ │ │ ├── adapter.py
│ │ │ ├── client.py
│ │ │ └── mapper.py
│ │ ├── bale/
│ │ │ ├── adapter.py
│ │ │ ├── client.py
│ │ │ └── mapper.py
│ │ └── whatsapp/
│ │ ├── adapter.py
│ │ ├── client.py
│ │ └── mapper.py
│ │
│ ├── core/
│ │ ├── config.py
│ │ ├── exceptions.py
│ │ ├── logging.py
│ │ ├── security.py
│ │ └── types.py
│ │
│ ├── domain/
│ │ ├── enums.py
│ │ ├── models/
│ │ │ ├── inbound.py
│ │ │ ├── outbound.py
│ │ │ └── conversation.py
│ │ └── ports/
│ │ ├── messenger.py
│ │ └── repositories.py
│ │
│ ├── db/
│ │ ├── base.py
│ │ ├── session.py
│ │ ├── models/
│ │ └── repositories/
│ │
│ ├── workers/
│ │ ├── broker.py
│ │ ├── scheduler.py
│ │ └── tasks.py
│ │
│ └── main.py
│
├── migrations/
│ ├── versions/
│ └── env.py
│
├── tests/
│ ├── unit/
│ ├── integration/
│ ├── contract/
│ └── conftest.py
│
├── scripts/
│ ├── register_webhooks.py
│ ├── delete_webhooks.py
│ └── generate_secret.py
│
├── .dockerignore
├── .editorconfig
├── .env.example
├── .gitignore
├── .pre-commit-config.yaml
├── AGENTS.md
├── compose.yml
├── Dockerfile
├── Makefile
├── pyproject.toml
├── README.md
└── uv.lock

## Flow

Messenger
│
▼
Webhook Endpoint
│
├── Verify signature/secret
├── Parse payload
├── Normalize event
└── Store inbound event
│
▼
Task Queue
│
▼
Message Dispatcher
│
▼
Application Handler
│
▼
Outbox Message
│
▼
Messenger Adapter
│
▼
Messenger API
