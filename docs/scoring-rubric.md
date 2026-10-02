# Scoring rubric

Every submission is judged by the Arkiv team in two steps: **gates**, then **score**.

## 1. Gates (pass or fail)

A submission that fails any gate is not scored.

- [ ] **It works.** A public deployment judges can open without asking for access.
- [ ] **It can be reproduced.** The steps and the exact query in the submission produce what the submission says.
- [ ] **Public repo under the MIT licence.**
- [ ] **`/arkiv/schema.md`** in the repo: entity types, attributes, expiration per type, the queries the app runs.
- [ ] **On-chain evidence on Tiramisu:** entity keys and creation transaction hashes (or explorer links).
- [ ] **`/arkiv/friction.md`** in the repo.
- [ ] **Demo video**, 3 minutes or less.
- [ ] **Built between 9 and 18 October 2026.** Pre-existing code is disclosed; the Arkiv integration and the core logic are new.

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
| "It's on-chain" is the whole argument | Names at least one property the project loses without Arkiv | Without queryable, expiring, verifiable entities the project falls apart, and it says what deliberately stays off Arkiv |

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
| One blob in the payload, reads by key, the same expiry on everything | Two or three features used well and tied to the product | Every feature used changes something the user sees, and the team explains why it chose it |

### Friction report · 25

`/arkiv/friction.md`: what got in your way while building with Arkiv.

| 1 | 3 | 5 |
|---|---|---|
| Praise, or "everything was great" | Real issues, each with the surface involved | Each issue has expected vs actual, versions and steps to reproduce, and points at what would fix it |

## 3. Ranking and prizes

- Each project's total is the average of the judges' totals, unrounded.
- **Pillar prizes:** the top-ranked project in each pillar.
- **Best Indian Team:** the top-ranked project overall from a team with at least one member of Indian nationality. If it also tops its pillar, it takes the $2,000 and the pillar prize goes to the next team in that pillar.
- **Ties:** higher "Why Arkiv?" wins, then higher "How you use Arkiv"; if still tied, the panel decides by consensus.
- Judges with a personal or professional connection to a team disclose it and recuse themselves from that entry.
- Judges' decisions are final.
