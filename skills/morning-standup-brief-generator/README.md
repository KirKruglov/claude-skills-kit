# Morning Standup Brief Generator

Turn your local notes and task files into a ready-to-use standup brief in seconds — no integrations required.

---

## Overview

Morning Standup Brief Generator compiles your local `.md` and `.txt` files into a structured daily brief in the classic standup format: **Yesterday / Today / Blockers / Questions**. It scans your working folder, extracts tasks and notes, prioritizes by deadline, and outputs a clean brief you can read at your morning standup. Use this skill when you want to prepare for a daily standup in under two minutes, when your tasks live in local files rather than a task manager, or when you want a file-based standup log without installing anything.

---

## Requirements

- A folder containing your notes and/or task files (`.md` or `.txt` format)
  - Files should contain task markers: `- [ ]` (open), `- [x]` (done), `TODO`, `BLOCKER`, etc.
  - Plain notes (without markers) are also supported — key points are extracted from bullet lists
- No external tools, connectors, or API keys required

**Recommended:** Keep your daily notes or task files in one working folder. Files modified in the last 48 hours get priority — older files are included only if no recent ones exist.

---

## How to Use

1. **Locate your working folder**
   - Find the folder where you keep your notes, task lists, or project files
   - Make sure it contains at least one `.md` or `.txt` file

2. **Trigger the skill**
   - Say: `"Morning standup brief"` or `"Prepare me for standup"`
   - In Russian: `"Утренний бриф для стендапа"` or `"Подготовь меня к стендапу"`

3. **Provide your folder path**
   - Tell the skill the path to your working folder (e.g., `/Users/yourname/work-notes/`)
   - If you're in a Cowork session with a folder selected, the skill uses that folder automatically

4. **Get your brief**
   - The skill scans your files, extracts done items, open tasks, blockers, and questions
   - You receive a formatted standup brief in chat
   - The brief is also saved as `standup-brief-YYYY-MM-DD.md` in your working folder

---

## Examples

### Example 1: Preparing for a daily standup from task notes

**Input:**
```
tasks.md (modified today):
- [x] Reviewed PR #14 — approved
- [x] Sent weekly report to manager
- [ ] Update API docs (due 2026-04-21)
- [ ] Schedule Q2 planning meeting
- BLOCKER: Waiting for design mockups from @Anna before starting front-end work
```

**Action:** Skill reads `tasks.md`, extracts completed items for Yesterday, open tasks for Today (sorted by deadline), and the blocker.

**Output:**
```markdown
# Standup Brief — 2026-04-20

## Yesterday (Done)
- Reviewed PR #14 — approved
- Sent weekly report to manager

## Today (Plan)
- Update API docs (due 2026-04-21)
- Schedule Q2 planning meeting

## Blockers
- Waiting for design mockups from @Anna before starting front-end work

## Questions / Awaiting Response
— none

---
*Generated: 2026-04-20 | Sources: tasks.md*
```

---

### Example 2: Multiple files with mixed notes and tasks

**Input:**
```
project-notes.md (modified today):
## Meeting takeaways
- Agreed to push release to April 25
- TODO: Prepare release checklist
- ASK @Mikhail about deployment pipeline

work-log.md (modified yesterday):
- [x] Fixed bug in auth module
- [ ] Write unit tests for auth fix
- BLOCKED: Can't merge until CI is green
```

**Action:** Skill reads both files, deduplicates, builds brief with items from across files.

**Output:**
```markdown
# Standup Brief — 2026-04-20

## Yesterday (Done)
- Fixed bug in auth module

## Today (Plan)
- Prepare release checklist
- Write unit tests for auth fix

## Blockers
- Can't merge until CI is green

## Questions / Awaiting Response
- Ask @Mikhail about deployment pipeline

---
*Generated: 2026-04-20 | Sources: project-notes.md, work-log.md*
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Morning standup brief | Утренний бриф для стендапа |
| Daily brief | Дейли бриф |
| Prepare me for standup | Подготовь меня к стендапу |
| Compile my tasks and notes for today's standup | Собери мои задачи и заметки для стендапа |

---

**Version:** 1.0.0
**Last updated:** 2026-04-20

> 📖 For detailed usage scenarios and tips, see [docs/USER-GUIDE.md](docs/USER-GUIDE.md)
