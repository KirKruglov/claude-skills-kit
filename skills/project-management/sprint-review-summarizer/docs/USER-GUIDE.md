# Sprint Review Summarizer User Guide

Learn how to turn your sprint notes into a structured stakeholder document with zero setup.

---

## Quick Start

Here's the fastest way to get a sprint review document:

1. Write or copy your sprint notes (any format — bullets, paragraphs, or a mix)
2. Say: "Sprint review summary" and paste the notes
3. Get back a markdown document with all four sections plus an executive summary

**Result:** A structured, copy-paste-ready document you can send to stakeholders immediately.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Preparing for the Sprint Review Meeting

**Situation:**
You are a product manager and the sprint review meeting is in 30 minutes. You have rough notes from the past two weeks scattered across a few bullet points in your notebook. You need a clean stakeholder document to present — covering what the team shipped, what got pushed, and what's next — but you don't have time to format it manually.

**What to do:**

1. Gather your sprint notes
   - Open your notes app, PM tool, or wherever you tracked sprint progress
   - Copy everything relevant: shipped items, deferred items, blockers, next priorities

2. Trigger the skill by saying: "Sprint review summary"
   - Paste all your notes in one go — order doesn't matter
   - Include any context you have: sprint number, team name, dates

3. Review the generated document
   - Check the **Executive Summary** — does the completion metric match your expectation?
   - Verify items are in the right sections (Delivered vs. Deferred vs. Risks)
   - Add any missing details manually if needed

4. Use the document in your meeting
   - Share your screen and walk through the sections top-to-bottom
   - Use **Next Sprint Focus** to transition into the planning discussion

**Expected result:**

You receive a clean markdown document with all four sections, an executive summary ("6 of 8 items delivered; 2 deferred"), and any decisions your notes mentioned. You paste it into your meeting doc or slide and present in minutes.

**Why this works:** Instead of spending 20 minutes formatting notes into a table, you get a structured document in seconds. The meeting preparation time drops from 30 minutes to 5.

---

### Scenario 2: Sending the Weekly Stakeholder Update After Sprint Close

**Situation:**
You are a scrum master. The sprint closed yesterday. Leadership expects a written update by end of day explaining what the team accomplished, what was missed, and what's coming next. You have the team's end-of-sprint notes but they're in rough, unpolished form — not suitable for exec-level communication.

**What to do:**

1. Collect the sprint notes from your team
   - Ask each team member to share 2–3 bullet points on what they shipped and what they didn't
   - Combine all notes into a single text block

2. Say: "Summarize sprint results" or "Turn my sprint notes into a report"
   - Paste the combined notes
   - Include the sprint number and dates if you have them

3. Review and polish the output
   - The skill generates the four-section document automatically
   - Review the **Risks & Issues** section — is the language appropriate for exec audience?
   - Add any strategic context the skill couldn't infer from the notes

4. Send to stakeholders
   - Copy the markdown into your email client or Notion page
   - Send as the official sprint summary

**Expected result:**

You receive a document structured for exec consumption: a one-line summary at the top, clear sections, and a Next Sprint Focus that sets expectations. Leadership gets the context they need without reading raw team notes.

**Why this works:** The skill converts unpolished team notes into exec-ready language. You don't have to rewrite — just review and send.

---

### Scenario 3: Tracking Deferred Work Across Multiple Sprints

**Situation:**
You are a team lead and notice that the same items keep appearing in your sprint notes as "not done." You want to create a clean sprint review document that makes the deferred work and its reasons visible to management — without it looking like random failures.

**What to do:**

1. Write your sprint notes with explicit reasons for deferrals
   - Example: "Payment integration deferred — vendor API docs still missing"
   - Include blockers as separate bullet points under Risks

2. Say: "Create sprint stakeholder doc" and paste your notes
   - The skill will pick up the deferred items and their reasons automatically

3. Review the **Deferred** and **Risks & Issues** sections
   - Check that the reasons for deferral are captured clearly
   - Verify the **Next Sprint Focus** reflects the plan to address deferred items

4. Share with management
   - The document shows deferred items with reasons — making the pattern visible without blame
   - Use the **Risks & Issues** section to escalate blockers that need management action

**Expected result:**

You receive a document where deferred items appear with their context (why they were deferred), and risks are called out explicitly. Management sees a clear picture of what's blocking the team, not just a list of misses.

**Why this works:** Deferred work with reasons tells a story. The document turns blockers into escalation points rather than unexplained gaps.

---

## Tips

### Tip 1: Include Signal Words for Better Classification

The skill classifies items based on language signals. Using clear signal words produces more accurate results:
- For delivered items: "shipped", "done", "released", "fixed", "launched"
- For deferred: "pushed", "moved", "deferred", "carried over", "didn't make it"
- For risks: "blocked", "at risk", "dependency", "concern"
- For next sprint: "next sprint", "upcoming", "plan for", "priority"

**Pro tip:** If an item is misclassified, edit the source notes to include a clearer signal word and rerun the skill. It takes 30 seconds.

### Tip 2: Add Sprint Metadata for a Polished Header

If you include sprint number, team name, and dates anywhere in your notes, the skill will use them in the document header. Even a single line like "Sprint 24, May 5–19, Platform team" at the top of your notes produces a professional-looking header.

**Pro tip:** If you regularly run sprint reviews, create a notes template with the metadata line pre-filled. Copy it at the start of each sprint and update as you go.

### Tip 3: Use "None noted this sprint" Sections as a Health Signal

The skill always generates all four sections, even if some are empty. An empty **Deferred** section and an empty **Risks** section is a good signal — it means the sprint went smoothly. Conversely, if **Deferred** is full and **Delivered** is short, the document makes that visible at a glance.

**Pro tip:** Share the document with the team after each sprint. The four-section format creates a consistent baseline for retrospective discussions.

---

**Version:** 1.0.0
**Last updated:** 2026-05-15
