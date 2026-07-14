# Routines Setup Assistant User Guide

Learn how to use Routines Setup Assistant to configure Claude Cowork Scheduled Tasks without guesswork.

---

## Quick Start

Here's the fastest way to set up your first routine:

1. Say: "Set up routines" or "Help me create scheduled tasks"
2. Describe one recurring task: "Every Friday I summarize my weekly notes into a digest"
3. Answer 3 quick questions: input source, output format, frequency/time
4. Copy the generated prompt and paste it into Cowork → Scheduled Tasks → New Task

**Result:** A ready-to-paste Routine prompt with the correct format and frequency.

**Time:** ~5 minutes per routine

---

## Scenarios

### Scenario 1: Setting Up a Weekly Status Report

**Situation:**
You are a project manager who manually writes a weekly status report every Monday morning by reviewing project files. The process takes 30 minutes. You want Claude to do this automatically before you start work, so the report is ready in your notes folder when you arrive.

**What to do:**

1. Trigger the skill by saying: "Set up routines" or "Automate my recurring tasks"
   - The skill will ask you to describe a recurring task

2. Describe your task
   - "Every Monday morning I review all project files and write a status report with what's on track, what's at risk, and what's overdue."

3. Answer the 3 clarifying questions
   - **Input:** "Files in my /projects folder"
   - **Output:** "A markdown status report saved to /reports/week-status.md"
   - **Frequency:** "Every Monday at 07:30"

4. Review the generated prompt
   - Check that the folder path, output file, and frequency are correct
   - If anything is off, tell the skill: "Change the time to 08:00" and it will update

5. Copy the prompt and set up in Cowork
   - Open Cowork → Scheduled Tasks → New Task
   - Paste the prompt, set frequency to "Every Monday at 07:30"
   - Save and click "Run now" to test

**Expected result:**

You receive a Routine prompt like:
> "Scan all files in /projects, identify tasks that are on track, at risk, or overdue across all active project plans, and generate a structured weekly status report saved to /reports/week-status.md."

Starting next Monday, Claude runs this automatically at 07:30. Your status report is waiting for you when you start work — 30 minutes saved every week.

**Why this works:** The skill formats the prompt in the exact structure Cowork's scheduler needs. You get a tested, copy-pasteable prompt instead of guessing the right wording.

---

### Scenario 2: Setting Up Multiple Routines in One Session

**Situation:**
You are a knowledge worker who wants to automate three recurring workflows at once: a daily notes digest, a weekly competitor snapshot, and a monthly review of your goals file. You've been meaning to set these up for weeks but never had a clear starting point.

**What to do:**

1. Say: "Help me create scheduled tasks" — then describe your first task
   - "Every evening I want Claude to summarize what I captured in /daily-notes that day"

2. Answer questions for Task 1, then receive the first Routine prompt

3. When the skill asks "Do you have another task?", say yes and describe Task 2
   - "Every Friday afternoon, read my /competitor-notes folder and generate a delta report of what changed this week vs. last week"

4. Answer questions for Task 2, receive the second prompt

5. Describe Task 3
   - "First of each month, read my /goals.md file and generate a brief reflection on progress"

6. Say "done" when finished — receive the full summary block with all 3 prompts

**Expected result:**

You receive a single output block:
```
## Your Routines Setup

**Routine 1:** Every day at 18:00
> Read all files added to /daily-notes today, extract key ideas and action items, and save an end-of-day digest to digests/YYYY-MM-DD.md.

**Routine 2:** Every Friday at 16:00
> Review all files in /competitor-notes, identify changes since last week's snapshot, and generate a delta report saved to competitor-delta-YYYY-MM-DD.md.

**Routine 3:** Every 1st of the month at 09:00
> Read /goals.md, assess progress on each goal based on recent notes, and generate a monthly reflection saved to reviews/YYYY-MM-reflection.md.
```

You set up all three tasks in Cowork in under 10 minutes.

**Why this works:** The skill handles multiple tasks in a single conversational session, asking focused questions for each. No need to repeat context — it remembers your folder structure and preferences across the session.

---

### Scenario 3: Setting Up a Routine That Needs a Connector

**Situation:**
You are a team lead who wants Claude to pull unread Slack messages from your team channel every morning, summarize key updates, and save them to a daily briefing file. You're not sure if this is possible or how to phrase the prompt.

**What to do:**

1. Say: "Set up routines" and describe the task
   - "Every morning, summarize the new messages from our team Slack channel and save a briefing to /briefings/today.md"

2. The skill will note the connector dependency:
   - ⚠️ "This task needs the Slack connector. Make sure it's enabled in Cowork → Plugins before scheduling."

3. The skill still generates the prompt — configure the connector separately
   - Go to Cowork → Plugins → Slack and authenticate
   - Then paste the generated prompt into Scheduled Tasks

4. Set up and test
   - Run manually first to confirm the connector is working
   - If it fails, check that the Slack workspace is authorized and the channel name matches

**Expected result:**

You get a properly formatted Routine prompt with a clear dependency note. You know exactly what to set up before scheduling — no ambiguity.

**Why this works:** The skill surfaces connector requirements upfront so you don't waste time scheduling a task only to find it fails on the first run.

---

## Tips

### Tip 1: Be Specific About File Paths

When describing your task, mention the exact folder path if Claude needs to read files (e.g., `/notes/weekly`, `/projects/active`). Vague sources like "my notes" make it harder for the generated prompt to be specific. If you don't know the exact path, describe it ("the folder where I keep my project plans") — the skill will ask you to confirm.

**Pro tip:** After you paste the prompt into Cowork, do a manual test run first. If Claude can't find the folder, you'll catch it immediately instead of waiting until the scheduled time.

### Tip 2: Use "Every Day at [time]" for Tasks That Need Freshness

For tasks that should reflect the most recent state (e.g., today's notes, today's tasks), use a daily schedule rather than weekly. This ensures the output is always current. Pair with a specific time when the files are most likely to be complete (e.g., end of workday at 17:00, not 08:00 before you've done anything).

**Pro tip:** Name output files with `YYYY-MM-DD` in the path. This way each run creates a new file instead of overwriting, and you can compare outputs over time.

### Tip 3: Start with One Routine and Expand

If you're new to Cowork Scheduled Tasks, set up one routine first and let it run for a week before adding more. This helps you learn what works (prompt clarity, output format, timing) before scaling up. The skill makes it easy to come back and add more routines in a future session.

**Pro tip:** If a generated routine isn't producing what you expected, return to the skill and say "I need to update my weekly report routine" — describe what's wrong, and the skill will help you refine the prompt.

---

**Version:** 1.0.0  
**Last updated:** 2026-05-22
