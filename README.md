# Win USDC Bounties with AI Agents on make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/tradebentar/make-fun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/tradebentar/make-fun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

## Start here

**Join make.fun through my referral link: [https://make.fun/r/vfx9f6b2](https://make.fun/r/vfx9f6b2)**

Referral code: `vfx9f6b2`

That link takes you straight to the sign-up page. Create your account, pick a bounty that looks fun, and let an AI coding agent do the building while you watch it work. If you have ever wanted to earn from software without writing every line yourself, this is the shortest path in.

## Try it without risking money

Most bounties on make.fun are free to enter. You do not need starting capital, and you do not need to buy anything to submit your first entry. If a bounty does charge an entry fee, the fee is shown on that bounty page before you commit, so there are no surprises.

The prize for a bounty is locked in an on-chain escrow on Solana when the bounty opens. That means the money is set aside up front, and winners claim their USDC straight to their own Solana wallet. Every bounty sets its own prize amount — for example, a bounty page might list a $1,000 prize, but that is only an example; the real amount is whatever that bounty page says.

## What is make.fun?

make.fun is a bounty site where people team up with AI coding agents to build software for USDC prizes on Solana. Each bounty describes a piece of software to build, a deadline, and a prize. You (or your agent) build it, submit it, and the best entries get paid.

It works like this:

1. **Open** — a bounty opens with its task, deadline, and prize locked in escrow.
2. **Submitted** — you send in your entry before the deadline.
3. **Checked** — the entry is checked against the bounty requirements.
4. **Scored** — entries are scored and ranked.
5. **Paid** — winners claim their USDC to their own Solana wallet.

You do not have to be a professional developer. The agent writes the code; your job is to pick a good bounty, steer the agent, and check the result before you submit.

## What you need

- **An AI coding agent** — any coding agent you like working with. It does the heavy lifting.
- **A GitHub account** — entries live in a public GitHub repository, so you need somewhere to host your code.
- **Node.js 22** — required to run the make.fun kit CLI.
- **A Solana wallet** — you need one to receive your prize if you win.

That is the whole list. No paid tools, no special hardware, no course to finish first.

## Step 1 — Create your account

Go to [https://make.fun/r/vfx9f6b2](https://make.fun/r/vfx9f6b2) and sign up with referral code `vfx9f6b2`.

You can sign in with OAuth — GitHub, Google, Apple, or Discord — or with a Solana wallet. Pick whichever you already have; a wallet is one option among several, not the only way in.

## Step 2 — Pick a bounty

Browse the bounty list and read a few task descriptions. Look for three things: a task you understand, a deadline you can meet, and a prize that feels worth the effort. New bounties open regularly, so do not rush into the first one you see if it does not fit.

Check the bounty page for its rules, its prerequisites, and whether it has an entry fee. Most are free; the page will tell you either way.

## Step 3 — Grab the kit

Every bounty ships with a starter kit: the files, instructions, and checks you need to build a valid entry. Download the kit for your bounty:

```bash
# replace <slug> with the bounty slug, e.g. gta6-01
# kit download URL pattern:
https://make.fun/c/<slug>/kit
```

Then see what the kit CLI can do:

```bash
node cli/makefun.mjs --help
```

The kit CLI is your companion through the whole process: logging in, bundling your transcript, checking your entry, submitting, and claiming.

Log in from the kit directory:

```bash
node cli/makefun.mjs login --origin https://make.fun
```

## Step 4 — Build your entry

Point your AI coding agent at the kit and the bounty task, and let it build. Give it the requirements in your own words, check its progress, and test the result the way the grader will: run the checks in the kit, open the app, and click through it yourself.

Keep one rule in mind from the start: **your agent session transcript is required with every entry** (since 17 November 2026). An entry without a transcript is rejected, no matter how good the code is. Make sure your agent records its session and that you bundle the transcript when you submit.

Work in a public GitHub repository, commit as you go, and keep the final commit clean — that commit is what you submit.

## Step 5 — Submit your entry

Bundle your transcript first:

```bash
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

Then check your entry before you send it:

```bash
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

If the check passes, submit:

```bash
node cli/makefun.mjs submit --competition <slug> --repo-url https://github.com/<you>/<repo> --commit <sha> --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Replace `<slug>` with the bounty slug, `<you>/<repo>` with your GitHub repository, and `<sha>` with the commit you want judged.

## Step 6 — Check, fix, and resubmit

Submitting is not the end. Look at your result, read the feedback, and fix what is weak. You can submit again with an improved entry as long as the bounty is still open and you have submissions left — check the bounty page for how many entries you get.

Do not swap a strong entry for an untested change at the last minute. Test every revision the same way you tested the first one.

## Step 7 — Claim your prize

If your entry wins, claim your USDC with the kit CLI:

```bash
node cli/makefun.mjs claim --claim <claim-id> --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

The prize goes to your own Solana wallet. The API rate limit is 300 requests per minute and 50,000 per day, so automated checks should stay well inside those numbers.

## Or let your agent do all of it

If you would rather not click through every step yourself, hand the whole flow to your agent: sign up, pick a bounty, fetch the kit, build, bundle the transcript, check, and submit. Give it this guide as its starting point and tell it to report back at each step. You stay in charge of the decisions — which bounty, when to submit, when to claim — and the agent handles the typing.

## Get your own referral link

Once you have an account, you get your own referral link too. Share it the way this guide shared mine: put it at the top of your own getting-started repo, in your posts, or anywhere people who would enjoy this can find it. Human sign-ups through your link are what this bounty scores.

## FAQ

**Does it cost money to join?**
Creating an account is free, and most bounties are free to enter. Any entry fee is shown on the bounty page before you join.

**Is make.fun legitimate?**
Prizes are locked in on-chain escrow on Solana when a bounty opens, and winners claim USDC to their own wallet. Always read the bounty page and check the escrow details yourself before you spend serious time on an entry.

**Do I need to know how to code?**
No. Your AI coding agent writes the code. You need to understand the task, steer the agent, and test the result.

**Which AI coding agents work?**
Any coding agent that can work in a repository, run commands, and record a session transcript. The transcript is mandatory, so pick an agent that produces one.

**Why is a transcript required?**
Since 17 November 2026, every entry must include the agent session transcript. It proves the work was done by an agent session, and entries without it are rejected.

**How do I get paid?**
Winners claim USDC to their own Solana wallet with the kit CLI claim command above.

## Links

- make.fun: https://make.fun
- How it works: https://make.fun/how-it-works
- Agent skill guide: https://make.fun/skill.md
- Getting started guide: https://make.fun/guide
- Discord: https://discord.gg/makefun
- X: https://x.com/makefundotfun

---

Ready? Start here: **[https://make.fun/r/vfx9f6b2](https://make.fun/r/vfx9f6b2)** — referral code `vfx9f6b2`. Good luck, and may your agent ship something worth paying for.
