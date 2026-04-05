# Claude Memory Auditor (Chat) — Keep Your AI Memory Clean and Accurate

Find contradictions, outdated entries, duplicates, and noise across all Claude.ai native memory layers.

---

## What It Does

Memory Auditor Chat scans every layer of Claude's native memory system — Memory Edits, Memory Summary, Project Summary, and Project Instructions — to detect problems that degrade Claude's performance over time. It adapts the audit scope to your Claude.ai environment (general chat or project) and proposes specific fixes with your explicit approval before making any changes.

> **Note:** This skill is designed for Claude.ai (web interface). For Cowork environments, use [memory-auditor-cowork](../memory-auditor-cowork/).

## How It Works

1. **Tool & context detection** — checks tool availability and identifies your environment and available memory layers
2. **Overview** — shows memory stats and a count of potential issues (you can stop here)
3. **Deep analysis** — classifies problems into four categories: contradictions, outdated entries, duplicates, and noise
4. **Actionable output** — for Memory Edits: direct delete/replace actions; for other layers: step-by-step manual instructions

## Quick Start

Open a conversation with Claude and say:

- "audit memory"
- "memory health check"
- "check my memory for issues"

Claude will run the audit and present findings in a structured report grouped by priority.

## Problem Categories

- **Contradiction** — conflicting entries across or within memory layers (highest priority)
- **Outdated** — facts that have changed based on newer records or chat history (highest priority)
- **Duplicate** — overlapping entries that can be merged (medium priority)
- **Noise** — correct but low-value entries: intermediate states, one-off questions, redundant phrasing (low priority)

## Supported Environments

| Environment | Available Layers | Auto-fix |
|-------------|-----------------|----------|
| Claude.ai general chat | Memory Edits, Memory Summary | Memory Edits |
| Claude.ai project | Memory Edits, Memory Summary, Project Summary, Project Instructions | Memory Edits |

## Requirements

- Claude account (free or paid)
- Access to Claude.ai (web interface)
- No external tools or API keys required

## Safety

Memory Auditor never performs a full memory reset. Every change to Memory Edits requires your explicit confirmation. The skill cannot directly modify Memory Summary, Project Summary, or Project Instructions — it provides manual instructions instead.

## Related Skills

- [memory-auditor-cowork](../memory-auditor-cowork/) — audits file-based memory in Cowork (auto-memory, CLAUDE.md, User Preferences, Project Instructions)
