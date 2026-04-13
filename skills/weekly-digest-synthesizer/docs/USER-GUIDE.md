# Weekly Digest Synthesizer User Guide

Learn how to use Weekly Digest Synthesizer to compile team status files into a structured weekly report.

---

## Quick Start

Here's the fastest way to get a digest:

1. Put your `.md` or `.txt` status files into one folder
2. Say: "Compile weekly digest from [folder path]"
3. Get back a `weekly-digest-YYYY-MM-DD.md` file with all updates organized by project

**Result:** A structured digest with a summary, per-project status, action items table, and blockers.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Friday Status Rollup for a Team Lead

**Situation:**
You are a team lead managing three parallel workstreams. Each workstream owner drops a weekly status note into a shared folder every Friday. Your job is to compile these into a single digest to send to your director before the end of day. Manually reading and reformatting three files takes 20–30 minutes. You need it done in under 5.

**What to do:**

1. Confirm all status files are in your shared folder (e.g., `~/Documents/weekly-statuses/`)
   - Typical files: `alpha-status.md`, `beta-status.md`, `infra-status.md`
   - Files can be loosely structured — free-text notes work fine

2. Trigger the skill by saying: "Compile weekly digest from ~/Documents/weekly-statuses/"
   - The skill scans the folder and processes all `.md` and `.txt` files

3. Review the draft digest
   - Check the **Summary** section — confirm it reflects the week correctly
   - Scan the **Projects** section — verify statuses and action items are accurate
   - Check **Risks & Blockers** — confirm all active blockers are captured

4. Send the digest
   - Copy the content into your status email or forward the `.md` file directly
   - Optionally edit the Summary paragraph for tone before sending

**Expected result:**

You receive `weekly-digest-2026-04-13.md` with:
- A 3-sentence summary of the week
- Per-project sections with status icons (✅ / ⚠️ / 🔴), updates, and action items
- A cross-cutting action items table with owners and due dates
- A blockers list with source file references

You send this to your director in under 5 minutes.

**Why this works:** Instead of opening three files and manually reformatting their content, the skill aggregates and structures everything automatically. You only need to review, not build.

---

### Scenario 2: Manager Catching Up After a Week Away

**Situation:**
You are a product manager who was out for a week. Your team continued working and left notes in four different files. You need to understand what happened, what decisions were made, and what needs your attention — without reading hundreds of lines of notes scattered across files.

**What to do:**

1. Locate the weekly notes left by your team
   - Files might be named `product.md`, `design.md`, `backend-notes.md`, `qa.md`
   - Even unstructured notes work — the skill will extract what it can

2. Trigger the skill by saying: "Weekly digest" and provide the file paths or folder
   - Example: "Weekly digest from ~/team-notes/ for the week of April 7"

3. Read the digest top to bottom
   - **Summary:** 3–4 sentences to orient yourself after being away
   - **Projects:** Scan each project; look for ⚠️ or 🔴 status indicators
   - **Cross-Cutting Action Items:** See what needs follow-up and who owns each item
   - **Risks & Blockers:** Identify what needs your decision or unblocking

4. Take action on blockers
   - For items marked "TBD" (no owner): assign them in your follow-up
   - For blocked projects: schedule a quick sync with the relevant person

**Expected result:**

You receive a complete picture of the week in a single document. You identify:
- Which projects moved forward and which are at risk
- What decisions were made in your absence
- What tasks are waiting for an owner or a deadline

You're fully caught up in under 10 minutes.

**Why this works:** You don't need to read every file — the skill surfaces the most important items and flags gaps. Status icons and the blockers section tell you exactly where to focus.

---

### Scenario 3: Recurring Monday Morning Digest (Automated)

**Situation:**
You are an operations lead who wants a weekly digest every Monday morning without doing anything manually. Your team drops Friday status notes into a shared folder. You want this digest generated automatically.

**What to do:**

1. Set up a folder where team status files are dropped each week
   - Example: `~/Documents/Claude/weekly-notes/`

2. Create a scheduled task in Claude:
   - Say: "Create a weekly task that runs every Monday at 9 AM — compile weekly digest from ~/Documents/Claude/weekly-notes/ and save the output"
   - The skill will set up the automation using Claude's scheduling system

3. Each Monday, find your digest ready
   - `weekly-digest-YYYY-MM-DD.md` waiting in the working directory
   - Review and forward as needed

**Expected result:**

Your weekly digest appears every Monday morning without manual effort. You spend 5 minutes reviewing, not 30 minutes compiling.

**Why this works:** The skill is compatible with Cowork scheduled tasks, so it runs autonomously at your chosen time. The folder acts as the inbox; the digest is the output.

---

## Tips

### Tip 1: Add Explicit Status Keywords to Your Files

The skill detects status from keywords like "blocked", "at risk", "on track", "completed", "delayed", or emoji like ✅ and 🔴. If your files include these, the skill produces more structured output. A simple "Status: On track" line at the top of each file goes a long way.

**Pro tip:** Agree with your team on a consistent format. Even a single "## Status: blocked" line per file dramatically improves digest quality.

### Tip 2: Use One File Per Project for Best Grouping

The skill groups content by project name. If you combine multiple projects into one file, it will still work but may group them under the filename rather than project names. For the cleanest output, use one file per project or workstream.

**Pro tip:** Name files clearly: `project-alpha.md`, `design-sprint.md`, `hiring.md` — the filename becomes the project name if no H1 heading is found.

### Tip 3: Flag Blockers Explicitly for Better Surfacing

The skill surfaces blockers in its own section. To ensure blockers are detected, use clear language: "Blocker:", "Blocked by", "Waiting on", or "Dependency:". Implicit blockers (buried in a paragraph) may be missed.

**Pro tip:** If the digest's "Risks & Blockers" section is empty but you know there are blockers, check if the source files mention them explicitly. Add a "Blocker:" line and re-run.

---

**Version:** 1.0.0
**Last updated:** 2026-04-13
