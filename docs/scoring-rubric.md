# Scoring rubric

Every submission is judged by the Arkiv team in two steps: **gates**, then **score**.

## 1. Gates (pass or fail)

A submission that fails any gate is not scored.

- [ ] **It works.** A public deployment judges can open without asking for access. This applies to every pillar: a library, CLI or dataset ships with a deployed app or product that shows how it is used and the value it adds.
- [ ] **It can be reproduced.** The steps and the exact query in the submission produce what the submission says.
- [ ] **Public repo under the MIT licence.**
- [ ] **`/arkiv/schema.md`** in the repo: entity types, attributes, expiration per type, the queries the app runs.
- [ ] **On-chain evidence on Tiramisu:** entity keys and creation transaction hashes (or explorer links).
- [ ] **`/arkiv/friction.md`** in the repo.
- [ ] **Demo video**, 3 minutes or less.
- [ ] **Built between 9 and 18 October 2026.** The Arkiv integration and the core logic are new. Pre-existing work is disclosed with the baseline commit SHA and a list of reused components.
- [ ] **Evidence that survives expiry.** If entities expire before judging, the creation transaction hashes and the demo video are the evidence; judges check them on the explorer.

**Not eligible:** the SDK installed but never queried · a Postgres app with an Arkiv logo · private keys, secrets or personal data stored in Arkiv.

## 2. Score (100 points)

Four criteria, **25 points each**. Each is scored 0–5 and weighted: `points = 25 × (score / 5)`.

| Score | Meaning |
|---|---|
| 0 | Absent |
| 1 | A slogan with no substance |
| 2 | Gestured at, but generic |
| 3 | Solid and specific to this project |
| 4 | Good: thoughtful and clearly reasoned |
| 5 | Excellent: sharp, and could be handed to another builder as is |

### Why this pillar? · 25

The problem side. Who is harmed today if this data is censored, shut down, leaked or forged, and does the project actually help them?

| 1 | 3 | 5 |
|---|---|---|
| The pillar is a label; nobody concrete loses anything if the project does not exist | A real user with a real problem, and the pillar is why today's solution fails them | The pillar **is** the product: it names who is censored, exposed or misled today and what changes for them from day one |

What each pillar asks for:

- **Censorship Resistance:** someone outside the team can read and query the data from Arkiv without the team's backend.
- **Open Source:** another team can build on the dataset or tool without asking permission, from a documented data contract.
- **Privacy:** what is visible on the explorer exposes no personal data; few attributes, encrypted or hashed payloads, expiry the user controls.
- **Security:** the app shows or filters records by their on-chain author (`$creator`), not by a field anyone can write.

### Why Arkiv? · 25

The solution side. What breaks on a database an operator controls, on IPFS, a subgraph or your own API?

| 1 | 3 | 5 |
|---|---|---|
| "It's on-chain" is the whole argument | Names at least one property the project loses without Arkiv | The project falls apart without the Arkiv property it relies on, and it says what deliberately stays off Arkiv |

### How you use Arkiv · 25

**We judge how and why you use a feature, not how many you use.** We check usage on chain and in the code; a feature claimed but not found counts against you.

| Feature | Use that scores |
|---|---|
| Attributes vs payload | What you query lives in typed attributes (numbers where you need ranges); the rest in the payload |
| Queries | Compound predicates, ranges, `createdBy()` / `ownedBy()`, cursor pagination |
| Entity Expiration | Lifetimes that differ per entity type and follow product logic |
| Lifetime Extension | `extendEntity` as a lease renewed by activity |
| Creation flags | For example, permissionless extension so a community can keep data alive |
| `$creator` / `$owner` | Verifiable authorship surfaced in the UX; ownership transfer |
| WebSocket entity events | `watchEntityEvents` over a WebSocket transport (no `fromBlock`, which forces polling); the UI reacts without a refresh loop |
| Batch writes | Atomic batches when several writes must land together |

| 1 | 3 | 5 |
|---|---|---|
| A blob in the payload read by key, or features added for show | The features used are correct and tied to the product | Every feature used changes something the user sees, and the team explains why it chose it. One feature used this way can score 5 |

### Friction report · 25

`/arkiv/friction.md`: what got in your way while building with Arkiv.

| 1 | 3 | 5 |
|---|---|---|
| Praise, or "everything was great" | Real issues, or tested paths that worked, each with the surface involved | Each issue has expected vs actual, versions and steps to reproduce, and points at what would fix it. A smooth integration documented with the same rigour (what you tested, what you expected, what happened) scores the same. Invented complaints score 0 |

## 3. Ranking and prizes

- Each project's total is the average of the judges' totals, unrounded.
- **Minimum score:** 50/100 to win.
- **Allocation order:** Best Indian Team first, then each pillar. One prize per team and per individual; a winner is skipped and the prize goes to the next eligible team.
- **Pillar prizes:** the top-ranked project in each pillar.
- **Best Indian Team:** the top-ranked project overall from a team with at least one member of Indian nationality. If it also tops its pillar, it takes the $2,000 and the pillar prize goes to the next team in that pillar.
- **No eligible project for a prize:** it goes to the next-highest-ranked project overall that has not won.
- **Ties:** higher "Why Arkiv?" wins, then higher "How you use Arkiv", then the earlier submission timestamp.
- Judges with a personal or professional connection to a team disclose it and recuse themselves from that entry.
- Judges' decisions are final.
