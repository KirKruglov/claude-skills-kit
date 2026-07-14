# Cowork Session Planner User Guide

Learn how to use Cowork Session Planner to start every session with a clear goal and structured work plan.

---

## Quick Start

Here's the fastest way to get your session brief:

1. Open your Cowork session with your project folder selected
2. Say: "Session brief"
3. Get back a brief with your project status, session goal, and work plan

**Result:** A structured plan ready to use as your session agenda.

**Time:** ~1 minute

---

## Scenarios

### Scenario 1: Starting a New Day on a Long-Running Project

**Situation:**
You are a product manager working on a multi-week documentation project. It's Monday morning and you haven't touched the project since Thursday. You remember there were a few things to finish, but you can't recall exactly where you left off. Before diving in, you want a clear picture of the current status and a focused plan for the day.

**What to do:**

1. Open your Cowork session with the project folder selected

2. Say: "Session brief" (nothing else needed)
   - The skill will scan your context.md, logs, and task files automatically
   - No additional input required

3. Review the brief
   - **Status** tells you where the project stands (pulled from your last log entry)
   - **Session Goal** shows the top recommended task based on your open work
   - **Work Plan** lists up to 5 prioritised items so you know exactly what to tackle first

4. Start with item 1 from the Work Plan
   - If the goal doesn't match what you had in mind, you can override it in your next message

**Expected result:**

You receive a brief showing your project name, last completed action, open tasks, and a ranked work plan. Instead of spending 10 minutes re-reading logs and task files yourself, you have a clear agenda in seconds.

**Why this works:** The skill reads the same files you would read manually — but does it in one pass, prioritises automatically, and surfaces blockers you might have missed.

---

### Scenario 2: Returning After a Break with a Specific Goal in Mind

**Situation:**
You are a content strategist. You've been away from a content calendar project for 4 days. You already know what you need to do today — finish the Q3 editorial plan — but you want a status check and a structured work plan so nothing slips through. You don't want to spend time re-reading files; you just want confirmation and a plan.

**What to do:**

1. Open your Cowork session

2. Say: "Prepare my session — I need to finish the Q3 editorial plan today"
   - Adding your goal after the trigger phrase overrides the auto-derived focus
   - The skill uses your stated goal as Session Goal and builds the work plan around it

3. Review the brief
   - **Session Goal** will show your stated goal (not an auto-derived one)
   - **Work Plan** will list sub-tasks or steps toward your stated goal
   - **Notes** will flag any blockers or missing files that could affect your work

4. Proceed directly to your first task
   - Say "save" if you want the brief stored as `output/session-brief.md` for reference

**Expected result:**

You receive a brief with your stated goal at the top and a breakdown of supporting tasks. Your context files are checked so you're aware of any changes since your last session.

**Why this works:** Combining your explicit goal with automatic file scanning saves both planning time and context-recovery time. You skip the "where was I?" phase entirely.

---

### Scenario 3: Mid-Session Re-focus After Getting Sidetracked

**Situation:**
You are an operations lead. You started your session two hours ago with a plan, but a chat message pulled you into an unrelated discussion. Now you're not sure what you were originally working on or whether you should continue what you were doing or switch to the new thing that came up.

**What to do:**

1. Say: "Session brief" or "What should I work on today in cowork"
   - The skill detects that you already have an active session (recent log entries or in-progress tasks)
   - It offers a **re-focus brief** instead of an initial brief

2. Review the re-focus brief
   - **Status** shows what you had in progress before the interruption
   - **Session Goal** is your original session goal (from log or task file)
   - **Notes** flags the mid-session state so you can decide consciously whether to continue or pivot

3. Decide and continue
   - If the original plan is still valid: continue from where you left off
   - If you need to pivot: state your new goal and trigger the skill again

**Expected result:**

You receive a re-focus brief that reminds you of your original plan and current open tasks. You make a conscious decision to continue or pivot — instead of defaulting to whatever came last.

**Why this works:** Interruptions are inevitable. The skill gives you a structured "re-entry point" that takes 30 seconds instead of 5 minutes of mental context-switching.

---

## Tips

### Tip 1: Richer Files → Richer Brief

The skill produces better briefs when your project has a `context.md` with a current status field, a `logs/log.md` with dated entries, and a `TASKS.md` with explicit statuses (pending/in_progress/done). You don't need all three, but each one adds a layer of accuracy to the brief.

**Pro tip:** Keep your log file updated with one-line entries at the end of each session. The skill uses the last entry as the primary "where we left off" signal.

### Tip 2: State Your Goal When You Already Know It

If you arrive at a session with a clear goal in mind, include it in the trigger phrase: "Session brief — I want to [goal]." This skips the auto-derivation step and builds the work plan directly around your stated intention. You still get the automatic status check and blocker detection.

### Tip 3: Save the Brief for Reference

If your work plan has 4–5 items and you want to track progress during the session, say "save" after the brief is generated. The skill writes it to `output/session-brief.md`. You can refer back to it mid-session without re-triggering the skill.

---

**Version:** 1.0.0
**Last updated:** 2026-04-27
