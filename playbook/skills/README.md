# Skills

*Written September 2026. AI tools change fast, so some details may have dated.*

A skill is a reusable instruction file (a `SKILL.md`) that teaches an AI assistant how to do one task well, the same way every time.

Most of the skills I used were built by other people and lightly adapted for my setup, so rather than republish them, this page credits and links to the originals. The exception is my PRD pair, which I designed and refined heavily, and which is published here in full.

**Keep your skills outside any one AI app.** Store them as plain files on your own computer or in a repo, and point each tool at them. Then you can switch tools or models without losing them, and the same skill behaves the same everywhere.

**On this page**

- [My PRD skills](#my-prd-skills): the two skills I built, published in full
- [Skills from others I recommend](#skills-from-others-i-recommend): what they do, where I used them, and where to get them

---

## My PRD skills

I built these because my workflow puts a prototype between the problem and the requirements, and nothing I found online was built around that order.

Two skills that write a product requirements document in two passes, with a prototype in between:

```
Problem pass  →  Design & prototype  →  Requirements pass  →  (build spec, written separately)
  Why                                      What                   How
```

Requirements written from a real prototype are specific; written before one, they're guesses. So the PRD is split in two, and the prototype is treated as evidence that can correct the problem definition.

| | [Problem statement](create-prd-problem-statement/SKILL.md) | [Requirements](create-prd-requirements/SKILL.md) |
|---|---|---|
| **When** | Before any design work | After a prototype exists |
| **Inputs** | The initiative's existing documents (brief, research, strategy notes), then your answers to its questions | The PRD with its problem section written, plus a folder of design material in any format |
| **Writes** | Background, objective and key results, value proposition, out of scope, assumptions and constraints | UX and flows, features with priorities and acceptance criteria, non-functional requirements, delivery channel, and the final summary |
| **Asks you** | Anything the documents don't answer, one question at a time | Non-functional requirements, and a verdict on any contradiction between the design and the problem section |

**What makes them different from a standard PRD prompt:**

| Feature | Why it matters |
|---|---|
| **Reads before it asks** | Questions start from what's already known, not a blank page |
| **Current fact only, with one decision log** | The spec stays readable; every change and its reason lives in one table |
| **Self-contained output** | The PRD can be pasted into any tool, including an AI app builder, and still make sense |
| **One testable statement per acceptance criterion, each with a fixed ID** | Criteria can be cited by specs, tests and tickets, and each one passes or fails on its own |
| **At most five acceptance criteria per feature** | Keeps the PRD at product level and pushes implementation detail into the build spec |
| **Contradictions are logged, not fixed** | The design can challenge the problem definition, but you make the call |

Both skills share one [PRD template](create-prd-problem-statement/prd-template.md), kept in the problem-statement folder. Install the two together.

---

## Skills from others I recommend

| Skill | What it does | Where I used it | Source |
|---|---|---|---|
| **Pre-mortem panel** | Imagines the idea has failed and has several personas explain why | Ideation: stress-testing candidate ideas | [claude-premortem-skill](https://github.com/b1rdmania/claude-premortem-skill) |
| **grill-me** | Interviews you relentlessly to stress-test a plan or decision | Discovery and shaping: interrogating each half of the PRD | [Matt Pocock](https://github.com/mattpocock/skills) |
| **LLM Council** | Five advisors answer independently, review each other anonymously, then a chair gives a verdict | Pressure-testing big decisions | [claude-skills-llm-council](https://github.com/aiwithremy/claude-skills-llm-council), based on Andrej Karpathy's LLM Council |
| **to-spec / to-tickets** | Turns requirements into a build spec, then into tickets | The build loop, once per slice. I added a checklist: name the numbers, what else a change breaks, and what happens when inputs fail | [Matt Pocock](https://github.com/mattpocock/skills) |
| **webapp-testing** | Drives a running web app in a browser to test it | Testing each slice | [Anthropic](https://github.com/anthropics/skills) |
| **Wiki ingest, query and lint** | Maintains an AI-written wiki from sources you capture | My [second brain](../second-brain.md) | [Karpathy's LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) |
| **Grounded journal** | Saves a daily entry and answers it from your own notes | Daily reflection on how I worked with AI | [Matt Wolfe](https://www.youtube.com/watch?v=yke4fLQUsh4) |
| **teach** | Runs a multi-session course on any topic, tracking what you've learned | Learning new topics during training | [Matt Pocock](https://github.com/mattpocock/skills) |
| **last30days** | Researches what people have said about a topic in the last 30 days, across Reddit, X, YouTube and more | Research | [last30days-skill](https://github.com/mvanhorn/last30days-skill) |

As with the rest of this playbook: take these as a starting point and adapt them to your own work. Nothing found online fits perfectly out of the box.

---

[← Back to the playbook](../README.md)
