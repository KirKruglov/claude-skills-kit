# Workspace Health Monitor — Claude Skill for Managers

> Weekly workspace audit: find forgotten tasks, orphaned files, and conflicting information in your notes and plans.

---

## What It Does

Workspace Health Monitor scans your working files — meeting notes, plans, task lists, logs — and produces a structured audit report highlighting:

- **Orphaned files** — documents not linked to any active project
- **Forgotten action items** — commitments buried in notes, never transferred to a task tracker
- **Duplicates and conflicts** — multiple versions of the same document, or contradictory dates and decisions across files
- **Cleanup recommendations** — prioritized list of what to archive, merge, or transfer
- **Clutter score** — an overall verdict ("Clean", "Moderate", "Cluttered", "Chaos") with a one-line summary

---

## How It Works

1. You provide your workspace files — via Cowork file access, file upload, or pasting text into the chat
2. Optionally, you list your active projects (just names is enough)
3. The skill scans all files, detects patterns, and cross-references content
4. You receive a formatted audit report with prioritized action items

If you don't provide the active projects list, the skill infers them from your file contents.

---

## Quick Start

Open a conversation with Claude and say:

- "Run a workspace health check on my notes folder"
- "Find forgotten action items in my files"
- "Audit my workspace — here are my meeting notes: [paste]"
- "Weekly cleanup — check for orphaned files"

---

## Examples

**Example 1:** You paste 10 meeting notes from the past month. The skill finds 3 action items with names attached ("Check with Alex", "Send to Maria") that were never completed, 2 files mentioning a project that no longer appears in any active plan, and a date conflict between two planning documents.

**Example 2:** In Cowork, you point the skill at your notes folder. It scans 30 files, identifies 8 orphaned files from a completed project, extracts 5 forgotten ToDo items, and gives you a "Moderate" clutter score with a 15-minute cleanup plan.

---

## Requirements

- Claude account (free or paid)
- Files accessible via one of: Cowork file access, file upload, or copy-paste
- Works best with text files: .md, .txt, .docx content, plain text notes
- Does not require integrations with external task trackers

---

## What This Skill Does NOT Do

- It does not delete or move files — recommendations only
- It does not connect to Jira, Asana, Linear, or other task trackers
- It does not analyze binary files without readable text content
- It does not replace your judgment — the audit is a diagnostic, not an order

---

## Related Skills

- `project-onboarding` — set up a new project context
- `memory-auditor-cowork` — audit Claude's own memory files in Cowork
