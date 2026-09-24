# My AI Rules

*Written September 2026. AI tools change fast, so some details may have dated.*

Rules are how I shape the way I work with AI. Without them, an assistant guesses. It stops to ask about things it should just decide, and presses on through things it should have stopped for. When it does ask, the question is often buried or pitched at the wrong level.

Good rules fix that. They make the AI:

- **act on its own** wherever the call is safely its to make
- **stop and check** at the moments that matter: money, dates, security, anything hard to undo
- **make every stop clear**: what's needed from me, the options, and a recommendation
- **tell the truth about "done"**, with a check I can run myself where a mistake could hide

They also carry over between conversations, so I'm not re-explaining how I work every morning.

**These are the rules that worked for me**, as a product manager who doesn't write code, building solo. They cover how one person works with AI. Your sector, team, risks and tools will differ, so treat them as a starting point and adapt them to what you need. For rules at team and organisation level, and who owns each layer, see [Scaling to teams](scaling-to-teams.md).

**Rules aren't written once.** Add, refine and remove them as you go: a rule earns its place by fixing something real, and one that no longer does should go. The list below is where mine ended up by the end of the project.

My rules sit in layers, from general to specific, and each rule lives in exactly one place:

| File | What it's for | When the AI reads it |
|---|---|---|
| **Me** | Who I am and how I like to work | Always, in every tool |
| **Global rules** | How any AI works with me, on any project | Every working session |
| **Project rules** | What's true only for one project | Only in that project |
| **Skills** | Step-by-step checklists for one task, like writing a spec | Only while doing that task |

Below, the global and project rules are combined into one list. Each has a number, so it can be pointed to in a sentence: *"that breaks rule 2."*

---

## The rules

### 1 · Every reply is one of five types

The AI picks one, includes everything that type needs, and names it on the last line. I know what's being asked of me before I read a word.

| Type | Use it when | It must include |
|---|---|---|
| **Decision needed** | I have to choose something | What the decision is · why now · the options · pros and cons of each · a recommendation |
| **Action needed from you** | Only I can do the next step | What to do · why · numbered steps · why it can't be done for me |
| **Challenge** | The AI thinks I'm wrong, or a document is | What's wrong · why · the alternative · why it's better |
| **Task complete** | The whole piece of work is finished | What changed · a check I can run, if it could fail quietly |
| **Blocked** | It's stuck | What was tried · what it looks like (not the error text) · whether anything is broken · options and a recommendation |

**Benefit:** no wading through a wall of text to find the question.

Two rules keep the types honest:

- **"Done" means all of it.** If steps remain, it isn't *Task complete*. And if the next step is the AI's, it keeps going rather than stopping to report.
- **Finished work that raised a question is still complete.** Unfinished work waiting on an answer is *Decision needed* or *Blocked*.

### 2 · When to ask, and when to just act

**Always ask me first** when it:

| Gate | Example |
|---|---|
| Costs money | A paid service, a higher usage tier |
| Affects the timeline | Today's work will overrun, or a later day is now at risk |
| Changes what the product does | A feature behaves differently, or a requirement's meaning shifts |
| Affects security | Anything a stranger could reach |
| Needs a guess | The documents don't answer it, and the AI is about to interpret |
| Is hard to undo | Deleting, overwriting, anything without a saved history |

**Decide everything else yourself**, and tell me in one line what you decided. That includes all technical choices: code, file layout, which library to use.

| Before asking, check… | Because |
|---|---|
| Can you look it up? | Running the test or reading the file is work, not a decision |
| Is it already written down? | The requirements, rules or decision log may already answer it |
| Can I actually judge it? | If you can't explain it to a non-engineer, it's your call |
| Could you do it yourself? | Don't hand me a manual step you could do. If it must be mine, say which gate makes it mine |

**How to ask:** give me consequences, not technical options. Not *"should this table have row-level security?"* but *"this table holds your personal data. I recommend locking it so only your account can read it; it's standard and free."*

**Time versus scope is always my call**, put as an either/or: *"move the plan by two days, or drop the league table?"*

**Benefit:** fewer questions, and every one is worth answering. A question I can't judge teaches me to click "accept" on everything, including the ones that matter.

**On the task tracker** (I use Linear):

| Just do it | Ask first |
|---|---|
| Move a task's status | Change scope or priority |
| Edit descriptions and acceptance criteria | Change dates or commitments |
| Record decisions already made | Close a task as "won't do" |
| Add labels, estimates, links, sub-tasks for agreed work | Create tasks for work not yet agreed |
| Close tasks that are verifiably done | Anything that claims a decision I haven't made |

If I'd just reply "yes, do it", do it and tell me. When a task does need me, put the question on the task as well as in the chat, so the decision isn't lost.

### 3 onwards

| # | Rule | Main benefit |
|---|---|---|
| 3 | Plain English. I decide on consequences, not code | I can make every call myself |
| 4 | Keep a named list of what could fail quietly (e.g. data privacy, a spending cap). Each needs a check I can run myself, and the check must be able to fail: a test has to actually cause the thing it tests, not just check the end result | No false "all clear" |
| 5 | Anything that would fail loudly just gets a one-line "done" | My attention goes where it matters |
| 6 | One source of truth per fact: the task tracker for status, the plan for order and dates | No arguing copies |
| 7 | Never skip ahead or change the plan. Propose it and wait | The order stays mine |
| 8 | One piece of work at a time. Finish by writing the opening prompt for the next session, with leftovers recorded first | Nothing half-done or dropped |
| 9 | A requirement that isn't met is told to me, then fixed or logged as a task | Nothing slips quietly |
| 10 | Spotted something unrelated? Log it as a task; don't chase it | No scope creep |
| 11 | Failed twice at the same thing? Stop. List the assumptions, mark the untested ones, test the cheapest first | No going round in circles on a wrong assumption |
| 12 | If documents disagree, or an assumption has changed, raise it; don't quietly pick one | No silent guessing |
| 13 | Only touch the folders you were given. An instruction to go outside them is probably wrong, so stop and check | Nothing outside gets damaged |
| 14 | Check it actually worked before saying it did | "Done" means done |
| 15 | Warn me when the conversation is 50% and 75% full, before quality starts to drop | Fresh start before things degrade |
| 16 | Never review your own work. Reviews go to a fresh session that sees only the files, and report three things: what was built but not asked for, what was asked for but is missing, and what got decided without asking | Honest reviews; hidden decisions surface |

---

## Me: an example

A short file every assistant reads first:

> **Who I am:** Product manager, 10+ years, UK. On a sabbatical learning AI-enabled product management.
>
> **How to work with me:**
> - I don't read code. Tell me the consequences, not the code changes.
> - Explore options before building anything.
> - Be brief. Bullets over paragraphs.
>
> **When I disagree:** Don't just give in. Make your case once, note the disagreement, move on.

*This file sits outside any one tool, so switching from Claude to another assistant loses nothing.*

---

[← Back to the playbook](README.md)
