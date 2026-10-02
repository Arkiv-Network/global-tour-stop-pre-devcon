# AGENTS.md — Arkiv × Devfolio Builder Challenge, India Edition

Context for AI coding agents (Claude Code, Cursor, Copilot, Codex…) helping a builder in this challenge.

## What this repo is

The official rules and resources for a 10-day online build on Arkiv, the Web3 database (9–18 October 2026), themed on CROPS: censorship resistant, open source, private, secure. This repo is the canonical source; if another surface disagrees, this repo applies.

| Question | File |
|---|---|
| What is the challenge? | [README.md](README.md) |
| Rules, eligibility, prizes, KYC | [RULES.md](RULES.md) |
| How is it scored? | [docs/scoring-rubric.md](docs/scoring-rubric.md) |
| What do I submit? | [docs/submission-checklist.md](docs/submission-checklist.md) |

## Key facts

- One CROPS pillar per project. Same rubric for all: Why this pillar? 25 · Why Arkiv? 25 · How you use Arkiv 25 · Friction report 25.
- Gates before scoring: working deployment, reproducible, public MIT repo, `/arkiv/schema.md`, `/arkiv/friction.md`, entity keys + tx hashes on Tiramisu, demo video ≤ 3 min, built 9–18 October.
- Prizes require attending Devcon 8 (Mumbai) and demoing at the Arkiv booth on 3–4 November; payout comes after the demo.
- Network: Tiramisu testnet, chain ID `7738577`, RPC `https://rpc.tiramisu.db-chain.testnet.arkiv.network`, WebSocket `wss://rpc.tiramisu.db-chain.testnet.arkiv.network`.
- SDK: `@arkiv-network/sdk` 0.8.x. Docs: https://docs.arkiv.network

## Hard rules for the SDK (0.8)

Do not reinvent these; check the installed package when unsure.

- **Queries:** `client.select().where(...).limit(...).fetch()`, plus `ownedBy()`, `createdBy()`, `cursor()`. There is **no server-side ordering** (no `orderBy`); sort on the client, or range-filter on `$createdAt`. Max 200 results per page.
- **Ranges only on numeric attributes.** Store timestamps, amounts and scores as numbers.
- **The payload is not queryable.** Anything you filter on goes in attributes.
- **Everything expires.** Set an expiry per entity type. Lifetime Extension (`extendEntity`) **sets** a new expiry; it reverts if the new one is not later.
- **Trust comes from `$creator`** (immutable). `$owner` is mutable and controls writes.
- **Live updates:** `watchEntityEvents` opens a real socket only with a WebSocket transport and no `fromBlock`; over HTTP it silently polls.
- All entities are publicly readable. Privacy means encrypting or hashing the payload, never a private toggle.
- Never put private keys, secrets or personal data in an entity.

## Vocabulary

Say "Entity Expiration" and "Lifetime Extension". Never write "TTL". Avoid "trustless" and "fully decentralized".

## What to ask the builder before coding

1. Which CROPS pillar, and who is harmed today without this project?
2. Why does it need Arkiv instead of Postgres, IPFS or an API, and what stays off Arkiv?
3. A funded test wallet on Tiramisu (never paste its private key into chat or code; use an env var).
4. The product's entity types and the 2–3 questions the app must answer, so the schema is designed before the UI.

Write `/arkiv/schema.md` and keep `/arkiv/friction.md` updated while building: both are required.
