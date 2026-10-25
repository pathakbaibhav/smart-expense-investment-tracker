# Smart Expense & Investment Tracker

Turns messy money data — bank SMS, email alerts, CSV/PDF statements, CAMS/KFintech CAS — into clean, categorized, queryable data, with a private local-LLM layer for parsing, categorization and plain-language questions.

**Status:** Phase 0 (foundations).

## Principles

- Ingestion is asynchronous and idempotent: raw input is stored first and can be re-parsed.
- Layered parsing: regex → local LLM → human review. Not everything goes to an LLM.
- Money is stored as integer paise, never floats.
- Postgres row-level security isolates every user's data.
- Built entirely on free tooling; financial data never leaves the machine.

## Planned stack

FastAPI · PostgreSQL + pgvector · Postgres job queue · Ollama · Next.js + Tailwind + shadcn/ui · Docker Compose
