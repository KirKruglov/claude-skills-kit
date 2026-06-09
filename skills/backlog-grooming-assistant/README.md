> [Версия на русском языке](README.ru.md)

# Backlog Grooming Assistant

Prepare your grooming session in minutes — flag problematic backlog items and generate an agenda automatically from a local CSV or Markdown export.

---

## Overview

Backlog Grooming Assistant reads a local backlog export (CSV or Markdown table), flags items with common problems — missing owners, no estimates, stale tasks, blocked items without ETA, and priority inflation — and generates a structured grooming session agenda with a scorecard. No Jira API or external service required; it works entirely from pasted or uploaded file contents. Use this skill when preparing for sprint grooming, auditing an accumulated backlog, or reviewing open items after a sprint.

---

## Requirements

- A backlog export file (CSV with column headers, or Markdown table)
  - Minimum: ID/number column and title column
  - Optional but recommended: owner, priority, estimate/story points, status, last-updated date
- No additional tools or external services required

**Recommended:** Export directly from Jira, Linear, Notion, or any task manager as CSV; alternatively, copy a Markdown table from your project wiki.

---

## How to Use

1. **Export your backlog**
   - Download a CSV from Jira/Linear/Notion, or copy a Markdown table from your project file

2. **Trigger the skill**
   - Say: "Groom my backlog" or "Backlog grooming assistant"
   - In Russian: "Подготовь повестку груминга" or "Проверь бэклог на проблемы"

3. **Paste or upload the backlog content**
   - The skill detects the format (CSV or Markdown) automatically
   - It maps common column name variations (e.g., "SP" → estimate, "Assignee" → owner)

4. **Review your grooming report**
   - Get a Markdown report with: Scorecard, Top Issues table, and a Grooming Agenda
   - Use the agenda as your meeting structure — each topic lists affected items and a recommended action

---

## Examples

### Example 1: Flagging Unowned and Unestimated Items

**Input (CSV):**
```
ID,Title,Owner,Estimate,Status,Priority,Last Updated
PROJ-42,Redesign login page,,,"In Progress",High,2026-04-20
PROJ-43,Fix search pagination,alice,3,In Progress,Medium,2026-05-10
PROJ-44,Add export feature,,,Backlog,High,2026-04-01
PROJ-45,Update API docs,,2,Backlog,Low,2026-05-12
```

**Action:** Skill parses 4 items, applies 7 flag checks, detects priority inflation (50% High), staleness on PROJ-44 (42 days), and missing owners on PROJ-42, PROJ-44, PROJ-45.

**Output:**
```markdown
# Grooming Report — 2026-05-13

## Scorecard
- Total items: 4
- Flagged items: 3 (75%)
- No owner: 3
- No estimate: 2
- Stale (>14 days): 1
- Blocked without ETA: 0
- Priority inflation: YES (50% High)

## Top Issues for Grooming

| Item | Title | Flags | Priority |
|------|-------|-------|----------|
| PROJ-44 | Add export feature | NO_OWNER, NO_ESTIMATE, STALE | High |
| PROJ-42 | Redesign login page | NO_OWNER, NO_ESTIMATE | High |
| PROJ-45 | Update API docs | NO_OWNER | Low |

## Grooming Agenda

### 1. Assign owners to unowned tasks
**Items:** PROJ-42, PROJ-44, PROJ-45
**Problem:** 3 items have no assigned owner
**Recommended action:** Assign a responsible team member to each item before the sprint

### 2. Estimate unscored items
**Items:** PROJ-42, PROJ-44
**Problem:** 2 items have no story point estimate
**Recommended action:** Size these items as a team during grooming

### 3. Review stale items
**Items:** PROJ-44
**Problem:** No activity for 42 days
**Recommended action:** Confirm relevance or close/archive

### 4. Re-prioritize — too many High/Critical items
**Problem:** 50% of items are High priority (priority inflation)
**Recommended action:** Rank items and downgrade at least 1 to Medium
```

---

### Example 2: Markdown Table Backlog

**Input (Markdown table):**
```
| # | Title | Status | Owner | Priority |
|---|-------|--------|-------|----------|
| 1 | Onboarding flow redesign | Blocked | bob | Critical |
| 2 | Email notification bug | In Progress | alice | High |
| 3 | Dashboard performance | Blocked | | High |
| 4 | Mobile app crash on iOS 17 | Backlog | | Critical |
```

**Action:** Skill parses Markdown table, detects 2 blocked items without ETA, 2 missing owners, priority inflation (75% High/Critical), and no estimate column (skipped check noted).

**Output includes:**
- Grooming Agenda with blocked items as top priority
- Skipped Checks noting "NO_ESTIMATE requires column 'estimate'"

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Groom my backlog | Подготовь повестку груминга |
| Backlog grooming assistant | Груминг-ассистент |
| Review backlog issues | Проверь бэклог на проблемы |
| Help me prepare grooming agenda | Помоги подготовиться к груминг-сессии |
| Flag problems in my backlog | Найди проблемы в бэклоге |

---

**Version:** 1.0.0  
**Last updated:** 2026-05-13  
**User Guide:** [docs/USER-GUIDE.md](docs/USER-GUIDE.md) · [docs/USER-GUIDE.ru.md](docs/USER-GUIDE.ru.md)
