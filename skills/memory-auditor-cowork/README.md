# Claude Memory Auditor for Cowork — Keep Your File-Based Memory Clean

Find contradictions, outdated entries, duplicates, and noise across all Cowork memory layers.

---

## What It Does

Memory Auditor for Cowork scans file-based memory layers specific to the Cowork environment: auto-memory (MEMORY.md + individual files), CLAUDE.md, User Preferences, and Project Instructions. It detects problems that degrade Claude's performance over time and proposes specific fixes with your explicit approval before making any changes.

This is a companion to [memory-auditor-chat](../memory-auditor-chat/) which works with native Claude.ai memory (Memory Edits, Memory Summary). Use **memory-auditor-cowork** when working in the Claude Cowork desktop app.

## How It Works

1. **Context detection** — automatically identifies your Cowork environment (project or standalone) and available memory layers
2. **Overview** — shows memory stats by layer and a count of potential issues (you can stop here)
3. **Deep analysis** — classifies problems into four categories: contradictions, outdated entries, duplicates, and noise
4. **Actionable output** — for auto-memory files: direct edit/delete actions; for CLAUDE.md, User Preferences, and Project Instructions: step-by-step manual instructions

## Quick Start

Open a Cowork session and say:

- "audit memory"
- "memory health check"
- "проверь память"

Claude will run the audit and present findings in a structured report.

## Key Differences from memory-auditor

| Aspect | memory-auditor | memory-auditor-cowork |
|--------|---------------|----------------------|
| Environment | Claude.ai (chat, project) | Cowork (standalone, project) |
| Layers | Memory Edits, Memory Summary, Project Summary, Project Instructions | auto-memory, CLAUDE.md, User Preferences, Project Instructions |
| Tools | `memory_user_edits`, `conversation_search` | Read, Write, Edit, Glob, Grep |
| Can modify | Memory Edits | auto-memory files |
| Output format | Flexible | Fixed template |

## Problem Categories

- **Contradiction** — conflicting entries across or within memory layers (highest priority)
- **Outdated** — facts that have changed based on newer records (highest priority)
- **Duplicate** — overlapping entries that can be merged (medium priority)
- **Noise** — correct but low-value entries: intermediate states, one-off facts, frontmatter mismatches (low priority)

## Requirements

- Claude account (free or paid)
- Claude Cowork desktop app
- No external tools or API keys required

## Safety

Memory Auditor never performs a full memory reset. Every change to auto-memory files requires your explicit confirmation. The skill cannot directly modify CLAUDE.md, User Preferences, or Project Instructions — it provides manual instructions instead. MEMORY.md index is always kept consistent after changes.
