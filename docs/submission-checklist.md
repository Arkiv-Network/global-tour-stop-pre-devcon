# Submission checklist

You submit on Devfolio. Besides the usual project fields, the form asks for the following. Prepare them before the deadline.

## In your repo

- [ ] Public, MIT licence, setup instructions in the README
- [ ] `/arkiv/schema.md`: entity types, attributes, expiration per type, the queries your app runs
- [ ] `/arkiv/friction.md`: for each Arkiv surface you used, expected vs actual, versions and steps to reproduce

## About you

- Telegram handle (we use it to reach you during the challenge)
- Country of residence (statistics only, it does not affect eligibility)
- Does any team member hold Indian nationality? (decides eligibility for Best Indian Team; if you win it, that member completes KYC and receives the prize)
- Builder communities you are part of
- Background (Web2, Web3, both) and whether you had used Arkiv before
- How you heard about the challenge

## Prize requirements

- **Devcon attendance (required to receive a prize):** if you win, will at least one team member attend Devcon 8 in Mumbai and demo at the Arkiv booth on 3–4 November? Prizes are paid only after the demo. If a winner cannot attend, the prize passes to the next-ranked team that can.
- **USDC payout wallet:** an EVM address. It can differ from the wallets your app uses.
- Acknowledgement that the team member who receives the prize completes KYC before payout.

## Your project

- CROPS pillar (one)
- Live app URL (libraries, CLIs and datasets too: a deployed app or product that shows how it is used)
- **Why [pillar]?** Who is harmed today if this data is censored, shut down, leaked or forged?
- **Why Arkiv?** Why not Postgres, IPFS, a subgraph or your own API? What would break, and what did you keep off Arkiv on purpose?
- **How do you use Arkiv?** For each feature, how and why, with a link to the line of code.
- Demo video, 3 minutes or less

## Verify your Arkiv integration (Tiramisu)

Never include private keys, seed phrases, access keys or RPC URLs with credentials.

- Wallets that create your entities, and the role of each (for verification, not payout)
- Entity keys and creation transaction hashes, or explorer links
- Link to `/arkiv/schema.md`
- How judges reproduce your Arkiv usage: steps and the exact query to run
- Pre-existing work, if any: the baseline commit SHA and the components you reused

## Your feedback

- Link to `/arkiv/friction.md`
- Arkiv surfaces you used
- How long it took to write your first entity
- LLMs you used, and whether you used the Arkiv MCP or skills
- Optional: the one thing we should improve first, whether you will keep building, whether you are open to a 20-minute feedback call

## Confirmations

- This is our team's work, built between 9 and 18 October; pre-existing or third-party work is disclosed.
- The repo is public under the MIT licence and every link is accessible to judges.
- We consent to Arkiv and Devfolio using our contact details for this challenge.
- Optional: list us in the public showcase (project name, one-liner, pillar). Declining does not affect judging.

At the deadline we record your repo's commit SHA, and that is what we judge. A force-push that rewrites history after the deadline disqualifies the entry. Keep your deployment up until winners are announced on 23 October. You can edit your Devfolio submission until it closes.
