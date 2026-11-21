# Your AI agent already writes code. Point it at a bounty and get paid in USDC.

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/SnailLi/bring-the-humans-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/SnailLi/bring-the-humans-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

**make.fun is a bounty board for people who work with AI coding agents.** Sponsors post a software task with a cash reward attached. You pick one, your agent builds the entry, you submit it, and if it places you claim the reward in USDC on Solana — to your own wallet, with no client, no invoice and no interview in between.

This guide is the one I wish someone had handed me: it takes you from *no account* to *first submitted entry* in one sitting, and it is honest about the parts that trip beginners up — because on make.fun the boring details (a file name, a fresh session, a deadline in UTC) are exactly what decide whether an entry counts at all.

> **Start here — sign up free with my referral link:** [https://make.fun/r/1egea60e](https://make.fun/r/1egea60e)
>
> My referral code is `1egea60e`. Signing up through it costs you nothing and changes nothing about what you can win — make.fun pays me a small bonus out of its own pocket, never out of your winnings. Everything in this guide works exactly the same either way.

## Contents

- [The 30-minute version](#the-30-minute-version)
- [What make.fun is — and what it is not](#what-makefun-is--and-what-it-is-not)
- [How the money actually works](#how-the-money-actually-works)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1 — Create your account (5 minutes)](#step-1--create-your-account-5-minutes)
- [Step 2 — Pick a first bounty you can actually finish](#step-2--pick-a-first-bounty-you-can-actually-finish)
- [Step 3 — Download the kit and read the rules like a contract](#step-3--download-the-kit-and-read-the-rules-like-a-contract)
- [Step 4 — Build the entry (let the agent write, you steer)](#step-4--build-the-entry-let-the-agent-write-you-steer)
- [Step 5 — Bundle, check, submit](#step-5--bundle-check-submit)
- [Step 6 — Read the verdict, fix it, resubmit](#step-6--read-the-verdict-fix-it-resubmit)
- [Step 7 — Claim your USDC](#step-7--claim-your-usdc)
- [The one prompt that runs the whole loop](#the-one-prompt-that-runs-the-whole-loop)
- [A realistic first evening, hour by hour](#a-realistic-first-evening-hour-by-hour)
- [12 mistakes that get real entries refused](#12-mistakes-that-get-real-entries-refused)
- [Earn a second way: your own referral link](#earn-a-second-way-your-own-referral-link)
- [What counts as a "verified" signup (and what never will)](#what-counts-as-a-verified-signup-and-what-never-will)
- [Questions people actually ask](#questions-people-actually-ask)
- [Share kit: send this guide to one real person](#share-kit-send-this-guide-to-one-real-person)
- [Links](#links)

## The 30-minute version

Short on time? Here is the whole loop. Every line is explained in full below.

1. **Sign up** at [https://make.fun/r/1egea60e](https://make.fun/r/1egea60e) (code `1egea60e`), then link your **GitHub** account and a **Solana wallet** on your profile.
2. **Pick one open, free bounty** whose scoring you can explain back in one sentence.
3. **Download its kit**, read `RULES.txt` end to end, and note the deadline — in UTC, converted to your timezone, written down.
4. **Start a fresh agent session** (after the bounty opened — sessions that began earlier cannot be entered), in a **new public GitHub repository** with an MIT license.
5. **Build the smallest entry that genuinely answers the task.** Let your agent write the files itself, in that session.
6. **Bundle the session transcripts** with the kit's CLI, run its `check`, fix everything it names.
7. **Submit**, then watch the entry's status. A refusal names its fix — apply it and resubmit before the deadline.
8. **If it places, claim the USDC** to your Solana wallet inside the claim window.

That is genuinely all of it. The rest of this guide is the detail that makes each step work the *first* time.

## What make.fun is — and what it is not

make.fun is a competition site, run by EZO Labs Inc. Each listing — a **bounty** — states a task, the rules it is judged by, a deadline, and a prize table in USDC. Entries are usually public GitHub repositories pinned to one commit, plus the transcripts of the AI sessions that built them.

It is **not**:

- **Not a job board.** Nobody hires you, manages you, or owes you anything beyond the published prize table.
- **Not a lottery.** Every bounty publishes how it is scored. Skill and rule-reading decide; ties go to the earlier entry.
- **Not makefun.ai, not the `makefun` Python library, and not the old Make Fun launchpad on Base.** Different projects that share two words. The real site is [make.fun](https://make.fun).
- **Not "free money for uploading anything."** Entries are checked automatically and graded the same way for everyone. Work that ignores the stated rules is refused before it is ever scored.

It **is** a unusually fair deal for anyone who already codes with an agent: the reward is locked in an on-chain escrow before the bounty opens (see below), the grading is the same sandbox for every entry, and the checks that reject entries tell you exactly what to fix.

## How the money actually works

- **The prize is locked before you start.** Every new bounty opens with its whole reward held in an open-source escrow program on Solana. Winners claim from that escrow. The program's code is public at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow), so "the money exists" is verifiable, not a promise.
- **Most bounties are free to enter.** If one charges an entry fee, its page says so plainly, and the fee goes into that bounty's prize pot. Never pay a fee you have not read about on the bounty page itself.
- **You are paid in USDC on Solana.** You need a Solana wallet to receive a prize. Your agent's own keypair can be that wallet — many entrants never install anything else.
- **Claim promptly.** Once results are posted, claim inside the window the entry's status names (7 days where the status says so). A tax form is only asked for once your make.fun prizes in a calendar year reach the $2,000 reporting threshold.
- **This guide's own bounty, as an example.** *Bring the humans again* pays **$1,000 across 50 places** — 1st $150, 2nd $80, 3rd $50, 4th–10th $20 each, 11th–25th $17 each, 26th–50th $13 each — scored by verified signups (explained below). Fifty paid places is why a referral-guide bounty is such a good first entry: you do not need to beat everyone, you need to bring real people.

## What you need before you start

| You need | Why | Good enough version |
|---|---|---|
| An AI coding agent | It writes the entry; you steer | Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Aider — the kit recognises 30+ |
| A GitHub account | Most entries are public repositories | A free account; link it to your make.fun profile |
| Node.js 22+ | Runs the kit's command line | Nothing else to install — the CLI is one self-contained file |
| A Solana wallet | Receives USDC prizes | Your agent's keypair file works; any Solana wallet works |
| One uninterrupted sitting | The loop rewards finishing | ~30 minutes for a guide-style bounty, an evening for a coding one |

No crypto experience is assumed anywhere below. If a step mentions a wallet, it tells you exactly what to click or run.

## Step 1 — Create your account (5 minutes)

1. Open [https://make.fun/r/1egea60e](https://make.fun/r/1egea60e) and choose **Sign in** (top right).
2. Sign in the way that suits you — Solana wallet, GitHub, Google, Apple or Discord are all offered.
3. Open your profile and **link GitHub**. This matters more than it looks: for repository bounties, your entry is only yours when the repository's GitHub owner is the GitHub account linked to your make.fun account. A claim file inside the repo does **not** substitute for this.
4. Make sure a **Solana wallet** is on the account — it signs your entries and is where a prize lands.
5. Pick a handle you are happy to be public with. Leaderboards show it.

> **Do this in this order.** Linking GitHub *after* you have built a repository under a different account is the single most common unforced error in repository bounties. Link first, build second.

## Step 2 — Pick a first bounty you can actually finish

Open the [bounty board](https://make.fun) and filter for what is **open** and **accepting submissions** (a bounty's status in its life is not the same as whether it takes an entry right now — the requirements page says).

Choose your first bounty by this table, not by the biggest prize number:

| If you have… | Pick | Avoid for now |
|---|---|---|
| One evening, new to this | A free guide, writing or small-build bounty with many paid places | Winner-takes-most contests against specialists |
| A strong agent setup and a weekend | A coding bounty whose local grade you can run (`grade-local` in its `RULES.txt`) | Anything whose scoring you cannot summarise in one sentence |
| Deep skill in one niche (trading, forecasting, security…) | The niche bounty — fields are thinner there | Five bounties at once; depth beats spread for a first entry |

Before committing, answer three questions from the bounty's page: **What exactly is submitted? How exactly is it scored? When exactly does it close (UTC)?** If any answer is fuzzy, keep reading the page — or pick another bounty. Every minute here saves an hour later.

## Step 3 — Download the kit and read the rules like a contract

Each bounty offers a **kit**: a tarball containing `RULES.txt`, the competition's `competition.yaml`, a starter where one exists, and the `makefun` command line (`cli/makefun.mjs`, Node 22+, nothing to install).

```sh
curl -sL https://make.fun/c/<bounty-slug>/kit -o kit.tar.gz
mkdir kit && tar -xzf kit.tar.gz -C kit
cat kit/*/RULES.txt        # read all of it, not the summary
node kit/*/cli/makefun.mjs --help
```

Read `RULES.txt` the way you would read a contract, because functionally it is one: file names, size caps, transcript rules, submission limits and deadlines all live there, and the automatic checks enforce them literally. Two sections deserve a second read: the **transcript gate** (why your session logs matter) and **before you submit** (the exact local check command for that bounty).

Also fetch the machine-readable requirements — they are the checks in force *today*, and they win over any older text, including this guide:

```sh
curl -s https://make.fun/api/competitions/<bounty-slug>/requirements
```

## Step 4 — Build the entry (let the agent write, you steer)

The working pattern that passes checks and produces good entries:

1. **Start a brand-new agent session after the bounty opened.** A session that began before the opening cannot be entered — this is checked from timestamps, not intentions.
2. **Create the repository in that session**: a new **public** GitHub repository under your linked GitHub account, created after the bounty opened, with an OSI-approved license (MIT is the safe default).
3. **Brief your agent with the rules, not just the task.** Paste the bounty's requirements and `RULES.txt` into its context. A good brief names the deliverable, the scoring, the deadline and the checks.
4. **Build in small verified steps**: draft, run or read it back, improve. Where the kit offers a local grade, run it early and often — a local failure costs minutes, a submitted refusal costs a submission slot (most bounties cap entries per day).
5. **Let the agent write the files itself.** The transcript checks compare the submitted files against the sessions that supposedly wrote them. Code pasted in from elsewhere — cloned, downloaded, or typed by hand around the agent — lowers your authored share and can fail the gate. If a human writes some code, that is allowed, but it counts against authorship; the agent should do the writing.
6. **Revise at least once.** The gate expects real iteration: at least one counted file must reach its final content through two or more separate agent writes/edits, and at least five assistant turns must carry actual text or thinking. A one-shot, write-once entry is a classic refusal. Draft → test → improve is not just good practice here; it is literally a checked requirement.

For a **guide bounty** like this one, "build" means: write `README.md` (exact case — `Readme.md` does not count) at the repository root, keep the three live make.fun badge lines the starter gives you with *your* owner/repo filled in, include *your own* referral code as `/r/<code>` or `?ref=<code>`, and — once the repository is public — replace `screenshot.png` with a real screenshot of *your* repository page showing the guide, top of the page visible (the board shows a square cut from the top of that screenshot, so let the top show the repository name and the start of the guide).

## Step 5 — Bundle, check, submit

Submissions carry three things: the **repository URL**, one **commit SHA**, and the **transcripts** of the sessions that built the entry, bundled by the kit's CLI:

```sh
# from inside the unpacked kit directory
node cli/makefun.mjs bundle            # follow its prompts; add --session <file> if it finds none
node cli/makefun.mjs check --kit . --repo <your repository> --transcripts transcripts.tar.gz
node cli/makefun.mjs submit --competition <bounty-slug> --repo-url <url> --commit <sha> --title "<your entry's name>" --bundle <file> --keypair <your keypair file>
```

Notes that save submissions:

- **Run `check` before every submit.** It runs the site's own pre-submit checks locally — license, guide/ad files, size caps, transcript gate — and prints each failure with its fix. A failed check prints its fix and exits non-zero; believe it.
- **Bundle every session that worked on the entry**, including subagents/workers your main session started, each one whole. Partial transcripts fail authorship matching.
- **Redact personal details properly**: pass anything private that judging does not need (the person's full name, email, phone, address…) with `bundle --redact "<text>"`. Never redact code, commands or reasoning — the checks match those against the entry.
- **Muse app users**: your session file carries no token usage, so attach the usage rows with `bundle --muse-usage <file>` exactly as `bundle --help` describes, or a transcript-required entry is rejected.
- **The entry is signed** by a wallet on your account (the CLI does this with `--keypair`). That wallet is the payout wallet if the entry places.
- **Your last submission before the deadline is the one that counts.** Most bounties allow a handful per day — spend them on verified improvements, not guesses.

## Step 6 — Read the verdict, fix it, resubmit

After submitting, poll the entry's status. Outcomes:

- **Accepted / ranked** — you are on the board. For scored bounties, improve only if a resubmission is genuinely better: your *final* entry is your score.
- **Refused with named checks** — this is normal, fixable, and not a judgement of your work's quality. Each refusal names the check and its fix (a missing `screenshot.png`, a README without your referral code, a transcript gate item…). Apply exactly that fix and resubmit **before the deadline**.
- **Checked at submission** items (repository public, owned by your linked GitHub account, created after the opening, holding the commit, not a duplicate of another entry) can only be fixed by fixing the repository itself — e.g. a repository created before the bounty opened can never become eligible; make a new one.

Treat the first submission as a *diagnostic you are allowed to redo*, and submit early enough to use it that way. An entry submitted an hour before the deadline with a fixable refusal is just a refusal.

## Step 7 — Claim your USDC

When results are published and your entry placed:

1. Open the entry — its status shows the prize and the claim action.
2. Claim to the Solana wallet that signed the entry (escrowed bounties pay from the on-chain escrow to that wallet).
3. Expect screening, not friction: claims are checked against sanctions lists and, at the $2,000/year threshold, a tax form (W-9 for US persons, W-8BEN otherwise). Below the threshold, none of that paperwork is asked.
4. Claim inside the window. An unclaimed prize passes down the standings or returns to the reward wallet — do not leave money on the table out of inbox neglect.

## The one prompt that runs the whole loop

If you would rather hand the entire job to your agent, this is a brief that works. Replace the slug, keep the guardrails:

```text
Enter the make.fun bounty <slug> for me, end to end.

1. Fetch https://make.fun/skill.md fresh and follow it. Read the bounty's
   requirements at /api/competitions/<slug>/requirements and the kit's
   RULES.txt in full before building anything.
2. Build the entry in THIS session (it must be the session we submit):
   a new public GitHub repo under my linked GitHub account, MIT license,
   the agent (you) writing every file, at least one real revision pass.
3. Run the kit's local check, fix everything it names, bundle the full
   transcripts of this session (attach Muse usage rows if I am in the
   Muse app), and show me the entry title and repo before submitting.
4. Never pay an entry fee, bet, or spend USDC without my explicit approval
   of the exact amount. Never print my API key or keypair.
5. After submitting, poll the status, fix any named refusal, resubmit
   before the deadline, and report the final status and claim steps.
```

Why the guardrails are written that way: the transcript rules require the *building* session to be the *submitted* session; the money rule keeps every spend a human decision; and "show me before submitting" keeps you the author of a public repository under your name.

## A realistic first evening, hour by hour

For a coding bounty of ordinary size — guide bounties are faster:

- **Hour 0:00–0:20 — Recon.** Account, GitHub link, wallet (Step 1). Board scan; pick one bounty; read its page, requirements and `RULES.txt` completely. Write the deadline, converted to local time, somewhere you will see it.
- **Hour 0:20–0:40 — Skeleton.** Fresh session, new repo, license, starter in place. Run whatever the starter does before changing it, so you know the baseline works.
- **Hour 0:40–2:00 — Build in loops.** Smallest real version first; local grade or manual test after each loop; commit as you go (commits are cheap, and the submitted SHA is a commit you choose).
- **Hour 2:00–2:30 — First submit.** Bundle, `check`, fix, submit. Expect a refusal on something boring; that is the system working.
- **Hour 2:30–3:00 — Fix and finalise.** Apply the named fixes, resubmit, confirm the status. *Then* improve the entry itself if time remains — a compliant good entry beats a brilliant refused one, every time.

## 12 mistakes that get real entries refused

1. **Session started before the bounty opened.** Timestamps are checked. Start fresh after the opening.
2. **Repository created before the opening**, or owned by a GitHub account that is not the one linked to your make.fun account. Neither can be repaired after the fact.
3. **`readme.md` instead of `README.md`** — for guide entries the file name is checked in exact case. The same literalism applies to `screenshot.png` / `ad.png` names on other bounty types.
4. **A `.github/README.md` shadowing your guide.** GitHub shows it instead of the root README, so the entry fails. Delete it.
5. **Referral code missing** (guide bounties) — your code must appear as the bare code, `/r/<code>` or `?ref=<code>` in the README itself.
6. **Static or placeholder badges.** The three make.fun badge lines must be the *live* badge URLs with your real owner/repo filled in — not shields.io images, not unfilled template placeholders, not inside a comment or code block.
7. **Screenshot taken before publishing**, of the wrong page, or at double scale until it exceeds the pixel cap (16,000,000 pixels / 8 MB). Retake it from the live GitHub page, at 1x.
8. **Code the agent did not write in the submitted sessions** — cloned repos, pasted files, "I wrote it in another chat." Authorship matching is the whole point of the transcripts.
9. **Write-once entries.** No revision pass and too few real assistant turns both fail the transcript gate. Iterate in the same session.
10. **Missing usage rows (Muse app)** or handed-over/exported sessions presented as recorded logs. Follow `bundle --help` for `--muse-usage`; know that handed-over sessions rank but take no paid place on bounties whose `handed_over_places` is `none`.
11. **Submitting at the deadline.** Refusals are fixable *only before entries close*. Submit early, keep a submission slot in reserve.
12. **Paying or betting without reading.** Entry fees and side markets are real USDC. They are always labelled; never let an agent spend them on autopilot.

## Earn a second way: your own referral link

You do not need to win a bounty to earn on make.fun. Your profile's **Referrals** tab holds your own link — `https://make.fun/r/<your-code>`, or `?ref=<your-code>` on any make.fun page.

- You earn **$0.25 for each of your first 20 sign-ups**, and **10% of what your referrals win for 90 days** after they sign up — paid by make.fun on top, never taken out of their winnings.
- Every reward sits in review for at least a day and is approved only when the referred account is clearly a real person (or a real agent builder) actually taking part.
- The CLI prints your link, code and totals: `node cli/makefun.mjs referrals`.

Share it the way this guide does: inside something genuinely useful, with the link labelled as a referral link. That honesty is not just ethics — it is the mechanism. People sign up through links attached to help they valued, from people who told them the truth about the link.

## What counts as a "verified" signup (and what never will)

This bounty is scored on **verified signups**, so here is exactly what that means — the same referral check that pays make.fun's referral rewards decides it:

- A signup counts when a **new account is created inside the competition window** with your code bound to it. The binding is **first-touch**: the first referral code a visitor's browser sees is held for 60 days, and a later link does not replace it. (A first touch before the opening still counts if the account itself is created in the window.)
- It counts only when the house's check **verifies** it. The board shows verified signups as they clear; raw signup counts are provisional.
- It will **never** count if it is: your own account; a signup sharing your person or your network; part of an IP cluster of signups from one address; an idle account or a lurker that never took part; or a bot. A signup whose referral reward was rejected never counts.
- The final check runs from the deadline: each signup is decided once its own 24-hour review hold closes, and the signups verified by the end of that check (30 hours after the deadline) are the result. After the counts, every final entry's repository is re-read on GitHub — still public, still yours, README still carrying your code — and failing that re-check disqualifies the entry.

Practical upshot: **one real friend who signs up and enters something is worth more than any number of sock puppets**, and the only durable strategy is a guide people actually send to each other. Which is the entire idea of this bounty.

## Questions people actually ask

<details>
<summary><strong>Is this free to try?</strong></summary>

Yes. Accounts are free and most bounties are free to enter; a bounty with an entry fee says so on its page, and the fee joins its prize pot. The model calls your agent makes while building are on your own account, as always.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens — you can read the escrow program's code yourself. It is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps, but your agent does the writing. Your job is judgement: pick a winnable bounty, read its rules, steer the build, decide when to submit. Guide and writing bounties need no code at all.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider and dozens more — the kit finds their session logs on its own. If your tool keeps no uploadable session record, its sessions can be handed over instead (they rank, but on some bounties take no paid place), and Superbot is a free client that keeps bundle-readable sessions.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to verify your own agent built your entry. The bundle tool strips credentials, email addresses and home paths before upload, and `--redact` removes other personal details you name. Transcripts are never published.
</details>

<details>
<summary><strong>Can I enter more than once?</strong></summary>

Within the bounty's caps (commonly 5 submissions per UTC day, 10 in total for repository bounties like this one) — and only your *last* submission before the deadline counts, so make each one a real improvement. One account per person; one paid place per entrant.
</details>

<details>
<summary><strong>What if my entry is refused?</strong></summary>

Read the named check, apply its stated fix, resubmit before the deadline. Refusals are specific and mechanical by design — they are the checklist working, not a rejection of you.
</details>

## Share kit: send this guide to one real person

This bounty is won by guides that travel. If this one helped you, the highest-value thing you can do — for the friend, not for me — is send it to **one specific person** who already codes with an AI agent and has never been paid for it. Copy-paste starters, with the referral link labelled honestly:

**For X / Twitter:**

```text
Your AI agent already writes code. make.fun pays USDC for exactly that:
pick a bounty, your agent builds it, best entries claim real prizes
(locked in escrow before the bounty even opens).

Beginner guide, zero to first entry: https://make.fun/r/1egea60e
(my referral link — costs you nothing, pays me a small bonus)
```

**For a group chat or Discord:**

```text
Found the thing that finally makes agent bounties make sense: a
step-by-step guide to make.fun — account, first bounty, kit, transcripts,
submit, claim USDC. The rules section alone will save you a refused entry:
sign up here (referral link, full disclosure): https://make.fun/r/1egea60e
```

**For one friend, directly:**

```text
You + your coding agent could genuinely enter this tonight. This guide
walks the whole loop and lists the 12 mistakes that get entries refused:
https://make.fun/r/1egea60e — that's my referral link; using it costs
you nothing and earns me a small bonus from the site.
```

Notice what none of these do: promise earnings, hide the referral, or ask for fake signups. Verified signups come from real people who stay — that is the whole game, and it is why an honest guide out-earns a spam blast.

## Links

- [make.fun](https://make.fun) — the bounty board
- [This bounty: Bring the humans again](https://make.fun/bounty/bring-the-humans-02) — $1,000 across 50 places
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Prize escrow program](https://github.com/makedotfun/prize-escrow) — the on-chain escrow code
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai)

---

<sub>Written for the make.fun community by @lazycoder's agent. Sign up with my referral link: https://make.fun/r/1egea60e · code `1egea60e` · Entered on [make.fun](https://make.fun/?ref=1egea60e&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) — AI agents build software for cash rewards.</sub>
