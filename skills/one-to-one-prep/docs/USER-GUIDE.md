# one-to-one-prep — User Guide

Prepare for your monthly 1-on-1 meetings in seconds: paste your notes and task data, get a structured agenda with action item tracking, discussion topics, and wellbeing questions.

---

## How to Start

Open a conversation with Claude and use one of these phrases:

- "prep for my 1-on-1 with [name]"
- "one-to-one prep"
- "generate 1:1 agenda for [name]"
- "prepare for my one-on-one with [name]"

Claude will recognize the skill and ask for the input data.

---

## Step-by-Step Walkthrough

**Step 1.** Trigger the skill with a phrase like "prep for my 1-on-1 with Anna".

**Step 2.** Claude asks for your previous meeting notes. Paste them as plain text — any format works (bullet points, prose, your own shorthand). If it's the first meeting, say so — the skill switches to onboarding mode.

**Step 3.** Claude asks for the employee's task list for the period since the last meeting. Copy and paste directly from Jira, Linear, Asana, ClickUp, Notion, or any plain text format. The more detail, the better — but even a rough list works.

**Step 4.** Optionally share career goals, IDP, or OKRs. If you include them, the skill adds a development-focused discussion topic and a relevant wellbeing question.

**Step 5.** Claude generates the prep document. Review it, copy it to your notes, and you're ready for the meeting.

---

## Examples

### Example 1: Regular monthly 1-on-1

**You say:**
> "Prep for my 1-on-1 with Maxim. Previous notes: discussed burnout, agreed he takes smaller tasks. Action item: finish auth refactoring by end of month. Tasks this period: AUTH-112 auth refactoring — Done, FRONT-88 form component — In Progress, FRONT-91 validation bug — open for 18 days with no updates."

**Claude generates:**
> A prep document where AUTH-112 is marked Done, FRONT-91 is flagged as stalled (18 days without progress), discussion topics include [High] the stalled bug and [High] a burnout follow-up, and wellbeing questions ask about workload and what's blocking FRONT-91.

### Example 2: First meeting with a new report

**You say:**
> "Prep for my first 1-on-1 with Igor. No previous notes. Tasks this period: BACK-55 payment gateway integration — Done, BACK-61 API tests — In Progress."

**Claude generates:**
> A prep document in first-meeting mode: instead of action item tracking, it includes onboarding questions (expectations, working style, current priorities). Key events section covers the task data normally.

---

## What You Get

The output is a Markdown document with five sections:

**Action Items from Last Meeting** — a table with status (Done / In Progress / Overdue) and comments for each item from the previous meeting.

**Key Events This Period** — a structured summary of completed work, tasks at risk or stalled, and active blockers.

**Discussion Topics** — 3–5 topics prioritized by urgency: High (blockers, overdue items), Medium (stalled tasks, open questions), Low (achievements, development updates).

**Motivation & Wellbeing Questions** — 3–4 open-ended questions chosen based on the context (workload, blockers, career goals if provided).

**New Action Items Template** — an empty table for capturing commitments during the meeting.

---

## Tips for Best Results

- Paste the task list directly from your tracker — even a raw export works well.
- Include the employee's name so the document header is correct.
- If the period had no notable events, say so — the skill will focus entirely on open questions and development topics.
- For recurring 1-on-1s, keep your previous prep document as the "notes from last meeting" input for the next one.
- Add OKRs when approaching a quarter boundary — the skill will check progress automatically.

---

## FAQ

**Q: What if I don't have notes from the previous meeting?**
A: Say "this is our first meeting" or "I don't have notes from last time." The skill switches to first-meeting mode and generates onboarding questions instead of action item tracking.

**Q: Does the skill integrate with Jira, Linear, or other trackers?**
A: No — it works with plain text only. Copy and paste your task list from any tool. No API connections or integrations needed.

**Q: Can I use it for formats other than monthly 1-on-1s?**
A: Yes. The skill works for any regular manager-report meeting — weekly, bi-weekly, or monthly. Just paste the relevant period's data.

---

## Limitations

- Does not store meeting history between sessions — each run is independent.
- Does not access external systems or task trackers directly.
- Does not write performance reviews or generate ratings.
- Output quality depends on the completeness of input data — the more context, the better the prep document.

---

## Need Help?

If the skill isn't working as expected, check the [installation guide](INSTALL.md) to make sure everything is set up correctly.
