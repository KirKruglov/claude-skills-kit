# Meeting Prep Briefer — User Guide

Practical scenarios for getting the most out of Meeting Prep Briefer.

---

## Quick Start

1. Paste your schedule or point to a file: "Meeting brief — 09:00 Product review (Anna, Mike), 15:00 Stakeholder update"
2. Receive one section per meeting with context, open questions, and agenda
3. Say "save" to write the brief to `output/meeting-brief-YYYY-MM-DD.md`

---

## Situations

### Situation 1: Busy morning, multiple back-to-back meetings

**Context:** You have 4 meetings starting at 9 AM. You have 10 minutes to prepare.

**What to do:**
1. Open your Cowork session with the project folder selected
2. Say: "Meeting brief — [paste your day's schedule]"
3. The skill scans your notes and produces a brief for each meeting in under a minute

**Expected result:** A single document with 4 sections — one per meeting — each containing context extracted from your workspace files. Meetings with no matching notes will show a placeholder prompt.

**Tip:** Keep a `today.md` file in your workspace and update it each morning — then just say "Meeting brief from `today.md`" every day.

---

### Situation 2: Preparing for a high-stakes 1-on-1

**Context:** You have a 1-on-1 with a direct report. You have notes from previous meetings and a running topics file.

**What to do:**
1. Ensure `bob-notes.md` or `1on1-bob.md` exists in your workspace with previous topics and action items
2. Say: "Prep my meetings — 14:00 1-on-1 with Bob"
3. The skill matches `bob` as a keyword and extracts relevant context from your notes file

**Expected result:** A brief with Bob's open action items from last session, unresolved questions, and a suggested agenda covering blockers and development topics.

**Tip:** Name your notes files after participant names (e.g., `bob.md`, `anna-notes.md`) — the skill uses filenames to match context automatically.

---

### Situation 3: End-of-day review — prepping tomorrow's meetings

**Context:** You want to prepare for tomorrow's meetings before logging off today.

**What to do:**
1. Save tomorrow's schedule to `tomorrow.md`
2. Say: "Meeting brief from `tomorrow.md` for 2026-04-29"
3. The brief will be dated for tomorrow and saved accordingly

**Expected result:** A full-day brief with tomorrow's date in the header, saved to `output/meeting-brief-2026-04-29.md`.

---

## Tips

- **File naming matters:** Name context files after meeting topics or participant names (`sprint-review.md`, `anna.md`, `q2-planning.md`) — the skill uses these to match context automatically.
- **Add open questions to your notes:** If you write "?" or "open question:" in your notes files, the skill extracts these into the Open Questions section.
- **Schedule format flexibility:** Any format with a time + title on each line works: `10:00 Team Sync`, `10:00 — Team Sync`, `10:00 | Team Sync (Alice, Bob)`.
- **Save for sharing:** Use the "save" command to export the brief as a markdown file — share it with participants or keep it as a meeting record.
- **No notes? Still useful:** Even with no context files, the skill generates a suggested agenda from the meeting title and participants — a useful starting point.
