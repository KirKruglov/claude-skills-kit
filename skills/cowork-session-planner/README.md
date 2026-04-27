# Cowork Session Planner

Start every Cowork session with a clear focus — your status, goal, and work plan in one brief.

---

## Overview

Cowork Session Planner generates a pre-session brief by scanning your project files (context, logs, tasks) and producing a minimal structured plan: current status, recommended session goal, and a prioritised work list. Use this skill at the very start of a Cowork session, when returning after a day or more away from a project, or any time you feel unfocused and unsure where to begin. Unlike session handoff skills that help you exit a session, this skill helps you enter one.

---

## Requirements

- A Cowork workspace with at least one of the following files:
  - `context.md` or `CLAUDE.md` — project overview
  - `logs/log.md` — recent activity log
  - `TASKS.md` or similar task file
- No external tools or integrations required
- Works with any project folder structure; richer files → richer brief

**Note:** If none of the above files exist, the skill will prompt you to provide a session goal manually.

---

## How to Use

1. **Open your Cowork session**
   - Make sure your project folder is selected (or note its path)

2. **Trigger the skill at the start of the session**
   - Say: "Session brief" or "Prepare my session"
   - Optional: add a goal — e.g. "Session brief — I want to finish the skill spec today"

3. **Receive your brief**
   - The skill scans your project files and produces a brief with: project status, session goal, and work plan (up to 5 items)
   - Blockers and missing files are flagged automatically

4. **Start working**
   - Use the work plan as your agenda for the session
   - Say "save" if you want the brief saved to `output/session-brief.md`

---

## Examples

### Example 1: Starting a new day on a skill development project

**Trigger:** "Session brief"

**Output:**
```
## Session Brief
**Project:** skills-dev
**Status:** team-update-aggregator completed 2026-04-24; cowork-session-planner is next in backlog (RICE 4.0, status: new).

### Session Goal
Develop cowork-session-planner skill package: spec → package → eval → README update.

### Work Plan
1. Write skill-spec.md for cowork-session-planner
2. Generate skill package (SKILL.md, README, USER-GUIDE)
3. Run eval testing
4. Update root README

### Blockers
- None

### Notes
- No open tasks file found; work plan derived from backlog.md and log.md
```

---

### Example 2: Returning after a 3-day break with a stated goal

**Trigger:** "Prepare my session — I need to finish the eval report for cowork-session-planner"

**Output:**
```
## Session Brief
**Project:** skills-dev
**Status:** cowork-session-planner package generated 2026-04-27; eval not yet run.

### Session Goal
Finish the eval report for cowork-session-planner and update root README.

### Work Plan
1. Run eval-runner on cowork-session-planner package
2. Review eval-report.md and apply any fixes
3. Update root README.md and README.ru.md
4. Update backlog.md status → done

### Blockers
- None

### Notes
- Your stated goal overrides the derived plan.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| session brief | бриф сессии |
| prepare my session | подготовь сессию |
| start my cowork session | начни мою сессию |
| what should I work on today in cowork | что делать в этой сессии |

---

**Version:** 1.0.0
**Last updated:** 2026-04-27
