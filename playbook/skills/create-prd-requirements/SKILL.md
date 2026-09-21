---
name: create-prd-requirements
description: Drafts the requirements half of a PRD (Section 3 of prd-template.md) from the finished problem section plus a folder of design material, then finalises the summary. Logs any contradiction between the design and the problem section for the user to rule on. Use when asked to "draft the PRD requirements for X" or "fill in the requirements section for X", after create-prd-problem-statement has run and a prototype exists.
---

# Create PRD Requirements

Writes the **What** half of a PRD: Section 3 (Requirements) of the template in the `create-prd-problem-statement` skill folder. Install the two skills together.

It runs after prototyping on purpose. Requirements written from a real prototype are specific; requirements written without one are guesses. The design material is treated as evidence. Where it contradicts the problem section, the contradiction is logged for the user to rule on, never quietly fixed.

This skill writes Section 3, finalises 1.1 Summary, updates Section 4, and changes Sections 1–2 only when the user confirms. It never writes technical design: that belongs in a separate spec.

## Inputs

Exactly two:

| Input | What it is |
|---|---|
| **The PRD** | The initiative's PRD, with Section 2 already written |
| **A design folder** | Anything describing the solution: prototype exports, screen flows, written notes, sketches, in any format |

If either isn't named, suggest the most likely candidate and ask the user to confirm. Don't guess silently, and don't ask an open-ended question. If Section 2 isn't written yet, say so and stop: there is nothing to check against.

## Gather context first

1. **Read the PRD in full:** Section 2 to check against, Section 4 for what's already open, and the Sources list for what has already been read.
2. **Read every file in the design folder,** whatever its format. Actually open and decode each one; don't describe a screen from markup you haven't rendered or read.
3. **Follow direct links one step out** for wider context.
4. **Ask about non-functional requirements before drafting features:** security, performance, scalability, accessibility, reliability. They rarely appear in a prototype and are the user's call. One at a time, with a suggested default. Never infer them, and never skip the category.

## Write current fact only

Sections 1–3 state what is true now. This pass is the most tempting place to write "revised" into the text, because it edits Sections 1–2 and drafts from new evidence. Don't: write the surviving fact and record the change in Section 4. Reasons behind a requirement stay in the text.

## Section 3 · Requirements

Use two-column tables for anything with more than one item. Define any term carried over from the design material the first time it appears.

### 3.1 UX / Prototypes

Walk through the design material in the order it's used, and describe the flow. Refer to screens by the names a reader would recognise, not file numbers.

### 3.2 Key Features

For each customer job in Section 2.3, write one feature grounded in the screens that serve it. Each feature gets one `| Section | Detail |` table holding:

- **Priority:** Must / Should / Could / Nice to have, with a one-line reason. Judge it on how closely it serves the core jobs, how central it is to launch, and how separable it is. Don't default everything to Must. Say it's a first-pass rating the user may change.
- **Serves:** which 2.3 job it delivers.
- **Happy path.**
- Bold divider rows, `| **Acceptance Criteria** | |` and `| **Unhappy Paths** | |`, with the criteria underneath.

**Every criterion has an identifier and says one thing.** Format: `<feature>-<kind>-<nn>`, numbered from 01 within each feature and kind. `AC` for acceptance criteria, `UP` for unhappy paths, and any other two-letter code a feature needs.

- **One statement per row.** If a row joins two separately checkable claims with "and", it is two rows. This is what makes the identifiers useful: each names one fact that can pass or fail on its own.
- **Identifiers never change.** They are cited from specs, tests, tickets and other criteria. A deleted criterion retires its number; the others are never renumbered.

> ✗ `| | The header shows the order total, the delivery date and a Change button that opens the address form. |`
>
> ✓ `| **F1-AC-01** | The header shows the order total. |`
> `| **F1-AC-02** | The header shows the delivery date. |`
> `| **F1-AC-03** | A Change button in the header opens the address form. |`

**At most five acceptance criteria per feature, all at product level.** A PRD criterion says when the product decision is met: several engineers could build it different ways and all be right. Layout, copy, gestures, colour and rendering detail belong in the build spec, which cites the PRD criterion by its identifier. Test each row: *could this be built several valid ways?* Keep it. *Does it only remove implementation ambiguity?* Move it to the spec. Fix an overrun by moving spec-level rows out, never by merging two criteria into one. A feature that genuinely needs more than five is named in the final report, with the reason. Unhappy paths aren't capped. Without a counted limit, criteria balloon into spec detail and swamp the document.

State the identifier scheme once at the top of Section 3, so readers know how to use it.

**Match jobs and features both ways.** A 2.3 job with no feature, or a feature serving no 2.3 job, becomes a Section 4 question and appears in the final report. Don't invent a feature to fill the gap, and don't drop it silently.

Then add a `| Requirement | Detail |` table for the non-functional requirements, using only the user's answers.

### 3.3 Delivery Channel

Usually already decided elsewhere. Check the initiative's decisions, state it with its source, and ask only if it's genuinely open.

### 3.4 Solution Assumptions and Constraints

Taken from the design material and context documents, in separate assumptions and constraints tables. Ask for anything not grounded in either.

## Check Section 2 against the design

The prototype exists precisely to test the problem definition, so compare every document in the design folder with Section 2's claims.

- **Adds detail without contradicting anything:** leave Section 2 alone. The detail belongs in Section 3.
- **Genuinely contradicts Section 2:** log it in a temporary **Document Inconsistencies** table at the bottom of the PRD: `# | Inconsistency | Evidence | Suggested resolution | Verdict`. Evidence must be locatable: a document name plus a page, screen or line. Leave Verdict for the user.
- **Once the user gives a verdict:** apply only the confirmed changes to Section 2, then remove those rows. Remove the whole table when it's empty. Skip it entirely if nothing contradicts.

Once Section 3 is written and any confirmed changes applied, **rewrite 1.1 Summary** as final, 2–3 sentences, no longer provisional.

## Section 4 · Open Questions

- Answer every existing question this pass can: fill the Reply and set the Status. Leave **Blocking?** alone unless the blocking itself has changed. Answering a question doesn't make it non-blocking.
- Add rows for anything new: an unanswered non-functional category, a job/feature gap, a proposed Section 2 change awaiting confirmation. Give each the next number.
- Use the template's named statuses. Open means the user has something to decide; deferred or waiting-on-someone-else rows get the matching status, with the situation stated in the Reply.
- Never delete a row.

## Output

- Write into the same PRD file the problem pass wrote.
- Section 3 in full, 1.1 finalised, Section 2 changed only where confirmed, Section 4 updated in place.
- Add the design folder and any newly read documents to the Sources list, without duplicates. No inline citations.

## Before you finish

- Every 3.x subsection is backed by the design material or context documents, or holds an answer the user gave. Anything else is a Section 4 question.
- Every 2.3 job maps to a feature and every feature maps back to a job, or the gap is a named question.
- All five non-functional categories were asked, not inferred.
- Every feature has a priority and a reason, and not everything is Must.
- Every criterion has an identifier, numbered from 01 with no gaps or duplicates, under the right feature.
- **Read every criterion back for a second claim hidden behind "and",** and split it. A bundled row often hides the thing it forgot to say.
- Every identifier cited elsewhere resolves, and points at the right subject.
- Each rule is stated once; other features point to its identifier rather than repeating it.
- No feature has more than five acceptance criteria, none of them spec-level, or the exception is named with its reason.
- Every Section 1–2 change was explicitly confirmed.
- Every contradiction found is a row in the inconsistencies table, not just mentioned in chat.
- **Scan Sections 1–3 for history, lists that should be tables, and excess words.**
- Read the draft back section by section, and don't take silence as agreement.
- **Read the whole document as a stranger.** Could it be pasted into a different tool with no other context and still make sense?
