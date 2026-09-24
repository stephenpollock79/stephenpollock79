# Second Brain and Context Management

*Written September 2026. AI tools change fast, so some details may have dated.*

A second brain is a notes vault that you and your AI share. You decide what goes in and ask the questions. The AI does the filing, summarising and linking. Over time it becomes the AI's long-term memory of your work.

This page is about one person's vault. Shared context for a team or an organisation needs its own layers and controls, covered in [Scaling to teams](scaling-to-teams.md).

## What it is

![How the second brain works: you capture sources and ask questions, the AI reads and writes a wiki inside a vault of plain files you own](images/second-brain.svg)

Three ideas, borrowed and combined:

| Idea | From | What it does here |
|---|---|---|
| **PARA** | [Tiago Forte](https://fortelabs.com/blog/para/) | Files your own notes by how actionable they are: **P**rojects, **A**reas, **R**esources, **A**rchives |
| **LLM Wiki** | [Andrej Karpathy](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) | You add sources; the AI writes and maintains a wiki of summaries and linked topic pages. It does the upkeep that most wikis decay without |
| **Grounded journal** | [Matt Wolfe](https://www.youtube.com/watch?v=yke4fLQUsh4) | A daily journal the AI answers from your own notes, not generic advice |

It's all plain markdown files in a folder, so any AI tool can read it and you're never locked in.

## Help the AI find its way

An AI can't hold a whole vault in its head at once, and shouldn't try: it's slow, expensive, and the important parts get lost. Give it a map instead, so it reads only what each task needs.

| Part | What it does |
|---|---|
| **An entry file** | A short file the AI reads first, at the top of the vault: what the vault is, how it's organised, and where to go next |
| **Task guides** | Where to look for each kind of task. For project work, start in that project's folder; to answer a question, start at the wiki index |
| **Index pages** | One per main folder, listing what's there with a one-line summary, so the AI can choose what to open |
| **Links between notes** | Related notes link to each other, so the AI follows a trail instead of searching everything |

## Why it's worth it

| Benefit | What it means |
|---|---|
| **The AI starts from what you know** | Decisions, reasoning and where things live are already written down. No re-explaining every session |
| **Knowledge compounds** | Every source you add gets linked to what's already there, so the vault gets more useful the more you use it |
| **You keep it, whatever the tool** | Plain files you own. Switch AI tools or models and nothing is lost |
| **Low effort to maintain** | The AI does the tedious part: summarising, cross-linking, tidying |

## Watch out for

| Issue | What to do |
|---|---|
| **Over-building** | It's tempting to keep adding folders, automations and rules. Start small and add only when something hurts |
| **Rubbish in, rubbish out** | Feed it strong, focused sources, not everything you've ever saved. Curate, don't dump |
| **Privacy** | The AI can read everything in the folders you connect. Keep passwords, keys and sensitive personal data out |
| **AI summaries can be wrong** | Keep the original sources untouched next to the summaries, so anything important can be checked |
| **Tool limits** | Some AI tools can't delete files, move them or run Git inside a connected folder. Find the limits early and work around them |

## How to set it up

1. **Install [Obsidian](https://obsidian.md)** (free) and create a vault. A vault is just a folder of markdown files.
2. **Add the PARA folders:** `Projects`, `Areas`, `Resources`, `Archives`.
3. **Add the wiki** inside `Resources`: a `raw` folder for sources (never edited) and a `wiki` folder the AI writes.
4. **Write an entry file** (`CLAUDE.md`, or `AGENTS.md` for other tools) that the AI reads first: how the vault is organised, where to look for each kind of task, and what it may and may not touch.
5. **Add an index page** to each main folder, and ask the AI to keep them up to date.
6. **Capture sources** with the [Obsidian Web Clipper](https://obsidian.md/clipper): articles, papers, video transcripts.
7. **Point your AI at the folder** and ask it to ingest what's new. It writes the summaries and links.
8. **Add a journal** (optional): a short daily entry the AI answers from your notes.
9. **Keep it tidy:** schedule regular ingests and a weekly health check, and back the vault up.

For the full build, start with [Karpathy's LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) and [Matt Wolfe's step-by-step video](https://www.youtube.com/watch?v=yke4fLQUsh4). I used Claude as the AI agent; the pattern works the same with other agents that can read and write files.

---

[← Back to the playbook](README.md)
