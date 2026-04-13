# Weekly Digest Synthesizer

Turn scattered status files into a structured weekly digest in minutes.

---

## Overview

Weekly Digest Synthesizer compiles status updates from multiple `.md` and `.txt` files into a single structured weekly digest. It groups content by project area, surfaces action items and blockers across files, and outputs a ready-to-share markdown report. Use this skill when you need to aggregate your team's weekly status notes, prepare a Friday summary for leadership, or compile updates from multiple workstreams into one document before an all-hands meeting.

---

## Requirements

- One or more `.md` or `.txt` files containing status updates
  - Works with any structure: bullet lists, free-text notes, or formatted status reports
  - Files should be accessible in your working directory or a specified folder
- No additional tools or skills required

**Best results:** Files with clear project names in headings and explicit status keywords ("blocked", "on track", "at risk") produce the most structured digests. Free-text notes still work but may yield less structured output.

---

## How to Use

1. **Gather your status files**
   - Collect `.md` or `.txt` files with weekly updates from your team or personal notes
   - Place them in one folder or note the file paths

2. **Trigger the skill**
   - Say: "Compile weekly digest" or "Weekly status digest from my files"
   - In Russian: "Составь еженедельный дайджест" or "Скомпилируй статусы из файлов"
   - Provide the folder path or list of files when prompted

3. **The skill processes your files**
   - Reads all `.md` and `.txt` files in the specified location
   - Extracts updates, action items, owners, due dates, and blockers
   - Groups by project area and flags cross-cutting items

4. **Review your digest**
   - Receive `weekly-digest-YYYY-MM-DD.md` with a Summary, per-project sections, action items table, and risks
   - Share with your team or paste into your status email as-is

---

## Examples

### Example 1: Team Lead Compiling Friday Status

**Input:** Three files — `project-alpha.md`, `project-beta.md`, `infra.md`

```
# project-alpha.md
## Status: On track
- Completed API integration this week
- Code review done, ready for QA
- Action: Maria — write test cases by 2026-04-17

# project-beta.md
## Status: At risk
- Design delayed — waiting on client approval
- Blocker: No response from client since Monday
- Action: Alex — follow up with client by 2026-04-15

# infra.md
## Status: On track
- Server migration completed
- No blockers
```

**Action:** Skill reads all three files, extracts status, updates, action items, and the blocker.

**Output:**
```markdown
# Weekly Digest — 2026-04-13

**Compiled from:** 3 files | **Projects covered:** 3 | **Action items:** 2

## Summary

Two projects are on track; Project Beta is at risk due to pending client approval. One blocker requires follow-up this week.

## Projects

### Project Alpha
- **Status:** ✅ On track
- **Updates:** API integration complete; code review done; ready for QA
- **Action items:** Maria — write test cases by 2026-04-17
- **Blockers:** None

### Project Beta
- **Status:** ⚠️ At risk
- **Updates:** Design phase delayed
- **Action items:** Alex — follow up with client by 2026-04-15
- **Blockers:** No client response since Monday

### Infra
- **Status:** ✅ On track
- **Updates:** Server migration completed
- **Blockers:** None

## Cross-Cutting Action Items

| Owner | Action | Due | Source File |
|-------|--------|-----|-------------|
| Maria | Write test cases | 2026-04-17 | project-alpha.md |
| Alex | Follow up with client | 2026-04-15 | project-beta.md |

## Risks & Blockers
- Client not responding — project-beta.md
```

---

### Example 2: Manager Aggregating Sparse Notes

**Input:** Two files with unstructured notes — `team-updates.md`, `q2-initiatives.md`

```
# team-updates.md
Anna finished the onboarding redesign. Waiting on legal to review the new terms.
Backend team fixed the login bug reported last week.

# q2-initiatives.md
OKR tracking dashboard: 60% done. No blockers.
Hiring: 2 interviews scheduled for next week. No decision yet.
```

**Action:** Skill extracts raw progress points; infers status from tone; no explicit owners found for some items.

**Output:**
```markdown
# Weekly Digest — 2026-04-13

**Compiled from:** 2 files | **Projects covered:** 2 | **Action items:** 1

## Summary

Team updates show progress on onboarding redesign and a resolved bug. Q2 initiatives are advancing; OKR dashboard at 60%. One legal dependency is pending.

## Projects

### Team Updates
- **Status:** ✅ On track
- **Updates:** Onboarding redesign complete; login bug resolved
- **Action items:** TBD — legal review of new terms (no deadline)
- **Blockers:** Legal review pending

### Q2 Initiatives
- **Status:** ✅ On track
- **Updates:** OKR dashboard 60% complete; 2 hiring interviews scheduled
- **Blockers:** None

## Cross-Cutting Action Items

| Owner | Action | Due | Source File |
|-------|--------|-----|-------------|
| TBD | Legal review of new terms | TBD | team-updates.md |
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Compile weekly digest | Составь еженедельный дайджест |
| Weekly status digest | Еженедельный дайджест |
| Make a weekly summary from my files | Скомпилируй статусы из файлов |
| Synthesize my team updates into a report | Собери обновления команды в отчёт |
| Weekly digest from [folder/files] | Дайджест из моих файлов за неделю |

---

**Version:** 1.0.0
**Last updated:** 2026-04-13
