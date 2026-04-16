# Hiring Pipeline Reviewer User Guide

Learn how to use Hiring Pipeline Reviewer to transform your interview notes into a structured weekly candidate status report.

---

## Quick Start

Here's the fastest way to get your pipeline report:

1. Copy your interview notes from the past week (any format)
2. Say: "Review hiring pipeline" and paste the notes
3. Get back a candidate status table with flags and recommendations

**Result:** A structured report showing each candidate's stage, score, and next step — ready to share or act on.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Preparing for Weekly Recruiter Sync

**Situation:**

You are a hiring manager preparing for your Friday sync with the recruiter. Over the past week, your team interviewed 4 candidates across different stages. Notes are scattered across your notes app — some detailed, some just a few lines. You need a single-page status to walk through with the recruiter and agree on next steps.

**What to do:**

1. Collect all interview notes from the week
   - Open your notes app and gather everything from the past 7 days
   - Don't worry about formatting — paste even rough notes

2. Trigger the skill by saying: "Hiring pipeline status"
   - Add the position title if you're hiring for multiple roles: "Hiring pipeline status for the Senior Product Designer role"
   - Paste or upload your notes

3. Review the Candidate Table
   - Check each candidate's current stage and last action date
   - Look for `⚠ stuck` flags — these are candidates you need to address today

4. Use the Recommendations section in your recruiter sync
   - Share your screen and walk through each recommendation
   - The "Decision needed" items become your agenda discussion points

**Expected result:**

You receive a one-page report with:
- Candidate Table (stage, score, next step, flags for all 4 candidates)
- Flags section (any stuck or incomplete candidates highlighted)
- Recommendations (advance / decline / decision needed for each person)

You walk into the recruiter sync prepared, decisions made, with a clear agenda for the 30-minute call.

**Why this works:** Instead of scrambling through scattered notes during the sync, you arrive with a clear view of the pipeline. The recruiter gets actionable direction, not a status update meeting.

---

### Scenario 2: Making a Go/No-Go Decision After Final Interviews

**Situation:**

You are a team lead who just completed a full interview loop for a backend engineer role. Three interviewers submitted separate evaluation notes in a shared document. The notes use different formats and one interviewer used a 1–5 scale while another used text comments only. You need to consolidate the picture before making a hiring decision and sending it to HR.

**What to do:**

1. Copy all three evaluation sheets from the shared document
   - Include reviewer names if available (helps the skill attribute concerns correctly)
   - Paste all three notes as one block

2. Trigger the skill by saying: "Summarize candidates — backend engineer final round"
   - The skill will merge multiple reviewer notes into a single record per candidate

3. Check the consolidated record
   - The score field shows the available score or a qualitative summary
   - Key strengths and concerns are merged from all reviewers
   - Look for conflicting signals across reviewers in the Notes/Concerns field

4. Generate a decision
   - Use the Recommendations section as the basis for your decision memo
   - If the team is split, the skill flags "Decision needed" — schedule a 30-minute debrief

**Expected result:**

You receive a clean, consolidated record for each candidate with merged reviewer notes. The Recommendations section gives you a starting point for the decision memo to HR.

**Why this works:** Instead of manually comparing three different evaluation sheets, you get a unified view in seconds. Split opinions are surfaced automatically, so you know exactly where to focus the debrief conversation.

---

### Scenario 3: Catching Up After Time Away

**Situation:**

You are a director who returned from a two-week vacation. Multiple roles were in progress during your absence, and the recruiting coordinator left you a 3-page document of interview notes from the past two weeks. You need to quickly understand where each candidate stands and who requires an urgent decision before candidates lose interest.

**What to do:**

1. Open the recruiter's status document and copy all notes
   - The notes cover multiple positions and multiple candidates

2. Trigger the skill: "Review hiring pipeline — catch-up after 2 weeks"
   - Mention the date range if helpful: "Notes from April 2–16"
   - The skill will group candidates and flag anyone who has been inactive

3. Focus on the Flags section first
   - `⚠ stuck` candidates are at highest risk of dropping out
   - Sort your action list by urgency: stuck candidates first, then "decision needed"

4. Send targeted follow-ups
   - For stuck candidates: contact the recruiter about scheduling the next step
   - For "advance" candidates: approve the next action immediately
   - For "decline" candidates: send the recruiter the list to initiate rejections

**Expected result:**

You receive a full pipeline view for all active candidates with clear flags showing who needs urgent attention. The skill identifies which candidates are at risk of going cold and which decisions can be made immediately.

**Why this works:** Rather than reading 3 pages of notes and trying to build a mental model, you get a prioritized action list within minutes. High-urgency situations (stuck candidates at offer stage, for example) are surfaced immediately.

---

## Tips

### Tip 1: Label Candidates Clearly in Your Notes

The skill can parse unlabeled notes, but it works best when each candidate section starts with their name. Even a simple "**Alex Chen:**" before each block significantly improves accuracy. If you use initials only (e.g., "A.C."), the skill will flag ambiguity — you'll save time resolving it upfront.

**Pro tip:** If you're using a shared notes doc, create a simple template: "Candidate: [Name] | Stage: [stage] | Date: [date]" at the top of each section. The skill reads this instantly.

### Tip 2: Specify Your Hiring Criteria for Better Recommendations

By default, the skill uses your notes to infer what matters for the role. For sharper recommendations, add a line like: "We're hiring a senior PM, must-haves: technical depth, cross-functional experience, data literacy." This helps the skill identify mismatches explicitly rather than just surfacing concerns.

**Pro tip:** Add criteria directly in your trigger phrase: "Review hiring pipeline for Senior PM — must-haves: technical depth, data literacy, 5+ years XFN experience."

### Tip 3: Use the "Stuck" Flag as Your Priority Queue

The `⚠ stuck` flag is your most actionable signal. Candidates stuck at offer stage are highest risk — they may accept a competitor's offer while you deliberate. Sort your weekly action list by flag type: stuck offers first, then stuck post-final-interview, then earlier-stage stuck candidates.

**Pro tip:** If you want a shorter stuck threshold (e.g., 3 days for offer-stage candidates), mention it in your prompt: "Flag anyone at offer stage who's been inactive for 3+ days."

---

**Version:** 1.0.0  
**Last updated:** 2026-04-16
