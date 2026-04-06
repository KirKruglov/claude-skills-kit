# delegation-brief — Structured Task Brief Generator for Claude Cowork

Stop wasting tokens on vague instructions. `delegation-brief` asks you 5 targeted questions and outputs a clear, ready-to-use task brief for your Cowork session.

---

## What It Does

Most failed AI interactions share one root cause: the task wasn't described clearly enough. `delegation-brief` fixes this before work begins.

The skill runs a short 5-question interview and generates a structured brief with:

- **Task** — what needs to be done
- **Expected result** — format and shape of the output
- **Files involved** — what to touch
- **Off-limits** — what must not be changed
- **Success criteria** — how to know the task is done

Copy the brief, paste it at the start of a new Cowork session — and Claude has everything it needs to work correctly on the first try.

---

## How It Works

1. You trigger the skill with a phrase like "create a brief" or "help me delegate"
2. Claude asks you 4 questions in one go (type of task, expected output, files, restrictions)
3. Claude asks one final question: what does success look like?
4. Claude generates the brief — ready to copy and use

No file access required. No technical knowledge needed.

---

## Quick Start

Open a conversation with Claude and say:

> "Create a delegation brief"

or

> "Help me structure my task for Cowork"

Claude will guide you through the rest.

---

## Examples

**Before using the skill:**
> "Fix the report"

**After using the skill:**
> **Task:** Update the Q1 sales report to correct the revenue figures in the summary table.
> **Expected result:** Modified file with corrected numbers, formatting unchanged.
> **Files involved:** `reports/q1-sales.xlsx`
> **Off-limits:** Charts, pivot tables, raw data sheet.
> **Success criteria:** Summary table matches the source data in the raw sheet.

---

## Requirements

- Claude account (free or paid)
- Claude Cowork
- No external tools, APIs, or file access required

---

## Who It's For

- New Cowork users who aren't sure how to phrase a task
- Non-technical professionals delegating work to an AI assistant
- Anyone who has experienced Claude doing the wrong thing because the instructions weren't specific enough

---

## Installation

See [docs/INSTALL.md](docs/INSTALL.md) for step-by-step setup instructions.
