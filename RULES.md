# Official Rules & Terms

> [!NOTE]
> **Draft.** Frozen when the challenge opens on 9 October 2026. After that, only dated clarifications are added. Weights, gates, eligibility and prizes do not change after the opening.

## 1. Overview

The Arkiv × Devfolio Builder Challenge, India Edition ("Challenge") is organized by Golem Factory GmbH, doing business as "Arkiv Network" ("Organizer"), and distributed through Devfolio. By submitting an entry, participants agree to these rules in full.

This repository is the only canonical source of the rules. If any other surface (Devfolio page, posts, the event MCP) differs, this file applies.

## 2. Eligibility

- Open to individuals and teams worldwide. Fully online.
- Participants must be 18 or older at the time of submission.
- No purchase necessary.
- Employees of Arkiv / Golem Network and their immediate families are not eligible for prizes.
- Teams have up to 5 members. The roster is frozen when submissions close: members cannot be added or removed afterwards.
- Multiple submissions are allowed only if they are distinct projects. One prize per individual or team across all entries.

### Best Indian Team

A team qualifies for Best Indian Team if **at least one member holds Indian nationality**. Teams declare it on the submission form. If the team wins this prize, that member is the one who completes KYC and receives the prize, which verifies the nationality.

## 3. Challenge period

| Date | |
|---|---|
| 9 October 2026 | Opening, live at Network School Astana; submissions open |
| 18 October 2026, 23:59 IST (18:29 UTC) | Submissions close |
| 19–22 October 2026 | Judging |
| 23 October 2026 | Winners announced |
| 25 October 2026 | Deadline for winners to confirm Devcon attendance |
| 3–4 November 2026 | Winner demos at the Arkiv booth, Devcon 8, Mumbai |

Late submissions are not accepted. At the deadline we record each repo's commit SHA and judge that commit; rewriting history after the deadline disqualifies the entry. Deployments stay up until 23 October. The Organizer may adjust these dates; changes are announced on Devfolio and the Arkiv Discord.

## 4. Submission requirements

Submissions are made on Devfolio, the only valid method. The full list of fields is in [docs/submission-checklist.md](docs/submission-checklist.md).

Every submission must pass these gates to be scored:

| Requirement | Details |
|---|---|
| Working app | Public deployment, connected to the Tiramisu testnet, usable without asking for access |
| Reproducible | Steps and the exact query that produce what the submission claims |
| Public repo | MIT licence, setup instructions in the README |
| `/arkiv/schema.md` | Entity types, attributes, expiration per type, queries |
| On-chain evidence | Entity keys and creation transaction hashes on Tiramisu |
| `/arkiv/friction.md` | Feedback on building with Arkiv |
| Demo video | 3 minutes or less |
| One CROPS pillar | Censorship Resistance, Open Source, Privacy or Security |

### Valid submissions

- Use Arkiv as the primary data layer, through the official SDK (`@arkiv-network/sdk` 0.8.x) or direct RPC.
- Original work created between 9 and 18 October 2026. Libraries, frameworks and boilerplate are allowed; the Arkiv integration and the core logic must be new. Pre-existing work is disclosed in the submission with its baseline commit SHA and the components reused.
- AI coding assistants are allowed.

### Disqualified submissions

- Plagiarised work or code copied from another participant.
- No meaningful Arkiv use (the SDK installed but never queried, or a conventional database app with Arkiv branding).
- Private keys or secrets stored in Arkiv, or real personal data stored in plaintext or hashed form (hashes of emails or phone numbers can be reversed). Use synthetic data; encrypted payloads of test data are fine.
- Malicious code or intentionally introduced vulnerabilities.
- No working app, or submitted after the deadline.

## 5. Prizes

| Prize | Reward |
|---|---|
| Best Indian Team | Devcon 8 ticket + $2,000 USDC |
| Censorship Resistance | Devcon 8 ticket + $750 USDC |
| Open Source | Devcon 8 ticket + $750 USDC |
| Privacy | Devcon 8 ticket + $750 USDC |
| Security | Devcon 8 ticket + $750 USDC |

**Total: $5,000 USDC and five Devcon 8 tickets.**

### Prize conditions

- **Attending Devcon is required.** At least one member of each winning team demos the project at the Arkiv booth at Devcon 8 (Mumbai, 3–4 November 2026). The USDC prize is paid **after the demo**, within 14 days.
- **Travel time is short.** Winners are announced 11 days before the booth demos. If you need a visa for India, check the requirements before you enter; the Organizer can provide an invitation letter on request.
- **One ticket per winning team.** Travel, visa and accommodation are the winner's responsibility.
- **One prize per team and per individual.** Prizes are allocated in this order: Best Indian Team first, then each pillar. A team (or a person already in a winning team) that has won is skipped, and the prize goes to the next-ranked eligible team.
- **Minimum score.** A project needs at least 50/100 to win. If a prize has no eligible project (no qualifying team, no valid entry in a pillar, or nobody left who can attend), it goes to the next-highest-ranked project overall that has not won and can attend.
- **Currency:** USDC, sent to the EVM wallet address of the team member who completes KYC.
- **KYC is required to claim a prize, not to enter.** Only the team member who receives the prize completes it.
- Prizes are non-transferable, except as described in Section 6.
- Taxes are the winner's sole responsibility. The Organizer does not withhold taxes or give tax advice.

## 6. Confirmation and runner-up policy

1. Winners are notified by email and Telegram on 23 October.
2. Each winning team confirms by replying to the notification email within **48 hours** of it being sent that it will attend Devcon and demo at the booth. A replacement winner gets its own 48-hour window from its own notification.
3. If a team does not confirm, declines, or its prize recipient cannot complete KYC, the prize passes to the next-ranked eligible team:
   - a pillar prize goes to the next team in that pillar;
   - Best Indian Team goes to the next-ranked team with at least one member of Indian nationality;
   - if no eligible team remains, Section 5 (minimum score) applies.
4. Replacements are offered until 28 October 2026. After that, a prize that is declined stays unawarded.
5. If a winning team confirms but does not demo at Devcon, the USDC prize is not paid.

## 7. KYC and disbursement

One member of each winning team, the prize recipient, completes KYC before Devcon. For Best Indian Team, the recipient is the member of Indian nationality.

1. **Government-issued ID** (passport preferred; national ID both sides).
2. **Signed declaration form**, provided by the Organizer, signed by hand.
3. **Selfie holding the ID**, with face and ID readable.

The recipient confirms the EVM wallet address for the payout. KYC documents go to the Organizer's compliance office, are retained per its compliance requirements, and are not shared with third parties except as required by law.

## 8. Judging

The Arkiv team judges every submission against the published [scoring rubric](docs/scoring-rubric.md): gates first, then four criteria at 25 points each. Judges with a conflict of interest recuse themselves. Ties are broken as described in the rubric. Judges' decisions are final and not subject to appeal.

## 9. Intellectual property

- Participants keep full ownership of their submissions, which must be published under the MIT licence.
- By entering, participants grant the Organizer a non-exclusive, royalty-free, worldwide licence to showcase the submission, reference it as an example of Arkiv usage, and fork the repository for educational purposes.
- The public showcase (project name, one-liner, pillar) lists only teams that opt in on the form. Declining does not affect judging.

## 10. Code of conduct

Treat everyone with respect. No harassment, discrimination, sabotage of other teams, or illegal or harmful content in any Challenge channel. Violations may lead to disqualification at the Organizer's discretion.

## 11. Liability

- The Organizer is not responsible for technical failures, network issues or testnet downtime.
- The Organizer is not responsible for travel, visas, accommodation or any cost beyond the stated prizes.
- The Organizer may extend deadlines or cancel the Challenge if circumstances require, and may add dated clarifications. Changes never apply retroactively against a team, and are announced on Devfolio and the Arkiv Discord.
- The Organizer's total liability is limited to the stated prizes.

## 12. Privacy

- Personal data collected on the submission form is used only to run the Challenge.
- With the participant's consent on the form, contact details are shared between Arkiv and Devfolio for this Challenge.
- Participants are not added to marketing lists without explicit consent.

## 13. Governing law

These rules are governed by the laws of Switzerland. Disputes are resolved through good-faith negotiation.

## 14. Contact

Questions: the [Arkiv Discord](https://discord.gg/arkiv).
