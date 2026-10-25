# Stephen Pollock

**Principal / Lead Product Manager** · most recently Director of Product Management at FanDuel · 10+ years in product · Edinburgh, UK · [LinkedIn](https://www.linkedin.com/in/stephen-pollock-1a67a187)

Since August 2026 I've been on a self-directed sabbatical to become an AI-enabled product manager. This page is what I built and what I learned.

<details>
<summary><b>Career highlights and the sabbatical</b></summary>

<br>

- **FanDuel Predicts (2025–26):** led promotions from 0-1 build to launch: 50k monthly active users within six months, promotional opt-in up from 5% to 30%, a team of 7 PMs.
- **FanDuel Martech (2022–25):** led a multi-year, AI-enabled transformation of the promotions platform across 4 dev teams: 10× personalisation, 50% faster time to market, 500+ hours a week saved.
- **Avaloq (2016–21):** Senior PM through to Head of Product. Grew a mature B2B portfolio management product used by 60+ banks — 25% more customers, 30% more revenue — then took the new cloud wealth platform (6 teams, 60 staff, £8m budget) from 0-1 to its first two live customers.

**The sabbatical.** The goal: use AI across the whole product lifecycle, from problem framing and discovery to build and test, and learn where it can be trusted and where it needs checking. It ran in three phases:

1. **Theory.** A month of structured training in AI tooling and LLM fundamentals, including the Anthropic Academy courses ([training resources](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/training-resources.md)).
2. **Practice.** Building real applications end to end, solo (see [Pet Projects](#pet-projects)).
3. **Playbook.** Writing up what I learned as a [playbook](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/README.md), including how I'd scale it to [teams and organisations](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/scaling-to-teams.md).

</details>

## Pet Projects

### Next Role

A job-search app that runs in your own Claude account: it finds roles, screens them against your preferences, researches them, drafts tailored CVs and cover letters, and preps your interviews. Built in about three weeks, part time, and used every day for my own job search; anyone can install their own copy. **[Try the demo and read more →](https://github.com/stephenpollock79/next-role)**

<details>
<summary><b>Process, scale, tools and cost</b></summary>

<br>

I directed the build rather than hand-writing the code.

| | |
|---|---|
| **Process** | Built by dogfooding: used daily for my own search, with bugs fixed and features added as I hit them → personal details moved out of the code → a guided setup wizard, a public demo and an install guide → tested end to end on a brand-new account |
| **Scale** | About 18,000 lines of JavaScript in 52 files · 11 Claude skills · 600+ published versions · about 560 automated checks |
| **Tools** | Claude (artifacts, skills, scheduled tasks, Claude in Chrome) · Gmail · GitHub · Playwright |
| **Cost** | No hosting, database or API costs: it runs entirely inside a Claude subscription |

More on how it was built: **[How I built it](https://github.com/stephenpollock79/next-role#how-i-built-it)**.

</details>

### The Gaffer

A decision-support app for Fantasy Premier League, built solo in under three weeks from problem brief to a deployed web app with authentication and a database. **[Watch the demo and read more →](https://github.com/stephenpollock79/fpl-advisor#the-gaffer)**

<details>
<summary><b>Process, scale, tools and cost</b></summary>

<br>

I directed the build rather than hand-writing the code.

| | |
|---|---|
| **Process** | Problem brief → clickable prototype and design system → PRD and architecture decision records → sliced tickets → build and test → deployed app |
| **Scale** | 11-screen clickable prototype in about two days · 12 build slices, each reviewed by a fresh AI session before it was called done |
| **Tools** | Claude (Code, Cowork, Design) · Obsidian · Linear · GitHub · Railway · Supabase |
| **Cost** | About $30 for a month of hosting, database and tracker, plus a Claude subscription. Under $3 of Claude API usage across the whole build, on top of the subscription |

How each phase worked, which mode of working with AI I used, and what I'd change: **[My project workflow](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/project-workflow.md)**.

</details>

## AI-Enabled Product Management

There's no one-size-fits-all way to work with AI, so I built my own playbook around one question asked at every step: who does the work, and who checks it.

<details>
<summary><b>The thinking and the four modes</b></summary>

<br>

> "AI can generate PRDs, interfaces, prototypes, and code, but it does not replace the judgment required to determine which problems are worth solving or which solutions are valuable, usable, feasible, and viable."
>
> — Silicon Valley Product Group, *Product in the AI Era: AI Resource Guide*, 2026

How we work has always depended on context: sector, product maturity, whether it's B2B, B2C or an internal platform, regulatory constraints and more. Add AI and its rate of change, and it becomes essential for every product manager to learn, experiment and iterate their way to the approach that works for them.

So I built a playbook from my own experience: how I worked end to end as a solo product manager on a real build, as at September 2026. It's about AI-enabled ways of working. For the other side, AI inside a product, see [The Gaffer](https://github.com/stephenpollock79/fpl-advisor#the-gaffer), where AI is the reasoning layer behind every recommendation.

**Four modes of working with AI**

| Mode | Who does the work | Who reviews it |
|:---|:---|:---|
| **1 · Human only** | Human | Another human reviews and helps iterate |
| **2 · AI validation** | Human | AI reviews and helps iterate |
| **3 · Human validation** | AI | Human reviews and helps iterate |
| **4 · Autonomous AI** | AI | AI reviews and iterates on its own |

The right mode depends on the stakes. The more a mistake costs, or the longer it would go unnoticed, the more a human belongs in the loop. Over time, more tasks will move down this list — and what decides how fast is error detection, not raw capability: see [where this could go](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/scaling-to-teams.md#where-this-could-go).

I've also documented how I'd scale it. [Scaling to teams and organisations](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/scaling-to-teams.md) revisits each part of the playbook and says what changes when a team, and then a whole organisation, works this way: who owns what, who stays accountable when AI does the work and AI checks it, and how I'd roll it out.

</details>

## Go Deeper

| Page | What's in it |
|---|---|
| **[Project workflow](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/project-workflow.md)** | Idea to deployed app, solo: each step and which AI mode I used |
| **[Best practices](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/best-practices.md)** | Fourteen recommendations from my own use, including what to avoid |
| **[AI rules](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/ai-rules.md)** | When AI acts alone, when it stops and asks, and how it explains |
| **[Skills](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/skills/README.md)** | Skills I use from others, plus the PRD pair I built, in full |
| **[Second brain](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/second-brain.md)** | A notes vault that gives AI memory of what you already know |
| **[Scaling to teams and organisations](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/scaling-to-teams.md)** | Ownership, accountability, tools and rollout beyond one PM |
| **[Training resources](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/training-resources.md)** | What's worth learning as an AI-enabled PM, and where I learned it |

All of it in one place: **[the full playbook](https://github.com/stephenpollock79/stephenpollock79/blob/main/playbook/README.md)**.
