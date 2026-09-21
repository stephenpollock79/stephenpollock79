# Project Workflow

How I took [The Gaffer](https://github.com/stephenpollock79/fpl-advisor#the-gaffer) from idea to deployed app, and how AI was used at each step.

> **Read this in context.** This is what worked for one product manager who can't code, building solo, on a small personal product. It isn't a template for teams, regulated products or larger codebases. Take the parts that fit your situation and change the rest.

![The workflow: seven steps in order, then a spec, build, test, review loop repeated per slice, then a validation pass](images/project-workflow.svg)

## Modes of working with AI

Each step used one of four modes, depending on the stakes:

| Mode | Who does the work | Who reviews it |
|---|---|---|
| **1 · Human only** | Human | Another human |
| **2 · AI validation** | Human | AI reviews and helps iterate |
| **3 · Human validation** | AI | Human reviews and helps iterate |
| **4 · Autonomous AI** | AI | AI reviews and iterates on its own |

## Step by step

| # | Step | How I did it | Mode |
|---|---|---|---|
| 1 | **Strategy & objectives** | Wrote down why the project existed: what I needed to learn (deploying, logins, a real database). | 2 |
| 2 | **Ideation** | Took a long list of ideas and had AI attack each one from five different user viewpoints. Scored the survivors against pass/fail tests, then had AI research competitors and data sources for the winner | 2 |
| 3 | **Discovery** | Defined the problem only, not the solution. AI drafted it from my input, then a separate AI pass interrogated it before any design started | 3 |
| 4 | **Design** | Briefed an AI design tool with real app patterns to copy. It produced an 11-screen clickable prototype in about two days; an AI design critique then drove a second version | 3 |
| 5 | **Shaping** | Wrote the detailed requirements *from* the prototype, not before it: nine features, each with testable acceptance criteria. A second interrogation pass produced a numbered decision log, so nothing got argued twice | 3 |
| 6 | **Tech design** | AI proposed the technical choices (stack, data model, security boundaries) as short decision records. I ruled on the consequences, not the code | 3 |
| 7 | **Planning** | Split the work into 12 slices, each small enough to build in a day or so. Deployed an empty app (hosting, database, login) before building any feature | 3 |
| ↻ | **Spec** | AI wrote each slice's spec just before building it, after reading the previous slice's review | 4 |
| ↻ | **Build** | A coding agent built the slice against its spec and ticket | 4 |
| ↻ | **Test** | Automated tests, each named after the requirement it proves, plus me using it on my phone | 3 |
| ↻ | **Review** | A fresh AI session, with no memory of building it, checked the slice against its spec: what was built but not asked for, what's missing, what was decided silently | 4 |
| 8 | **Validate** | Tested whole journeys end to end, then ran a security probe (it found public sign-up switched on in production), a polish pass, and a retro | 3 |

## What went well, and what I'd improve

| Went well | I'd improve |
|---|---|
| **Time spent before coding.** A prototype, then requirements written from that prototype, then a spec for each slice. Requirements drawn from something real were specific, and the build ran with relatively few problems | **Stop sooner on repeat failures.** One feature took eighteen attempts before the wrong assumption behind it was found |
| **The review loop.** Each fresh-eyes review made the next slice's spec better | **Keep human checks human.** If a step needs a person to review it (mode 3), don't let it slide into AI checking itself (mode 4) when time is short |
| **Solo, in under three weeks.** From problem brief to a deployed app with a real database and login | **Set project and AI rules on day one.** Decide how you want to work with AI before you start, not as problems appear |

---

[← Back to the playbook](README.md)
