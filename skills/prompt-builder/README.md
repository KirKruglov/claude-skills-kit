> [Версия на русском языке](README.ru.md)

# Prompt Builder

> Build structured, reusable prompts for Claude through a guided 7-question interview.

---

## What It Does

Prompt Builder conducts an interactive interview and assembles a ready-to-use structured prompt based on your task description. Instead of writing a prompt from scratch, you answer 7 questions — and Claude does the formatting work.

The output is a clean Markdown document with clearly labeled sections:

- **Role** — what role Claude should take on
- **Context** — background and prerequisites Claude needs
- **Task** — the exact deliverable
- **Input data** — what you'll pass to Claude
- **Output requirements** — format, length, and style of the result
- **Constraints** — what to avoid, tone, restrictions
- **Examples** — optional input/output pair for clarity

---

## How It Works

1. You trigger the skill with a phrase like "create a prompt for X"
2. Claude asks 7 structured questions, one at a time
3. You answer each question — loosely worded answers are fine; Claude interprets intent
4. If an answer is unclear, Claude asks a focused follow-up before moving on
5. After all 7 questions, Claude assembles and displays the final prompt
6. You can request edits, or save the prompt as a `.md` file

---

## Quick Start

Open a conversation with Claude and say:

- "Create a prompt for code review"
- "Write a prompt for writing blog articles"
- "Prompt builder — I need a prompt for data analysis"
- "Help me build a prompt for summarizing meeting notes"

---

## Output

A self-contained Markdown document, ready to paste into any new Claude conversation. Example structure:

```markdown
## Role
Senior code reviewer with expertise in Python and clean code principles.

## Context
The codebase is a Django REST API maintained by a small team. We follow PEP 8 and prefer explicit over clever.

## Task
Review the provided code snippet for bugs, style issues, and optimization opportunities. Prioritize correctness first, then readability.

## Input data
A Python code snippet pasted directly into the chat.

## Output requirements
A structured list with three sections: Bugs, Style Issues, Optimization Suggestions. Each item should include a short explanation and a suggested fix.

## Constraints
Do not rewrite the entire function. Focus on targeted, minimal changes. Use a direct, technical tone.
```

---

## Requirements

- Claude account (free or paid)
- No file uploads or integrations required
- Works in any Claude interface: Claude.ai, API, Cowork

---

## What This Skill Does NOT Do

- It does not execute or test the prompts it generates — it only builds them
- It does not connect to any external tools, APIs, or files
- It does not remember previously built prompts across conversations
- It does not generate prompts automatically without the interview — the guided process is intentional
