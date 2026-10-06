# Submission checklist

Everything happens on Devfolio, in two moments: when you **register** and when you **submit** your project. Questions marked * are required.

## 1. When you register (each person)

Devfolio asks for your name, email and GitHub, plus:

- Telegram handle (we use it to reach you during the challenge)
- Country of residence (statistics only, it does not affect eligibility)
- Does any team member hold Indian nationality? (to compete for Best Indian Use Case you need at least one; KYC for that prize is done with that person)
- Builder communities you are part of
- Background (Web2, Web3, both) and whether you had used Arkiv before
- How you heard about the challenge
- Optional: whether you plan to attend Devcon 8 in Mumbai (not required to win)
- **USDC payout wallet:** an EVM address. It can differ from the wallets your app uses.
- Acknowledgement that winners complete KYC before payout
- Consent to Arkiv and Devfolio using your contact details for this challenge

## 2. When you submit (once per team)

### In your repo

- [ ] Public, MIT licence, setup instructions in the README
- [ ] `/arkiv/schema.md`: entity types, attributes, expiration per type, the queries your app runs
- [ ] `/arkiv/friction.md`: for each Arkiv surface you used, expected vs actual, versions and steps to reproduce

### On the Devfolio project form

The standard fields: project name, tagline, description, technologies, your repo, a demo video of 3 minutes or less, and **tracks**: pick every track you compete in, a CROPS pillar (Censorship Resistance, Open Source, Privacy, Security) or Best Indian Use Case.

Then our questions. Your answers are private: only the Arkiv team and judges see them. Files in your repo, including `/arkiv/schema.md` and `/arkiv/friction.md`, are public.

**Project**

1. Live app URL *
2. Does any team member hold Indian nationality? *

**Judging answers** (each scored criterion is 25% of the total)

3. Which tracks are you entering? * The same tracks you picked on Devfolio.
4. Why this pillar? (25%) * For CROPS tracks. Who is harmed today if this data is censored, shut down, leaked or forged? Answer for each pillar you entered.
5. Why India? (25%) * For Best Indian Use Case. Who in India uses it, and what real problem does it solve for them?
6. Why Arkiv? (25%) * What would break on Postgres, IPFS, a subgraph or your own API? What did you keep off Arkiv on purpose?
7. How do you use Arkiv? (25%) * For each Arkiv feature you use: how, why, and a link to the code.
8. Friction report: link to `/arkiv/friction.md` (GitHub URL) (25%) * What you expected, what happened, versions and steps to reproduce.

**Verification on Tiramisu**

9. Wallet addresses that create your Arkiv entities, and the role of each * Judges find your entities and their creation transactions from these addresses.
10. Link to `/arkiv/schema.md` (GitHub URL) *
11. How can judges reproduce your Arkiv usage? * The steps and the exact query to run.
12. Pre-existing work you reused (or None) * Anything made before the challenge, such as an earlier hackathon project, a fork or a template, with its baseline commit SHA.

**Feedback**

13. Arkiv surfaces you used * (TypeScript SDK, direct JSON-RPC, WebSocket events, Docs, Hub, Faucet, Access keys, Block Explorer, Data Explorer, Arkiv MCP, Arkiv skills, Arkiv Plugin, Other)
14. If you selected Other, name it
15. How long after you started did you write your first Arkiv entity? * (2h or less, 2h to 24h, 1+ day)
16. Which LLMs did you use? (or None) *
17. What is the one thing we should improve first? *
18. Open to a 20-minute feedback call with the Arkiv team? *

**Confirmations**

19. This is our team's work, built between 9 and 18 October. Any pre-existing or third-party work is disclosed. *
20. Our repo is public under the MIT licence and every link is accessible to judges. *
21. We plan to attend Devcon 8 in Mumbai (optional, not required to win)

Never paste private keys, seed phrases, access key secrets or RPC URLs with credentials into any answer.

## At the deadline

At the deadline we record your repo's commit SHA, and that is what we judge. A force-push that rewrites history after the deadline disqualifies the entry. Keep your deployment up until winners are announced on 23 October. You can edit your Devfolio submission until it closes.
