> [Версия на русском языке](README.ru.md)

# Routines Setup Assistant

Set up Claude Cowork Scheduled Tasks in minutes — no blank page, no guesswork.

---

## Overview

Routines Setup Assistant interviews you about your recurring workflows and generates ready-to-paste prompts for Claude Cowork's Scheduled Tasks feature. It asks three targeted questions per task (what input, what output, how often) and produces a structured prompt in the correct format — complete with frequency and setup instructions. Use this skill when you want to automate a weekly digest, a recurring status report, a daily review, or any other task you currently do manually on a schedule.

---

## Requirements

- Access to Claude Cowork with Scheduled Tasks enabled
- A description of at least one recurring task you want to automate (no specific format needed — plain language works)
- (Optional) If your task reads from files: know the folder path (e.g., `/projects`, `/notes/weekly`)

**Note:** Some tasks require Cowork connectors (e.g., reading email or Slack). If your task depends on an external tool, make sure the relevant connector is enabled in Cowork → Plugins before scheduling.

---

## How to Use

1. **Think of a recurring task**
   - Something you do weekly, daily, or monthly that Claude could handle
   - Examples: summarizing notes, generating status reports, reviewing project files

2. **Trigger the skill by saying:**
   - "Set up routines" or "Help me create scheduled tasks"
   - In Russian: "Настрой рутины" or "Помоги создать scheduled tasks"

3. **Answer 3 questions per task**
   - What input does the task need? (files, nothing — runs from memory)
   - What output should Claude produce? (saved file, report in chat, checklist)
   - How often and at what time? (e.g., every Monday at 08:00)

4. **Review your Routines**
   - Receive a formatted block with one prompt per task + frequency
   - Copy each prompt and paste into Cowork → Scheduled Tasks → New Task

---

## Examples

### Example 1: Weekly Project Status Report

**Input:** "Every Monday I scan my project files to check what's overdue and write up a summary."

**Action:** Skill asks about input folder, output format, and preferred time. User confirms `/projects` folder, markdown file output, Monday 08:00.

**Output:**
```
## Your Routines Setup

**Routine 1:** Every Monday at 08:00
> Scan all files in /projects for overdue tasks across all project plans and generate a concise weekly action list saved to weekly-overdue.md.

---

**Next steps:**
1. Open Claude Cowork → Scheduled Tasks
2. Click "New Task" and paste the prompt above
3. Set frequency to "Every Monday at 08:00"
4. Save and test with a manual run first
```

---

### Example 2: Daily Notes Digest

**Input:** "I add notes throughout the day to a /daily-notes folder. Every evening I want a summary of what I captured."

**Action:** Skill confirms folder path, output format (markdown saved to file), and time (17:00 daily).

**Output:**
```
## Your Routines Setup

**Routine 1:** Every day at 17:00
> Read all files added to /daily-notes today, extract key ideas and action items, and save a structured end-of-day digest to digests/YYYY-MM-DD.md.

---

**Next steps:**
1. Open Claude Cowork → Scheduled Tasks
2. Click "New Task" and paste the prompt above
3. Set frequency to "Every day at 17:00"
4. Save and test with a manual run first
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Set up routines | Настрой рутины |
| Help me create scheduled tasks | Помоги создать scheduled tasks |
| Automate my recurring tasks | Автоматизируй мои повторяющиеся задачи |
| I want Claude to run something every week | Хочу чтобы Claude запускался каждую неделю |
| Create a routine for me | Создай рутину для меня |

---

**Version:** 1.0.0  
**Last updated:** 2026-05-22
