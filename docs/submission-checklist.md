# Submission checklist

Everything happens on Devfolio, in two moments: when you **register** and when you **submit** your project. Questions marked * are required.

## 1. When you register (each person)

Devfolio asks for your name, email and GitHub, plus:

- Telegram handle (we use it to reach you during the challenge)
- Country of residence (statistics only, it does not affect eligibility)
- Does any team member hold Indian nationality? (to compete for Best CROPS (India) you need at least one; KYC for that prize is done with that person)
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

The standard fields: project name, tagline, description, technologies, your repo, a demo video of 3 minutes or less, and **tracks**: pick every CROPS pillar you compete in (Censorship Resistance, Open Source, Privacy, Security).

Then our questions. Answers marked Private are hidden from the public project page; only the Arkiv team and judges see them. Files in your public repo, including `/arkiv/friction.md`, stay public.

**Project**

1. Live app URL *
2. Does any team member hold Indian nationality? * (Private)

**Judging answers**

3. Why this pillar? * Write a short, labelled answer for each pillar you entered. Who is harmed today if this data is censored, shut down, leaked or forged?
4. Why Arkiv? * Why not Postgres, IPFS, a subgraph or your own API? What did you keep off Arkiv on purpose?
5. How do you use Arkiv? * For each feature you use, say how and why, and link to the relevant code.

**Verification on Tiramisu**

6. Wallet addresses that create your Arkiv entities, and the role of each *
7. Entity keys and creation transaction hashes, or explorer links *
8. Link to `/arkiv/schema.md` *
9. How can judges reproduce your Arkiv usage? * The steps and the exact query to run.
10. Pre-existing work * Anything made before the challenge that you reused, such as an earlier hackathon project, a fork or a template. Give the baseline commit SHA and what you reused, or write None.

**Feedback** (form answers are Private)

11. Link to `/arkiv/friction.md` *
12. Arkiv surfaces you used * (TypeScript SDK, direct JSON-RPC, WebSocket events, Docs, Hub, Faucet, Access keys, Block Explorer, Data Explorer, Arkiv MCP, Arkiv skills, Other)
13. If you selected Other, name it. Otherwise leave blank.
14. How long after you started did you write your first Arkiv entity? *
15. Which LLMs did you use? Write None if you did not use any. *
16. What is the one thing we should improve first? *
17. Are you open to a 20-minute feedback call with the Arkiv team? *

**Confirmations**

18. This is our team's work, built between 9 and 18 October. Any pre-existing or third-party work is disclosed. *
19. Our repo is public under the MIT licence and every link is accessible to judges. *
20. Optional: we plan to attend Devcon 8 in Mumbai and can showcase the project at the Arkiv booth. Not required to win.

Never paste private keys, seed phrases, access key secrets or RPC URLs with credentials into any answer.

## At the deadline

At the deadline we record your repo's commit SHA, and that is what we judge. A force-push that rewrites history after the deadline disqualifies the entry. Keep your deployment up until winners are announced on 23 October. You can edit your Devfolio submission until it closes.
