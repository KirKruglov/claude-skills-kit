# Morning Standup Brief Generator — User Guide

Learn how to generate your daily standup brief from local files in under two minutes.

---

## Quick Start

Here's the fastest way to get a standup brief:

1. Make sure you have at least one `.md` or `.txt` file with your notes or tasks in a folder
2. Say: `"Morning standup brief"` and provide the path to your folder
3. Get back a standup brief with Yesterday / Today / Blockers / Questions

**Result:** A structured standup brief displayed in chat and saved as `standup-brief-YYYY-MM-DD.md` in your folder.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Solo developer preparing for a team standup

**Situation:**
You are a developer keeping your daily tasks in a `work.md` file. You have 5 minutes before your team's morning standup and need to quickly pull together what you did yesterday, what you're doing today, and flag any blockers — without digging through your notes manually.

**What to do:**

1. Open your Cowork session with the folder where `work.md` lives (or note the folder path)

2. Trigger the skill by saying: `"Morning standup brief"`
   - If you haven't set a working folder yet, provide the path: e.g., `/Users/yourname/work/`

3. Wait for the skill to scan your file and extract items
   - It will pick up `- [x]` items for Yesterday, `- [ ]` / `TODO` items for Today, and anything marked `BLOCKER`

4. Review the brief in chat
   - Double-check that blockers are correctly captured
   - Add anything the skill may have missed by editing the saved file

**Expected result:**

You receive a brief like:
```
## Yesterday (Done)
- Reviewed PR #22 and left comments
- Fixed flaky test in CI pipeline

## Today (Plan)
- Implement login timeout (due tomorrow)
- Respond to PR feedback from @Ivan

## Blockers
- Waiting on @Lead to approve DB schema change

## Questions / Awaiting Response
- Ask @DevOps about staging environment access
```

You read this brief aloud at standup — done in 60 seconds.

**Why this works:** Instead of scrolling through `work.md` every morning, you get a ready-to-read brief. No manual sorting, no forgetting blockers.

---

### Scenario 2: Product manager aggregating notes from multiple files

**Situation:**
You are a product manager with notes scattered across several files: `sprint-notes.md`, `meeting-log.md`, and `backlog-ideas.md`. Before your standup you need to know what progress was made, what's planned for today, and what's blocking the team.

**What to do:**

1. Put all relevant files in one folder (or use your existing project folder)

2. Trigger the skill: `"Compile my tasks and notes for today's standup"`
   - Provide the folder path

3. The skill will automatically:
   - Filter to files modified in the last 48 hours
   - Extract tasks, completed items, and blockers from all files
   - Deduplicate items appearing in multiple files

4. Review the brief
   - Check the **Sources** footer to confirm which files were used
   - If an important file was missed (no recent changes), mention it explicitly: "Also include planning.md"

**Expected result:**

You receive a combined brief pulling tasks from all files:
```
## Yesterday (Done)
- Closed 3 support tickets with design team
- Updated product roadmap for Q2

## Today (Plan)
- Prepare demo for stakeholder review (due today)
- Review sprint velocity with engineering lead

## Blockers
- Awaiting legal sign-off on Terms of Service update

## Questions / Awaiting Response
- Need answer from @Marketing on campaign timeline

---
Sources: sprint-notes.md, meeting-log.md
```

**Why this works:** Multiple files, one brief. No need to open each file and copy-paste manually.

---

### Scenario 3: Saving a standup log over time

**Situation:**
You want to keep a weekly log of your standups — one file per day — to review at the end of the week or for reporting purposes. You've been using the skill for a few days and want to make sure each brief is saved and accessible.

**What to do:**

1. Trigger the skill each morning: `"Daily brief"` — same folder every time

2. The skill automatically saves `standup-brief-YYYY-MM-DD.md` with today's date in the filename
   - Each day gets its own file: `standup-brief-2026-04-20.md`, `standup-brief-2026-04-21.md`, etc.
   - If today's brief already exists, the skill asks before overwriting

3. At the end of the week, open your folder — you'll have 5 brief files ready to review

4. Use your weekly briefs to draft your Friday status update or weekly retrospective

**Expected result:**

Your folder accumulates daily briefs:
```
/work-notes/
├── standup-brief-2026-04-18.md
├── standup-brief-2026-04-19.md
├── standup-brief-2026-04-20.md
├── tasks.md
└── meeting-log.md
```

**Why this works:** The skill creates a natural audit trail of your daily work with zero extra effort.

---

## Tips

### Tip 1: Use standard task markers for best results

The skill detects common task markers: `- [ ]` (open), `- [x]` (done), `TODO`, `BLOCKER`, `#task`. Using these consistently in your notes ensures the skill extracts the right items into the right sections. If you use custom markers (e.g., `[pending]` or `WIP`), the skill may not detect them and will fall back to extracting bullet points from your notes.

**Pro tip:** Add due dates directly in your task lines — e.g., `- [ ] Submit report (due 2026-04-21)`. The skill will sort by deadline and put the most urgent tasks first.

### Tip 2: Keep one folder, update daily

The skill works best when your notes are consolidated in a single folder that you update regularly. Files modified in the last 48 hours get priority — so if you update your `tasks.md` every day, you'll always get fresh results. If you have files scattered across multiple folders, consider creating a `standup/` folder with symlinks or copies of your key files.

### Tip 3: Don't overwrite — use the log

Each day's brief is saved with the date in the filename (`standup-brief-2026-04-20.md`), so your history is preserved automatically. If you ever need to recall what you were working on last Tuesday, just open the file. Resist the urge to edit the saved brief — keep it as a log. If you need to adjust your standup after the fact, add a note at the bottom rather than modifying the generated content.

---

**Version:** 1.0.0
**Last updated:** 2026-04-20
