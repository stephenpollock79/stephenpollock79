# Best Practices

*Written September 2026. AI tools change fast, so some details may have dated.*

What I'd recommend, and what I'd avoid, after a month of training and one solo build with AI. None of these came from reading alone; each was learned through a combination of theory and doing, and most by getting it wrong first. They aren't set-and-forget either. Like any way of working, they need revisiting as the tools and the work change.

These worked for me, a product manager who doesn't write code, building solo. Take them as a starting point and adapt them to your own work. For what changes once a team or a whole organisation works this way, see [Scaling to teams](scaling-to-teams.md).

---

## Recommended

| # | Practice | What it means | Benefit |
|---|---|---|---|
| 1 | **Set your AI rules early** · [my rules](ai-rules.md) | Write down when the AI should ask, when it should just act, and what a good question looks like. Said it twice? Write it down | The AI acts on its own where it safely can, and stops only when it matters |
| 2 | **Put each instruction in the right layer** | Always true about you, true for one project, or true for one task? Put each rule at that level and nowhere else | Rules apply where they should and don't leak everywhere else |
| 3 | **Give your AI a second brain** · [how](second-brain.md) | A notes vault the AI can read and write: your decisions, reasoning, and where things live | Every conversation starts from what you know, not from zero |
| 4 | **Keep it portable** | Store rules, notes and context as plain files you own, not inside one tool's settings | Switch tools or models and lose nothing |
| 5 | **Journal how you work with AI** | A short, dated note each day: what worked, what didn't, what annoyed you | You spot patterns you can't see day to day, and fix them |
| 6 | **Plan, then brief properly** | Before building, write what you want and how you'll know it works. Then brief each piece of work: what's decided, what's in scope, what the output should look like | The AI builds from a clear target instead of guessing, and gets it right in fewer rounds |
| 7 | **Pick the right tool for the task** | **LLMs** are good at language and judgement: understanding messy input, summarising, drafting, choosing what matters and explaining why. **Deterministic code** is good at anything that must give the same answer every time: calculations, scores, rules, validation. Let the LLM decide and explain; let code compute | Outputs you can trust, reproduce and check by hand |
| 8 | **Keep tools, skills and plugins to a minimum** | Every tool, skill or plugin adds setup, context the AI has to load, and something to maintain. Start with a few, learn them well, and add only when a real need appears | A setup you understand, that stays fast and cheap to run |
| 9 | **Adapt what you adopt** | Tools, skills and plugins from the internet are built for someone else's work. Treat them as a first draft: test them on your real tasks, then tailor them to fit | They work for your needs, not just in the demo |

---

## Avoid

| # | Avoid | What it means | Benefit of avoiding it |
|---|---|---|---|
| 1 | **Letting the same session mark its own homework** | The conversation that made something will defend it. Send reviews to a fresh session that sees only the files | Honest reviews that catch hidden decisions |
| 2 | **Letting AI try a third time when failing a task** | Failing twice isn't lack of effort; it's a wrong assumption. Stop and ask what it believes before it tries again | Problems fixed at the root, not patched over and over |
| 3 | **Context creep** | Rules, instructions, notes and documents pile up, because adding feels safer than removing. Past a point the AI can't hold it all, and starts ignoring what matters. Prune as often as you add | A lean context the AI actually follows |
| 4 | **Running a conversation to its limit** | Quality drops as a conversation fills up, with no warning. Start fresh with a short handover | Consistent quality from start to finish |
| 5 | **Over-relying on AI** | AI can build, test and review, but it can be confidently wrong. Keep a human in the loop, using the real thing, before any feature reaches a customer | Problems caught by you, not your users |

---

[← Back to the playbook](README.md)
