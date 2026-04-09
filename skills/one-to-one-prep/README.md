# one-to-one-prep — 1:1 Meeting Prep Generator for Managers

> Turn your notes and task tracker data into a structured 1-on-1 agenda in seconds.

**one-to-one-prep** is a Claude skill for team leads, engineering managers, and department heads. Paste your previous meeting notes and your report's task list — get a ready-to-use prep document with action item status, prioritized discussion topics, and wellbeing questions.

No integrations required. Works with plain text from any task tracker.

---

## What It Does

- Tracks action items from the previous 1-on-1 and marks each as Done, In Progress, or Overdue
- Analyzes task tracker data to surface completed work, stalled tasks, blockers, and anomalies
- Generates 3–5 prioritized discussion topics based on actual context
- Suggests open-ended motivation and wellbeing questions relevant to the situation
- Outputs a ready template for capturing new action items during the meeting
- Handles first meetings with no previous notes — switches to onboarding mode automatically

---

## How It Works

1. Paste your previous 1-on-1 notes (or say it's the first meeting)
2. Paste your report's task list from any tracker (Jira, Linear, Asana, ClickUp, Notion, or plain text)
3. Optionally add career goals, IDP, or OKRs for development-focused questions
4. Get a structured Markdown prep document ready for the meeting

---

## Quick Start

Open Claude and say:

> "Prep for my 1-on-1 with Alex"

Then paste your data when Claude asks for it.

---

## Trigger Phrases

**English:**
- "prep for my 1-on-1 with [name]"
- "one-to-one prep"
- "generate 1:1 agenda"
- "prepare for my one-on-one"
- "1-on-1 meeting prep"

**Russian:**
- "подготовь 1-on-1 с [имя]"
- "prep для ван-он-вана"
- "сгенерируй агенду для 1-on-1"
- "подготовка к встрече с сотрудником"

---

## Output Structure

```
# 1-on-1 Prep: [Name] — [Date]

## Action Items from Last Meeting
| Task | Status | Comment |
|------|--------|---------|

## Key Events This Period
Completed / At Risk / Blockers

## Discussion Topics
1. [High] ...
2. [Medium] ...
3. [Low] ...

## Motivation & Wellbeing Questions
- ...

## New Action Items
| Task | Owner | Due Date |
|------|-------|----------|
```

---

## Requirements

- Claude account (free or paid)
- Claude.ai Projects, Claude Cowork, or Claude Code
- No external integrations — works with plain text input

---

## Related Skills

- [decision-log](../decision-log/) — extract and track decisions from meeting notes
