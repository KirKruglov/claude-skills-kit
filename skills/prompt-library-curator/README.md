# Prompt Library Curator

Organise and tag your personal prompt collection into a structured, navigable markdown catalog — without any manual sorting.

## Overview

You have prompts saved in notes, files, or chat history — but they're scattered and hard to find when you need them. **Prompt Library Curator** takes your raw prompt collection and turns it into a clean `prompt-library.md` file with categories, tags, an index table, and duplicate detection. Unlike prompt-creation skills, this skill curates what you already have.

## Requirements

- Your existing prompts as pasted text or a `.md` / `.txt` file
- At least 1 prompt (recommended: 5–100 for best results)

## How to Use

1. Trigger the skill with one of the phrases below
2. Paste your prompts directly into chat — or reference a `.md`/`.txt` file
3. Receive a structured `prompt-library.md` catalog with categories, tags, and an index table

The skill preserves your original prompt text verbatim. It adds metadata around it, not inside it.

## Examples

**Example 1 — Pasted list:**

> *"organize my prompts"*
> [paste 20 prompts separated by blank lines]

→ Returns `prompt-library.md` with index table, 4 categories, 2 duplicates flagged.

**Example 2 — File-based:**

> *"tag my prompts — I have them in prompts.md"*

→ Reads `prompts.md`, assigns tags and complexity to each prompt, outputs structured catalog.

## Triggers

| English | Russian |
|---------|---------|
| `organize my prompts` | `организуй мои промпты` |
| `prompt library` | `библиотека промптов` |
| `tag my prompts` | `разбери мою коллекцию промптов` |
| `structure my prompt collection` | `структурируй промпты` |
