# Training Resources

*Written September 2026. AI tools change fast, so some details may have dated.*

The topics I'd learn to become an AI-enabled product manager, and the places I got the most value from while training.

> **Picked for my gaps, not yours.** I came into this with 10+ years of product management and a career in finance before that, but no engineering background. So I leaned hardest on how AI actually works and how software gets built, and lightest on product craft. Your experience and gaps will be different, so weight this list accordingly.

---

## Topics worth learning

The areas I'd cover to become an AI-enabled product manager, with one or two places to start on each.

| Topic | What it is | Why it matters | Start with |
|---|---|---|---|
| **1 · How LLMs work, and their limits** | What a language model is (a system trained to predict text) and where that breaks: making things up, forgetting, confident mistakes | You can't judge when to trust AI, or which mode to use, without knowing how it fails | [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) (Karpathy, 1 hr) · [AI Capabilities and Limitations](https://anthropic.skilljar.com/ai-capabilities-and-limitations) (Anthropic Academy) |
| **2 · Context management and second brains** | Deciding what the AI knows at each moment: rules, notes, documents and memory across sessions | The biggest lever on quality. Too little and AI guesses; too much and it loses the thread | [Effective context engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) (Anthropic) · [My second brain](second-brain.md) |
| **3 · What LLMs can do** | What today's tools can actually do: read files and images, search, use tools, run long tasks, and which model suits which job | Capabilities change monthly. Knowing the current limits stops you under-using AI, or trusting it with the wrong job | [How I Use LLMs](https://www.youtube.com/watch?v=EWvNQjAaOHw) (Karpathy, 2 hr) · [Claude 101](https://anthropic.skilljar.com/claude-101) (Anthropic Academy) |
| **4 · Prompting** | Writing clear instructions: context, examples and the output you want | Still the foundation every other technique builds on | [Prompt engineering overview](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview) · [Interactive tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial) (both Anthropic) |
| **5 · Skills** | Reusable instruction files that teach AI one task, done the same way every time | Turns your best way of doing a task into something repeatable and shareable | [Introduction to Agent Skills](https://anthropic.skilljar.com/introduction-to-agent-skills) (Anthropic Academy) · [My skills](skills/README.md) |
| **6 · Agents and connecting tools** | AI that works in a loop: plans, uses tools and checks its own work. MCP is the standard way to connect it to your apps and data | Where most AI-enabled PM work is heading: handing over whole tasks, not asking single questions | [Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) (Anthropic) · [What is MCP?](https://modelcontextprotocol.io/docs/getting-started/intro) |
| **7 · Evals and AI quality** | Testing AI output systematically: define what good looks like, study real failures, measure | Without evals, "it seems fine" is the only quality bar, and that bar isn't good enough for any AI feature | [Your AI Product Needs Evals: FAQ](https://hamel.dev/blog/posts/evals-faq/) (Hamel Husain) · [AI evals guide for PMs](https://www.productcompass.pm/p/ai-evals) (Product Compass) |
| **8 · AI efficiency** | The same result for less cost and time: the right model for the job, lean context, reusing work | Barely matters solo, but matters a lot across a team or an organisation | [Choosing the right model](https://platform.claude.com/docs/en/about-claude/models/choosing-a-model) · [Manage costs effectively](https://code.claude.com/docs/en/costs) (both Anthropic) |
| **9 · Building with coding agents** | Directing AI to build software with plans, specs and tests, rather than "vibe coding" | Product managers can now build real prototypes and apps. The discipline keeps what they build safe | [AI Hero](https://www.aihero.dev) (Matt Pocock) · [Claude Code 101](https://anthropic.skilljar.com/claude-code-101) (Anthropic Academy) |
| **10 · AI-enabled product management** | Bringing it all together: using AI across the whole product lifecycle, choosing how much to hand over at each step, and building AI into products | The topics above only pay off when they add up to a way of working | [My playbook](README.md), one worked example · [Product in the AI Era](https://www.svpg.com/ai-resource-guide/) (SVPG) |

---

## Where I learned

The people, channels and courses I got the most from, grouped by what they're good for.

## How AI and LLMs actually work

| Resource | Format | Why it was useful |
|---|---|---|
| [Andrej Karpathy](https://www.youtube.com/@AndrejKarpathy) | YouTube | The clearest explanation of what a large language model is and how it's built. Start with his intro talks; you don't need the maths to follow them |
| [Anthropic Academy](https://anthropic.skilljar.com) | Free courses | Structured, official courses on AI fluency, working with Claude, and tools like MCP. The backbone of my first month |
| [Dwarkesh Podcast](https://www.dwarkesh.com) | Podcast | Long, rigorous interviews with AI researchers. Where the field is heading, from the people building it |

## Keeping up with AI tools

| Resource | Format | Why it was useful |
|---|---|---|
| [Matt Wolfe](https://www.youtube.com/@mreflow) | YouTube | Weekly round-ups of new AI tools and news, pitched at non-engineers. His second-brain walkthrough shaped [mine](second-brain.md) |

## Building with AI

| Resource | Format | Why it was useful |
|---|---|---|
| [Matt Pocock / AI Hero](https://www.aihero.dev) | YouTube · site | Disciplined AI-assisted development: plan, spec, build, test, rather than "vibe coding". His [public skills](https://github.com/mattpocock/skills) were the starting point for my spec and ticket skills |
| [Greg Isenberg](https://www.youtube.com/@GregIsenberg) | YouTube | Practical walkthroughs of building AI products and small AI businesses. Good for seeing what's possible, fast |
| [Y Combinator](https://www.youtube.com/@ycombinator) | YouTube | Founder advice and Startup School, now heavily focused on building with AI. Sharp on what to build, not just how |

## Product management in the AI era

| Resource | Format | Why it was useful |
|---|---|---|
| [Lenny's Podcast](https://www.lennyspodcast.com) | Podcast · newsletter | The best single source for product, growth and leadership, with a growing focus on how AI is changing the PM role |
| [The Product Compass](https://www.productcompass.pm) | Newsletter | Paweł Huryn's frameworks and templates for AI-enabled PM work. Very practical |
| [Product School](https://productschool.com) | Podcast · YouTube · courses | Broad, accessible content on PM skills and careers, including AI product management |
| [The Beautiful Mess](https://cutlefish.substack.com) | Newsletter | John Cutler on how product teams and organisations actually work. A useful counterweight to tool hype |

---

[← Back to the playbook](README.md)
