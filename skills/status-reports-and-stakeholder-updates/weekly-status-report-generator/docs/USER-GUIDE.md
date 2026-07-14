# User Guide — Weekly Status Report Generator

This guide covers realistic usage scenarios and tips for getting the best results from Weekly Status Report Generator.

---

## Quick Start

1. Open a new session with Claude.
2. Say: **"Write my weekly status report"**
3. Paste your raw notes for the week — any format works.
4. You'll get a Manager Report and a Skip-Level Brief, ready to copy and send.

---

## Scenarios

### Scenario 1: Friday end-of-week recap in under 2 minutes

**Situation:** It's Friday afternoon. You have scattered notes from Slack, a task manager, and a couple of meeting takeaways. Your manager expects a weekly update before EOD.

**What to do:**
1. Open a Claude session.
2. Say: "Write my weekly status report"
3. Paste everything you have — it can be messy:
   ```
   shipped the onboarding flow rework (finally!), reviewed alex's PR, had a planning meeting for Q3 — still unclear on scope, blocked on brand assets from design team, next week: finalize Q3 roadmap, catch up with sales
   ```
4. The skill extracts Done, In Progress, Blockers, and Next Week items automatically.
5. Copy the Manager Report block and paste it into your team channel or email.

**Expected result:** A clean 4-section status update, sent in under 2 minutes, no reformatting required.

---

### Scenario 2: Skip-level update for a monthly check-in

**Situation:** You have a monthly skip-level meeting next week and want to prepare a crisp 3-point summary of the past month's highlights.

**What to do:**
1. Collect your key wins, challenges, and upcoming focus from your notes.
2. Say: "Write my weekly status report" (the skip-level brief format works equally well for monthly summaries).
3. Paste a brief summary:
   ```
   Launched A/B test on pricing page — conversion up 12%. Led team through product sprint planning. Ongoing: redesigning the admin dashboard. Main struggle this month: unclear requirements from the product team kept slowing us down. Next month focus: close the admin dashboard redesign and kick off the analytics revamp.
   ```
4. Copy only the **Skip-Level Brief** section from the output.

**Expected result:** A focused 3-bullet executive summary — Top result, Main challenge, Next focus — ready to reference in your meeting or send as a pre-read.

---

### Scenario 3: Delegating status reporting during a busy travel week

**Situation:** It's a heavy travel week and you have 30 seconds, not 10 minutes, for your weekly update.

**What to do:**
1. Quickly jot anything down — even a voice memo transcription or raw Slack messages:
   ```
   met with partner team in Berlin — good progress on API specs, reviewed contract draft, nothing shipped this week due to travel, next week back in office — will push the partner API milestone
   ```
2. Trigger the skill. Even sparse notes produce a valid report — the skill flags when notes are brief.
3. Send the Manager Report as-is; use the Skip-Level Brief if needed.

**Expected result:** A complete status update from a 30-second note dump. The skill handles the structure; you handle the content.

---

## Tips

- **Don't format your notes.** The messier, the better. The skill handles bullet lists, paragraphs, numbered lists, and raw Slack pastes equally well.
- **Include metrics when you have them.** Any number in your notes (percentages, counts, dates) is preserved verbatim in the report — don't round or abbreviate.
- **For skip-level use only:** You can trigger the skill just to get a 3-bullet summary — ignore the Manager Report section if you only need the brief.
- **Recurring use:** Run the skill every Friday with consistent note-taking and you'll have an archive of structured weekly updates without any extra effort.

---

> Back to [README.md](../README.md)
