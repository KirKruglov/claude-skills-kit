# Retro Pattern Analyzer User Guide

Learn how to use Retro Pattern Analyzer to find what keeps coming up in your team's retrospectives — and finally do something about it.

---

## Quick Start

Here's the fastest way to get your first report:

1. Collect 3–5 retrospective `.md` or `.txt` files from recent sprints into one folder
2. Say: "Analyze retro files" and provide the folder path
3. Get back `retro-patterns-YYYY-MM-DD.md` with recurring pains, unresolved actions, and positive patterns

**Result:** A one-page report showing which problems keep coming back, which action items were never resolved, and what your team is consistently doing well.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Preparing for a Quarterly Retrospective

**Situation:**

You are a scrum master or engineering manager. Your team just finished Q1 (4 sprints). You're about to run the quarterly retrospective and want to open the conversation with data — not vibes. You need to know which problems persisted all quarter, which action items were raised but never closed, and what the team should stop debating and just fix.

**What to do:**

1. Collect your Q1 retro files
   - Find the 4 sprint retro notes (any format — Notion export, markdown, plain text)
   - Name them clearly: `retro-s1.md`, `retro-s2.md`, `retro-s3.md`, `retro-s4.md`
   - Place them in one folder

2. Trigger the skill by saying: "Analyze retro files" or "Retro pattern analysis"
   - Provide the folder path
   - Optionally add: "focus on team process issues"

3. Review the Recurring Pains block
   - Items marked `4/4` appeared every sprint — these are your highest-priority discussion topics
   - Items marked `↑ growing` are getting worse and need immediate attention
   - Items marked `↓ resolving` are improving — celebrate and note what changed

4. Prepare your retro opening
   - Copy the Recurring Pains table and paste it as the first slide or doc section
   - Lead with: "Here's what we saw repeating all quarter — let's decide what to actually fix today"

**Expected result:**

You receive a report showing, for example:
- "Slow deployment" appeared 4/4 sprints, trend `↑ growing`
- "Unclear QA ownership" appeared 2/4 sprints, trend `→ stable`
- "Automate pipeline" action item was raised in S1 and reappeared in S2, S3, S4 as a problem

You open the quarterly retro with concrete data instead of relying on memory. The team spends time solving the right problems rather than debating which ones exist.

**Why this works:** Teams tend to repeat the same retro complaints without tracking them across sprints. This report makes the pattern undeniable — and creates the urgency to actually close it.

---

### Scenario 2: Tracking Whether Last Sprint's Action Items Got Done

**Situation:**

You are a team lead. Two sprints ago, your team committed to 3 specific action items to improve how they handle code reviews. Now you want to know: were they actually implemented? Or are the same problems showing up again?

**What to do:**

1. Gather the last 3 sprint retro files
   - Include the sprint where the action items were created and the 2 sprints that followed
   - Any format works (even rough meeting notes)

2. Say: "Find recurring issues in retrospectives"
   - Provide the 3 files

3. Check the Unresolved Action Items block
   - Look for action items raised in sprint N that reappeared as problems in sprint N+1 or N+2
   - Each row shows: what the action was, when it was raised, and when it came back

4. Use the results in your next 1:1 or team check-in
   - For unresolved items: ask "What got in the way of closing this?"
   - For resolved items (they don't appear in Recurring Pains): recognize the improvement

**Expected result:**

You receive a clear list of action items with their follow-through status. For example:
- "Establish code review SLA" — raised in S5, reappeared in S6, S7 → unresolved
- "Add automated linting" — raised in S5, not in S6 or S7 pains → likely resolved

You have a data-backed conversation starter for your next team discussion. No need to rely on memory or re-read 3 sets of notes.

**Why this works:** Most teams forget their action items by the next sprint. The Unresolved Action Items block makes follow-through visible and specific.

---

### Scenario 3: Building a Team Health Report for Leadership

**Situation:**

You are a VP of Engineering or department head. You want to give your leadership team a concise view of team health trends across 6 sprints — not anecdotes, but patterns. You have retro notes from the past quarter but no structured way to summarize them.

**What to do:**

1. Collect 5–8 retro files from the past quarter
   - Ask your scrum masters to share their retro notes in `.md` or `.txt`
   - Normalize filenames with dates: `retro-2026-01-15.md`, `retro-2026-01-29.md`, etc.

2. Say: "Analyze our sprint retrospectives"
   - Provide the folder path or list of files

3. Review all three blocks of the report
   - **Recurring Pains:** What systemic issues exist? How long have they persisted?
   - **Unresolved Action Items:** What did the team commit to but not deliver?
   - **Stable Positive Patterns:** What is the team consistently doing well?

4. Present the report to leadership
   - Copy the three tables into your deck or shared doc
   - Add a narrative: "This quarter's top systemic issue was X, appearing in 5/6 sprints. Team committed to fixing it in sprint 3 but it reappeared. Proposed intervention: [your recommendation]."

**Expected result:**

A one-page summary of team health patterns — ready for a leadership deck or async update. You present data, not opinions, and can point to specific sprints where issues started or resolved.

**Why this works:** Leadership doesn't need to read retro notes. They need signals. This report gives them the right level of abstraction — persistent patterns, not one-off complaints.

---

## Tips

### Tip 1: Name Files with Dates for Automatic Ordering

The skill uses filenames to determine sprint chronology. If you name your files with dates — `retro-2026-03-15.md`, `retro-2026-03-29.md` — the skill automatically sorts them and shows trends accurately. If files aren't dated, add a date to the first line of each file (`Sprint date: 2026-03-15`).

**Pro tip:** Keep a consistent naming convention across your team. Even a simple `sprint-N-retro.md` scheme works as long as N is sequential.

### Tip 2: Don't Worry About Retro Format Consistency

Your team probably doesn't write retros in the same format every sprint. Some use "What went well / What went wrong", others use "Start-Stop-Continue" or "Plus-Delta". The skill normalizes all common formats. Just provide the files as-is.

**Pro tip:** If a file has no section headers at all (just raw notes), the skill will still process it using keyword detection — though results will be less precise. Adding minimal headers (even `# Problems` and `# Wins`) takes 30 seconds and significantly improves output quality.

### Tip 3: Use the Focus Area Filter for Targeted Analysis

If you only care about one category of issues — say, technical debt, team communication, or release process — add a focus phrase when triggering the skill: "Analyze retro files, focus on release and deployment themes." The skill will filter the report to only show themes matching that area. This is useful when presenting to a specific audience (e.g., technical lead vs. product manager).

**Pro tip:** Run the report twice — once unfiltered for the full picture, once with a focus area for your specific meeting. Two minutes, two different conversations.
