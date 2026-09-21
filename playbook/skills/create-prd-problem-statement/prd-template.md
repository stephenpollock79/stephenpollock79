# PRD Template

A product requirements document in two parts: **Why** (the problem) and **What** (the requirements). **How** (technical design) belongs in a separate spec written by whoever builds it, and is deliberately left out of this template.

It is filled in two passes, with a prototype in between:

1. `create-prd-problem-statement` fills Sections 1–2 (the problem).
2. You design and prototype.
3. `create-prd-requirements` fills Section 3 (the requirements) from the prototype, and finalises the summary.

Section 4 (open questions) collects across both passes.

Sections marked **[skip for solo projects]** stay in the template so it holds up in a company with real stakeholders. On a one-person project, mark them N/A rather than forcing an answer.

## Authoring principles

These apply to every section, whichever pass is writing it.

- **Current fact only.** Sections 1–3 describe what is true now, in the present tense. No dates, no "revised", "decided", "confirmed" or "updated", no pointers to Section 4. If something changed, write the surviving fact plainly and record the change in Section 4. The *reason* a non-obvious choice was made is not history: keep it in the section where a reader needs it.
- **Fully self-contained.** Write as if the document will be pasted, alone, into a different tool with no other context (for example, an AI app builder). Define every project-specific term and piece of jargon the first time it appears. Never rely on the reader having followed a link. Cite sources only in a **Sources** list at the bottom.
- **Tables over bullets over prose.** Anything with more than one discrete item (benefits, assumptions, constraints, features, sources) goes in a two-column table: a short label and its detail, e.g. `| Assumption | Detail |`. Use a bulleted list only for a short list of bare phrases, and keep genuinely sequential explanation as prose or a numbered list.
- **Minimum words that still state the fact and its reason.** Cut restatement, hedging and filler. Never cut an acceptance detail or the reason behind a decision.
- **Flag contradictions, don't resolve them quietly.** When sources disagree, say so rather than picking the cleaner-sounding side.
- **Confirm high-consequence claims.** A hard deadline, a kill or pivot trigger, or any other binary commitment taken from a source document is checked with the product owner before it is written as fact. Source documents go stale.
- **Positioning isn't scope.** "We're not a stats dashboard" is a positioning statement, not automatically a feature exclusion. Confirm before converting one into the other.

---

## 1 · Key Information

### 1.1 Summary (2–3 sentences)

What is this document about? Drafted provisionally after Section 2; finalised only once Section 3 exists.

### 1.2 Stakeholders **[skip for solo projects]**

Name and role of key stakeholders.

## 2 · Problem Definition (Why)

### 2.1 Background

- What is this initiative about?
- Why now? What has changed?
- Which competitors or alternatives exist?

### 2.2 Objective

- What is the objective, and why does it matter?
- Who benefits, and how?
- How does it align with the wider strategy?
- Key Results: how will success be measured? Each one specific, measurable and dated.

### 2.3 Value Proposition

- Which customer jobs or needs does this address?
- What will customers gain?
- Which pains will they avoid?
- What does it do better than the alternatives?

### 2.4 Out of Scope

What this initiative will explicitly not do, and why.

### 2.5 Problem Assumptions and Constraints

The core customer and business assumptions and constraints.

## 3 · Requirements (What)

### 3.1 UX / Prototypes

Wireframes and user flows.

### 3.2 Key Features

For each customer job in 2.3: a happy path and unhappy paths, each with acceptance criteria.

- **Every feature has a priority:** Must / Should / Could / Nice to have, with a one-line reason. The point is build order: if time runs short, the lowest priorities are the ones already agreed to go first.
- **Non-functional requirements:** security, performance, scalability, accessibility, reliability.

### 3.3 Delivery Channel

Native mobile, desktop app, mobile web, desktop web, or other.

### 3.4 Solution Assumptions and Constraints

The core assumptions and constraints on the solution.

## 4 · Open Questions

A table, so answers can be added as they arrive. **This is the document's only decision log.** Every question, correction or change of direction anywhere in Sections 1–3 gets a row here, even if it was never asked as a question.

| # | Question | Owner | Blocking? | Status | Reply |
|---|---|---|---|---|---|
| 1 | … | … | Yes / No | Open | *(blank until answered)* |

- **Blocking?** and **Status** are separate. Blocking means the build is stuck without an answer. Status means whether it has been answered. Never infer one from the other.
- **Open means the product owner has something to decide.** If the direction is settled and the next step is someone else's, use a named status instead:

| Status | Meaning |
|---|---|
| Open | Needs a decision from the product owner |
| Resolved | Answered, and any affected section updated |
| Post MVP | Deliberately deferred beyond this release |
| Requires design update | Decided, but a screen or flow must change first |
| Requires design review | Not yet known whether design work is needed |
| Pending build | Decided; only a build or test step remains |

- **Never delete a row.** When a question is answered, update the affected section, fill the Reply and set the Status.
- **When the table gets long,** move Resolved and Post MVP rows by hand into a separate decision log document. From then on, row numbers are fixed and never reused, so references to them always resolve.
