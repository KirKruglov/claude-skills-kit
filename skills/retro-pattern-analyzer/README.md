# Retro Pattern Analyzer

Stop re-reading the same complaints sprint after sprint. Surface what keeps coming back — and what your team has silently given up trying to fix.

---

## Overview

Retro Pattern Analyzer reads retrospective files from multiple sprints and produces a structured report that shows recurring pain points, unresolved action items, and stable positive patterns. It handles any common retro format (What went well / What went wrong / Action items, Start-Stop-Continue, Plus-Delta, and others) and works with plain `.md` or `.txt` files — no Jira or external tools required. Use this skill when preparing for quarterly retrospectives, identifying systemic problems that persist across sprints, tracking whether last sprint's action items actually got resolved, or reporting to leadership on team health trends.

---

## Requirements

- 2 or more retrospective files in `.md` or `.txt` format
  - Any standard retro format: What went well / What went wrong / Action items; Start-Stop-Continue; Plus-Delta; or free-text notes
  - Files can be named with dates (e.g., `retro-2026-03-15.md`) for automatic chronological ordering
  - Minimum 2 files required; recommended 3–10 for meaningful pattern detection
- No external tools, APIs, or integrations required

**Recommended:** Files from 3+ consecutive sprints yield the most actionable patterns. Two files will work but patterns are preliminary.

---

## How to Use

1. **Gather your retro files**
   - Collect `.md` or `.txt` files from your last 3–10 sprints
   - Place them in one folder, or note the individual file paths
   - Files can have any formatting — the skill detects sections automatically

2. **Trigger the skill**
   - Say: "Analyze retro files" or "Retro pattern analysis"
   - In Russian: "Проанализируй ретро" or "Паттерны в ретроспективах"
   - Provide the folder path or list of files

3. **The skill processes your files**
   - Parses sections from each file (went-well / went-wrong / actions)
   - Groups similar items into themes across sprints
   - Identifies recurring pains, unresolved actions, and positive patterns
   - Calculates frequency and trend for each theme

4. **Review your report**
   - Receive `retro-patterns-YYYY-MM-DD.md` with three blocks: Recurring Pains, Unresolved Action Items, and Stable Positive Patterns
   - Use it to open your next retro, brief leadership, or prioritize team improvements

---

## Examples

### Example 1: Quarterly retro review before planning

**Input:**
```
Folder: /sprints/retros/
Files: retro-q1-s1.md, retro-q1-s2.md, retro-q1-s3.md, retro-q1-s4.md
```

Each file contains sections like:
```
## What went wrong
- Deployment process took 2+ hours
- No clear owner for QA sign-off

## What went well
- Daily standups kept the team aligned

## Action items
- Automate deployment pipeline by S3
```

**Output (`retro-patterns-2026-04-17.md`):**
```markdown
## 🔴 Recurring Pains (went-wrong, ≥2 sprints)

| Theme | Sprints | Frequency | Trend |
|-------|---------|-----------|-------|
| Slow / manual deployment | S1, S2, S3, S4 | 4/4 | ↑ growing |
| Unclear QA ownership | S2, S3 | 2/4 | → stable |

## 🔁 Unresolved Action Items

| Action Item | Raised in | Reappeared in | Status |
|-------------|-----------|---------------|--------|
| Automate deployment pipeline | S1 | S2, S3, S4 | unresolved |

## ✅ Stable Positive Patterns

| Theme | Sprints | Frequency |
|-------|---------|-----------|
| Daily standups keep team aligned | S1, S2, S3, S4 | 4/4 |
```

---

### Example 2: Focus on delivery problems only

**Input:**
```
Files: retro-sprint-12.md, retro-sprint-13.md, retro-sprint-14.md
Focus: "delivery and release"
```

**Output:** Same report structure, filtered to show only themes related to delivery and release process.

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Analyze retro files | Проанализируй ретро |
| Retro pattern analysis | Паттерны в ретроспективах |
| Find recurring issues in retrospectives | Выяви паттерны в ретро |
| What keeps coming up in our retros? | Что повторяется из спринта в спринт? |
| Analyze our sprint retrospectives | Повторяющиеся темы в ретроспективах |

---

**Version:** 1.0.0
**Last updated:** 2026-04-17
