# Backlog Grooming Assistant — User Guide

Learn how to turn a raw backlog export into a structured grooming session agenda in minutes.

---

## Quick Start

Here's the fastest way to get a grooming report:

1. Export your backlog as CSV from Jira, Linear, or Notion (or copy a Markdown table)
2. Say: "Groom my backlog" and paste the file contents
3. Get back a Markdown report with a Scorecard, Top Issues table, and Grooming Agenda

**Result:** A ready-to-use meeting agenda with flagged items and recommended actions.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Preparing for a Sprint Grooming Meeting

**Situation:**
You are a Product Manager. Tomorrow's grooming session starts in 24 hours and you have a 60-item backlog. You need to identify which items need attention before the team can discuss them — missing owners, items without estimates, and tasks that haven't been touched in weeks. Without a structured scan, the session will drag on as the team discovers problems live.

**What to do:**

1. Export your backlog from Jira or Linear as CSV
   - Include columns: ID, Title, Owner/Assignee, Estimate/SP, Status, Priority, Last Updated
   - Save the file or leave it open in your spreadsheet

2. Trigger the skill: "Backlog grooming assistant"
   - Paste the CSV content (or the Markdown table if exporting from Notion)
   - Wait for the skill to parse all 60 items and apply flag checks

3. Review the Scorecard
   - See how many items have issues (e.g., "18 flagged (30%)")
   - Check priority inflation: if >50% are High/Critical, that's a signal to re-prioritize

4. Use the Grooming Agenda as your meeting structure
   - Copy the agenda into your meeting invite or Confluence page
   - Each section tells the team what to discuss and which item IDs to look at

5. Focus the session on Top Issues
   - Share the Top Issues table with the team before the meeting
   - Ask each item owner to come prepared with context

**Expected result:**

You receive a Grooming Report with:
- **Scorecard:** exact counts for each problem type (no estimates, no owners, stale, blocked)
- **Top Issues table:** the 10 items that most urgently need attention, ranked by flag count
- **Agenda:** organized by problem type — each topic lists affected items and a recommended action

The 90-minute grooming session focuses only on flagged items. The team skips items that are already clean, saving 20–30 minutes of meeting time.

**Why this works:** Instead of discovering problems live during the meeting (e.g., "wait, who owns this?"), the team arrives knowing exactly which items need discussion. The session becomes a decision meeting, not an audit.

---

### Scenario 2: Backlog Audit After a Sprint

**Situation:**
You are a Scrum Master. The sprint just ended and your team's backlog has grown to 40 items — a mix of carryover, new requests, and items that were added months ago and never touched. You want to identify what should be archived, re-estimated, or re-prioritized before planning the next sprint.

**What to do:**

1. Export the full backlog from your task manager as CSV
   - Make sure to include the "Last Updated" or "Modified" column — the skill needs it for staleness detection

2. Say: "Review backlog issues" or "Flag problems in my backlog"
   - Paste the CSV content
   - The skill will flag items with no activity in the past 14+ days as STALE

3. Focus on the Stale and Blocked sections of the agenda
   - Items flagged STALE haven't been touched in 14+ days → decide: keep, archive, or delete
   - Items flagged BLOCKED_NO_ETA are stuck without a resolution date → schedule unblocking

4. Use the Skipped Checks section to understand what wasn't verified
   - If you're missing the "Last Updated" column, the STALE check is skipped
   - Add that column to your next export for a more complete audit

**Expected result:**

You receive a report showing:
- Which items have been dormant for 14+ days (candidates for archiving)
- Which items are blocked without a clear path forward
- A clean list of action items for the backlog clean-up conversation

The team archives stale items, resolves blockers, and enters the next sprint planning with a lean, actionable backlog.

**Why this works:** Stale and blocked items are the #1 source of backlog bloat. By flagging them systematically rather than doing a manual scroll-through, you save time and ensure nothing gets missed.

---

### Scenario 3: Detecting Priority Inflation

**Situation:**
You are a Team Lead who noticed that the team's backlog "always feels urgent." Almost every item is labeled High or Critical. You want to surface this pattern and bring it to the grooming meeting as a structured conversation rather than a vague complaint.

**What to do:**

1. Export the backlog with at least a Priority column
   - CSV works best; include Title, Priority, Owner, Status

2. Say: "Help me prepare grooming agenda" and paste the CSV
   - The skill checks if more than 50% of items are High or Critical priority
   - If yes, it flags `ALL_HIGH_PRIORITY` and adds a re-prioritization item to the agenda

3. Present the Scorecard at the start of grooming
   - Show the "Priority inflation: YES (X% High/Critical)" line
   - Use it to open the conversation: "We have N items flagged as High — let's stack-rank them"

4. Use the Agenda's re-prioritization section to facilitate the discussion
   - Work through the top items and ask: "If we can only do 3 of these, which 3?"
   - Downgrade items that don't meet the bar for High priority

**Expected result:**

The Scorecard shows the exact percentage of High/Critical items (e.g., "68% of backlog is High priority"). The Grooming Agenda includes a dedicated re-prioritization topic with a suggested action.

The grooming session ends with a re-balanced backlog where High truly means High, giving the team clarity on what to focus on in the next sprint.

**Why this works:** Priority inflation is easy to feel but hard to prove. The scorecard gives you the data to have the conversation — "68% of our backlog is High priority" is more persuasive than "everything feels urgent."

---

## Tips

### Tip 1: Always Include "Last Updated" for Better Staleness Detection

The STALE flag only works if your export includes a date column (e.g., "Last Updated", "Modified", "Updated At"). If this column is missing, staleness checks are skipped and noted in the report. Before exporting, verify that the date column is included — it's one of the most actionable flags for backlog clean-up.

**Pro tip:** In Jira, add "Updated" to your CSV export columns. In Linear, use the "Last Activity" field.

### Tip 2: For Large Backlogs (100+ Items), Filter by Active Status First

If your backlog has 100+ items, export only the active items (exclude Done/Closed/Archived). This keeps the report focused on what matters. The skill handles large backlogs (showing top 10 issues), but a pre-filtered export gives you more precise results per topic.

**Pro tip:** Add a filter in Jira: `status != Done AND status != Closed` before exporting.

### Tip 3: Share the Top Issues Table Before the Meeting

Copy the Top Issues table from the report and paste it into the meeting invite or a shared document 24 hours before the grooming session. Ask item owners to come prepared with context on their flagged items. This turns the meeting from "let's figure out what's wrong" into "let's decide what to do."

**Pro tip:** Include the Scorecard summary line ("18 flagged items (30%)") in the meeting invite subject line to set the right expectations before anyone arrives.

---

**Version:** 1.0.0  
**Last updated:** 2026-05-13
