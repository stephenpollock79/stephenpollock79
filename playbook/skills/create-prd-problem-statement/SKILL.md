---
name: create-prd-problem-statement
description: Drafts the problem half of a PRD (Sections 1–2 of prd-template.md) by reading the initiative's existing documents first, then asking one question at a time for whatever is still missing. Use when asked to "start a PRD", "draft the PRD problem section for X" or "create the problem statement for X". Run before prototyping; the companion create-prd-requirements skill fills Section 3 afterwards.
---

# Create PRD Problem Statement

Writes the **Why** half of a PRD: Section 1 (Key Information) and Section 2 (Problem Definition) of [prd-template.md](prd-template.md). It reads what already exists about the initiative first, so the questions it asks start from what is known rather than a blank page.

It only writes Sections 1 and 2, plus Section 4 (Open Questions). Section 3 (Requirements) is left as a heading for the companion skill, `create-prd-requirements`, which runs after a prototype exists.

Section 2 is not locked when this skill finishes. The prototype is new evidence, and the requirements pass may propose changes to Section 2 if the two disagree. Those changes are always confirmed with the user, never made silently.

## When to use

The user names an initiative and asks to start its PRD or draft its problem section. If no initiative is named, ask which one before doing anything else.

## Gather context first

Don't search everything. Work outward from the initiative.

1. **Find the initiative's own documents.** Ask the user where they live if it isn't obvious.
2. **Read what exists:** the idea or discovery brief, any validation or risk findings, competitor research, strategy notes. Don't assume any particular document exists; note what's missing rather than inventing it.
3. **Follow direct links one step out** for wider context, such as the parent strategy or a decision record.
4. **Ask the user for anything Sections 1–2 still need.** One question at a time, each with a suggested answer and your reasoning where you have one. Never a batch of questions at once.

## Write current fact only

Sections 1–2 state what is true now. No dates, no "revised", "decided", "confirmed" or "updated", no pointers to Section 4. If a fact changes during the session, write the new fact plainly and add a row to Section 4 recording the change. The *reason* behind a requirement, exclusion or constraint is not history and stays in the section.

## Section 1 · Key Information

- **1.1 Summary:** draft it, and mark it "Provisional, to be rewritten once Section 3 exists".
- **1.2 Stakeholders:** mark N/A on a solo project. Ask only if there genuinely are other stakeholders.

## Section 2 · Problem Definition

For each subsection, draft from what the documents actually say and note which document supports each claim. Where nothing supports a claim, ask rather than infer.

Use a two-column table for anything with more than one item (jobs, gains, pains, differentiators, exclusions, assumptions, constraints). Cut every word that doesn't add a fact or a reason.

| Subsection | What to write | Watch for |
|---|---|---|
| **2.1 Background** | Context, why now, competitors | Check competitors are current, not copied from an old scan. When a source lists concrete items, carry the full list. Say where the product's information or inputs come from, if the sources define it |
| **2.2 Objective** | Objective, who benefits, strategic fit, Key Results | Key Results need a date and a checkable condition, not a restated goal. Look for a stated success measure beyond delivery dates. Confirm any deadline or kill trigger with the user before stating it |
| **2.3 Value Proposition** | Jobs, gains, pains avoided, differentiators | Differentiators must hold up against the competitors in 2.1, not just the initiative's own claims |
| **2.4 Out of Scope** | What won't be built, and why | Usually not written down anywhere, so expect to ask. Don't turn positioning language into a feature exclusion without confirming. Don't imply deferred items will come back unless a decision point for that exists |
| **2.5 Assumptions and Constraints** | Assumptions table, constraints table | Check the sources for cost exposure, access control and operational limits. Carry forward any "must not use" or prohibited-source list as its own constraint |

## Section 4 · Open Questions

Fill it with real content using the template's table. Anything still unanswered, and any change made during the session, gets a row. Never leave it as a bare heading.

## Output

- Write into the initiative's PRD file.
- Leave Section 3 as a heading with one line: "Filled by the requirements pass, after prototyping."
- Put all citations in a **Sources** list at the bottom. None inline.

## Before you finish

- Every 2.x subsection is either backed by a cited source or holds an answer the user gave. Anything else is a Section 4 question.
- Read the draft back to the user section by section. Don't dump the whole document and take silence as agreement.
- **Scan for history.** Any date, change word or Section 4 reference in Sections 1–2 is a defect: move it to Section 4.
- **Scan for lists that should be tables.** Convert any multi-item list with detail per item.
- **Cut excess words,** but never an acceptance detail or a reason.
- **Read it as a stranger.** Could this be pasted into a different tool with no other context and still make sense? Fix anything that depends on a link or undefined jargon.
