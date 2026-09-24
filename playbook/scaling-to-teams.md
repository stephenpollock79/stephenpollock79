# Scaling to Teams and Organisations

*Written September 2026. AI tools change fast, so some details may have dated.*

The rest of this playbook was built by one product manager, working solo, who doesn't write code. This page covers what I'd change to use it in a team or across an organisation.

> **Recommendations, not results.** I haven't run this workflow with a team yet. These are the changes I'd make, based on what I learned building solo. Treat them as a starting point to test, not a proven method.

## The core ideas

**1. Make bets you can undo.** Nobody knows where AI tools will be in a year, so avoid choices that are hard to reverse:

- **Don't tie yourself to one AI provider.** Models and tools change fast, and today's leader may not be tomorrow's.
- **Keep rules, skills, context and workflows portable.** Store them as plain files your team owns, so they work with whichever tool you use next.
- **Don't throw out working tools on a hunch.** Replacing what people already use is hard to reverse (see [Tools](#tools)).

**2. Roles will overlap, and sometimes blend.** Solo, I was the product manager, designer, engineer and tester. With AI, a product manager can prototype, a designer can build, and an engineer can write requirements. The traditional roles (product manager, user researcher, analyst, designer, engineer, tester) won't disappear, but the lines between them will soften. My current take:

- **High-value or complex work:** the expert for each step still leads.
- **Everyday work:** get comfortable with anyone on the team, working with AI, taking it from design through to release.

Treat work as **high-value or complex** if any of these is true:

- It affects customers or money in a way that matters
- It would be hard to undo
- The team hasn't done anything like it before

**What never blends, whatever the work:**

- Code going to production is reviewed by an engineer
- Security, legal and regulatory sign-off stay with the experts

**3. Automation won't arrive evenly.** Coding has sped up a lot this year; other steps may not keep pace. That moves the bottleneck, either upstream to discovery and design, or downstream to code review and testing. Do teams then need more product managers and designers, or will AI speed those roles up just as much? Nobody knows yet. On my own project, most of my time went on the steps before coding. Rather than guess, watch where work waits, and rebalance roles and AI around it.

**4. Adoption never finishes.** Tools change monthly, so treat adoption as an ongoing product, not a one-off rollout: start with a pilot, measure it, give it an owner, and protect time for people to keep learning (see [Keeping up](#keeping-up) and [Rolling it out](#rolling-it-out)).

**On this page**

- [Workflow](#workflow)
- [Modes](#modes)
- [Tools](#tools)
- [AI rules](#ai-rules)
- [Skills](#skills)
- [Second brain and context management](#second-brain-and-context-management)
- [Keeping up](#keeping-up)
- [Rolling it out](#rolling-it-out)
- [Where this could go](#where-this-could-go)

---

## Workflow

*My solo version: [Project workflow](project-workflow.md).*

The last two columns are the team and organisation model. Which one applies depends on the work (see core idea 2).

| Step | Solo | High-value or complex work | Everyday work |
|---|---|---|---|
| **Strategy & objectives** | Me | Product lead, agreed with leadership | Product lead, agreed with leadership |
| **Ideation** | Me, with AI | Product manager, designer and engineering lead together | Product manager, with AI |
| **Discovery** | Me, with AI | Product manager and user researcher, backed by real user research | Product manager, with user research where it's needed |
| **Design** | Me, with an AI design tool | Designer leads; the product manager may prototype to show the designer the problem | Anyone, with AI, often the product manager prototyping |
| **Shaping** | Me, with AI | Product manager, with design and engineering reviewing the requirements | Whoever did the design, with AI |
| **Tech design** | AI proposed, I ruled on the consequences | Engineers own it; the product manager checks the impact on users | Anyone, with AI, reviewed by an engineer |
| **Planning** | Me | The whole team, with slices sized to its capacity | Whoever picks up the work |
| **Build loop** | AI built and reviewed, I tested | Engineers direct the coding agents, a human engineer reviews the code, and testers own test coverage | Anyone, with AI coding agents; an engineer reviews the code before it goes live |
| **Validate** | Me | Testers and security, released through the team's normal process | Whoever built it tests it; security checks are never skipped |

**Core recommendation:** keep the chain of artefacts, where each step's output feeds the next, and give every artefact a named human owner, whichever column the work is in.

## Modes

*My solo version: [modes in my project workflow](project-workflow.md#modes-of-working-with-ai).*

A reminder of the four modes:

| Mode | Who does the work | Who reviews it |
|---|---|---|
| **1 · Human only** | Human | Another human reviews and helps iterate |
| **2 · AI validation** | Human | AI reviews and helps iterate |
| **3 · Human validation** | AI | Human reviews and helps iterate |
| **4 · Autonomous AI** | AI | AI reviews and iterates on its own |

How they shift in a team:

| | High-value or complex work | Everyday work |
|---|---|---|
| **Usual modes** | Mostly 1 to 3 | Mostly 3, and 4 where the team has agreed it |
| **Who reviews** | The expert for that step | Anyone on the team, except for the things that never blend |

- **The safer the environment, the more AI can do on its own.** In test and staging environments, AI can run build, test and fix loops in mode 4. Anything going to production gets a human review.
- **Mode 1 comes back.** Solo, I never needed it. In a team, people working together on the hard problems is still where much of the value is.
- **Decide mode 4 as a team.** Agree in writing which work AI may do and check on its own. Start with a short list and grow it as trust builds.
- **Automation doesn't move accountability.** Mode 4 changes who does the work, not who answers for it. Every piece of work has one named human who owns the outcome, even when AI produced it and AI checked it. If nobody can say who that is, the work shouldn't be running in mode 4.

**Core recommendation:** make the mode for each type of work, and each environment, an explicit, written team decision, not something each person decides alone.

## Tools

*Related: [Best practices](best-practices.md), especially picking the right tool and keeping tools to a minimum.*

**Choose tools that support all four modes, not just AI.** My personal project needed no mode 1, so my tools were built for one person working with AI, such as a notes vault on my own computer. Teams work in more ways than that:

| How people work | Example |
|---|---|
| One person alone | Drafting a spec with AI |
| Two people together | Pairing on a design or a tricky bug |
| A group | A workshop or planning session |
| One person to many | A demo or a review with stakeholders |

- **One shared, largely cloud-based set of tools,** so people can see, edit and review the same work.
- **Agree the data rules first.** Security, legal and data teams decide what information can go into which tool.
- **Curate what AI reads.** Pointing AI at 100,000 wiki pages is expensive and noisy, and AI trusts whatever it finds. A small, well-organised set of plain files, such as markdown, works better for now.
- **Track the cost.** Small for one person; not for an organisation.

### The hardest balance: context for AI vs tools for people

The biggest open question I see discussed. AI works best with small, plain files; people work best in rich shared tools like wikis, trackers and whiteboards. Three options:

| Option | What goes wrong |
|---|---|
| Connect AI to every existing tool | Expensive, noisy, and poor results |
| Replace the existing tools with markdown files | Breaks how people work together, and is hard to reverse |
| **Keep the collaboration tools, and add a small curated layer AI can read** | **My recommendation for now.** Revisit it as the tools improve |

**Core recommendation:** pick tools that work for people working together as well as for AI, curate what AI reads, and settle the data rules before anything else.

## AI rules

*My solo version: [AI rules](ai-rules.md).*

Split the rules into three layers, each with its own owner:

| Layer | Owned by | Examples |
|---|---|---|
| **Organisation** | Leadership, security and legal | What data AI may see; what always needs a human check |
| **Team** | The team | How specs are written; when AI must stop and ask |
| **Personal** | Each person | Reply style; level of detail |

- **Keep them in one shared place,** as plain files, where changes are reviewed and a changelog records each one.
- **Keep refining them.** Add, change and remove rules in each retro, as I did solo.

**Core recommendation:** keep rules short and layered, stored in one shared place, and reviewed before they change.

## Skills

*My solo version: [Skills](skills/README.md).*

Run skills the way many companies run shared code: **anyone can suggest a change, and the owner reviews it before it goes in.**

- **A core library,** with a named owner for each skill.
- **Test before sharing.** A skill joins the core library only after someone other than its author has used it on real work.
- **Make your own version.** A person or team can copy a core skill and adapt it to their work, such as a PRD skill tuned for a regulated product.
- **Keep versions linked to the core.** Each version records which core skill it came from, picks up improvements to the core, and suggests its own improvements back. Otherwise versions drift apart and the library stops being shared.
- **Keep them portable.** Plain files that work across AI tools, not locked into one.
- **Retire what isn't used.**

**Core recommendation:** treat skills like internal products, with an owner, a review before release, room for teams to make their own versions, and retirement when nobody uses them.

## Second brain and context management

*My solo version: [Second brain](second-brain.md).*

AI is only as good as the context it's given. Solo, my notes vault was AI's memory. In a team, context needs the same three layers as the rules:

| Layer | What it holds | How it changes |
|---|---|---|
| **Organisation** | Strategy, policies, a glossary of terms | Anyone proposes; named owners review |
| **Team** | Decisions, customer research, product knowledge | Any team member proposes; another reviews |
| **Personal** | Your own notes, drafts and learning | You |

- **Context flows down, not up.** Personal context can draw on team and organisation context. Nothing personal moves into a shared layer unless someone chooses to add it.
- **Put shared context where the team already works,** and let AI read it.
- **Keep sensitive data out** of any layer AI can read unless the data rules allow it.
- **Keep it current.** Out-of-date context is worse than none, because AI will trust it.

**Core recommendation:** give every person a second brain, give teams and the organisation shared ones, and put controls on how the shared layers change.

## Keeping up

*Where I learned: [Training resources](training-resources.md).*

AI tools change monthly. Without a plan for learning and ownership, everything above goes stale.

- **Protected learning time for everyone who builds the product.** Many engineering teams already give around 10% of their time, a day a fortnight, to learning. Extend it to product, design and testing, and possibly company-wide. I took two months out to learn this; most people can't, so a day a fortnight is the realistic version.
- **Tie learning to real work.** Try a new tool or skill on a live task, then share what happened. Otherwise learning time drifts into watching videos.
- **A regular show-and-tell,** so what one person learns spreads to everyone.
- **A small team dedicated to AI adoption.** It owns training, rollout, the organisation layer of rules and context, the core skills library, and the measures.
- **Enable, don't gatekeep.** Pair the central team with an AI champion in each team, who spreads what works and feeds back what doesn't. A central team that approves everything becomes the next bottleneck.
- **Watch the market.** Someone trials new models and tools regularly. Portable rules, skills and context make switching cheap when something better arrives.

Protected time for everyone is a big investment, so treat it as a leadership decision and measure its return like any other.

**Core recommendation:** make learning part of the job, with protected time for everyone, and give adoption a dedicated team that enables rather than controls.

## Rolling it out

1. **Start small.** One willing team and one real piece of work, not an organisation-wide launch.
2. **Agree how you'll measure success, and when you'll check, before you start:**

   | Measure | What it tells you |
   |---|---|
   | Time from idea to release | Is it faster? |
   | Rework after review | Is quality holding up? |
   | Problems found after release | Is it safe? |
   | Where work waits | Which step has become the bottleneck? |
   | Team confidence, from a short survey | Do people want to keep going? |

3. **Hold regular retros,** and change the rules, skills, modes and tools based on what you learn.
4. **At the agreed checkpoint, decide:** expand, change or stop, based on the measures.
5. **Spread what works.** Train the next teams, and share rules, skills and context across them, led by the adoption team and champions (see [Keeping up](#keeping-up)).

**Core recommendation:** pilot, measure, then scale, the same way you'd launch any product.

## Where this could go

Agentic capability will keep growing, and more of this workflow will run as mode 4 — AI doing the work and checking it, with no human in the loop for longer stretches.

The limiting factor isn't what an agent can do. It's error detection. An agent that takes a wrong turn, drifts from the objective, or loops on a faulty assumption will keep going confidently, and the longer it runs unsupervised the more expensive that is to unwind. So the question isn't how much autonomy to give — it's what has to be in place before you can give it: guardrails that detect the failure, stop the run and escalate to a human. Cost ceilings. Checks against the original objective, not just the last instruction. Detection of loops and repeat failures.

Which puts the pressure somewhere specific for product managers. If an agent can run unsupervised for a week, the acceptance criteria are the only thing standing between that and a week of confident wrong work. Specification quality stops being a craft nicety and becomes the control mechanism.

Beyond that it's hard to predict, which is exactly why the bets you make today should be ones you can undo. Where I think the rest is heading:

- **Roles blend further.** More people will work across the whole process, with experts leading where the stakes are high.
- **The mix of roles shifts.** As each step speeds up at a different rate, the balance of product managers, designers, engineers and testers in a team will change. Which way it goes is still open.
- **Humans decide what to build and what to release.** Once a design is approved, AI could run spec, build, test and review on its own, all the way to a fully built test environment. People then come back in for two checks before anything goes live:
  - **A smoke test:** does it work the way users need?
  - **A code review:** even if it works, is it good code? Secure, able to scale, and easy to build on.

  This depends on strong automated tests, security checks and cost control being in place first. Even then, a named person still owns each release: the more of the work AI does, the more explicit that has to be.
- **Tools meet in the middle.** I expect the wiki, tracker and whiteboard tools to become more AI-friendly: a good surface for people to work together, with a format underneath that AI can read cheaply and well. When they do, the curated layer from [Tools](#tools) may no longer be needed.
- **Providers keep changing.** Teams whose rules, skills and context are portable will switch to the best tool easily. Teams locked into one provider won't.

---

[← Back to the playbook](README.md)
