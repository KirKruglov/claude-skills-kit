# Meeting Prep Briefer

Walk into every meeting prepared — participants, context, and open questions from your own files, in seconds.

---

## Overview

Meeting Prep Briefer generates a structured per-meeting brief for every call in your day. Give it your schedule (paste it or point to a file), and it scans your workspace notes to assemble a brief for each meeting: who's attending, relevant context from your files, open questions to resolve, and a suggested agenda. No calendar integrations, no CRM, no API keys — it works entirely with local files already in your Cowork workspace.

Unlike generic meeting-prep tools, this skill works offline and requires zero setup. If you keep notes, project files, or previous meeting summaries in your workspace, you already have everything it needs.

---

## Requirements

- A daily schedule — pasted as text or saved as a local `.md` / `.txt` file
- Optional: local workspace context files (project notes, participant notes, previous meeting summaries)
- No external tools or integrations required

**Note:** The skill produces a useful brief even without context files — it will flag which meetings have no matching notes and prompt you to add them.

---

## How to Use

1. **Prepare your schedule**
   - Paste it directly in the chat, or save it as `today.md` / `schedule.md` in your workspace
   - Minimum format: `10:00 — Team Sync (Alice, Bob)` — one meeting per line

2. **Trigger the skill**
   - Say: "Meeting brief" or "Prep my meetings"
   - Optionally include a file path: "Meeting brief from `today.md`"

3. **Receive your briefs**
   - One section per meeting with participants, context, open questions, and suggested agenda
   - Context is pulled automatically from matching workspace files

4. **Save if needed**
   - Say "save" to write the full brief to `output/meeting-brief-YYYY-MM-DD.md`

---

## Examples

### Example 1: Paste schedule inline

**Trigger:** "Meeting brief — 10:00 Team Sync (Alice, Bob, Carol), 14:00 1-on-1 with Bob"

**Output:**
```
# Meeting Brief — 2026-04-28

---

## 10:00 — Team Sync

**Participants:** Alice, Bob, Carol

**Context:**
- From `project-notes.md`: Sprint 12 ends Friday; 3 open stories remain.
- From `alice-notes.md`: API timeline flagged as a risk.

**Open Questions:**
- Is the API dependency resolved before Friday?
- Who owns design handoff?

**Suggested Agenda:**
1. Sprint status check (5 min)
2. API risk decision (10 min)
3. Owners & next steps (5 min)

---

## 14:00 — 1-on-1 with Bob

**Participants:** Bob

**Context:**
- No context files found — add relevant notes to your workspace.

**Open Questions:**
*(none listed — add questions before the meeting)*

**Suggested Agenda:**
1. Current blockers check-in (10 min)
2. Career development update (10 min)
```

---

### Example 2: Load schedule from file

**Trigger:** "Prep my meetings from `today.md`"

The skill reads `today.md` from your workspace, parses all meetings, scans for matching context files, and produces a full-day brief.

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| meeting brief | бриф по встречам |
| prep my meetings | подготовь встречи |
| prepare for today's meetings | бриф на встречи дня |
| briefing for my calls today | что нужно знать перед встречами |

---

**Version:** 1.0.0
**Last updated:** 2026-04-28
