> [Версия на русском языке](README.ru.md)

# Context Builder Cowork — Claude Skill

> Creates a structured `project-context.md` file for Claude Cowork through a guided interview — ready to download and drop into any project.

---

## What It Does

Context Builder Cowork walks you through a structured interview and assembles a complete `project-context.md` file that Claude can use as a persistent project reference in Cowork. Two modes:

- **Full mode** — 15 questions across 9 blocks: basics, project essence, current goal, structure, participants, constraints, data paths, open questions, optional sections
- **Quick mode** — first 3 blocks only (8 questions); remaining sections are filled with `[to clarify]` placeholders

---

## How It Works

1. You trigger the skill with a phrase like "create project context"
2. Claude asks questions block by block — you answer at your own pace
3. Claude assembles a `project-context.md` file from your answers
4. You download the file and add it to your Cowork project

If you have all the information ready, you can provide it in one message — Claude will skip the interview and assemble the file directly.

---

## Quick Start

Open a conversation with Claude and say:

- "Create project context"
- "New project context for my analytics project"
- "Quick context — I need a fast setup"
- "Generate a context file for Cowork"

---

## Modes

| Mode | Trigger | Blocks covered |
|------|---------|----------------|
| Full (`new`) | "create project context" | All 9 blocks, 15 questions |
| Quick | "quick context" | Blocks 1–3, 8 questions; rest → placeholders |

---

## Output File Structure

```
project-context.md
├── Basics (type, status, dates)
├── Project Overview
├── Vision
├── Current Stage Goal
├── Project Structure
├── Participants and Dependencies
├── Constraints
├── Data Structure (input/output paths)
├── Open Questions
└── Changelog
```

---

## Requirements

- Claude account (free or paid)
- Claude Cowork or Claude.ai (any interface)

---

## What This Skill Does NOT Do

- Does not read existing files — context is built from your answers only
- Does not invent facts — unknown fields become `[to clarify]` placeholders
- Does not require Cowork to run — you can use it in any Claude conversation
