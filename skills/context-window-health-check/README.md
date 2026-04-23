# Context Window Health Check

A Claude skill that assesses the health of your current session and tells you — in plain language — whether to keep going, create a handoff, or start fresh. No token counts, no code required.

## Overview

Long Claude sessions can quietly degrade: Claude may start losing track of earlier details, repeat itself, or give inconsistent answers. This skill detects those warning signs and gives you a clear, actionable status in seconds — designed for non-technical users who don't want to think about context windows or tokens.

Unlike CLI tools (e.g., Claude Code's token counter), this skill works entirely inside the chat interface.

## Requirements

No files needed. The skill reads the current conversation directly.

## How to Use

1. Type one of the trigger phrases below (or describe what you're experiencing)
2. The skill analyses visible session signals: message count, topic diversity, and any symptoms you mention
3. You receive: a status indicator (🟢 / 🟡 / 🔴), a plain-language explanation, and one concrete recommendation

## Examples

**Example 1 — Explicit check**
> "Check my context — we've been working on this for a while."

Response: `🟡 Caution — This session spans several topics and has been running for about 25 turns. Claude may start losing early details. Recommendation: Create a handoff summary before starting the next task. → Use session-handoff-composer.`

**Example 2 — Symptom-based trigger**
> "You seem to be forgetting what we agreed on earlier about the project structure."

Response: `🔴 Critical — You've reported that Claude is losing track of earlier context. This is a strong signal that the session has exceeded reliable working memory. Recommendation: Start a new session. → Use session-handoff-composer to preserve key context before switching.`

## Triggers

| English | Russian |
|---------|---------|
| `check my context` | `проверь мой контекст` |
| `context health check` | `оценка контекста` |
| `is my context running out` | `контекст заканчивается?` |
| `should I start a new session` | `мне нужна новая сессия или можно продолжать` |

## Status Reference

| Status | Meaning | Recommendation |
|--------|---------|----------------|
| 🟢 Healthy | Session is in good shape | Keep working |
| 🟡 Caution | Session is getting long or branching | Create a handoff before the next major task |
| 🔴 Critical | High risk of context loss | Start a new session; use `session-handoff-composer` first |

## Related Skills

- **session-handoff-composer** — create a structured handoff document when starting a new session
