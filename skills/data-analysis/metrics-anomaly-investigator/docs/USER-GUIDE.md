# Metrics Anomaly Investigator User Guide

Learn how to turn a confusing metric change into a structured investigation plan and a stakeholder narrative — without writing a single line of code.

---

## Quick Start

Here's the fastest way to get started:

1. Notice a metric drop or spike in your dashboard
2. Say: "Investigate metric anomaly: [metric name] [dropped/increased] [delta] [period]"
3. Add any context you have (recent releases, campaigns, experiments)
4. Get back a ranked hypothesis table + a draft Slack/email narrative

**Result:** A prioritised investigation checklist and a ready-to-paste stakeholder update.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Responding to an Unexpected Drop Before Your Weekly Review

**Situation:**
You are a product manager. It's Monday morning. You open your dashboard and see that weekly active users dropped 22% compared to last week. Your weekly leadership review is in 3 hours. You need to understand what might have caused this and have something to share with the team — even if the root cause isn't confirmed yet.

**What to do:**

1. Identify the key facts about the drop
   - Metric: weekly active users
   - Period: this week vs. last week
   - Delta: –22%
   - Context: check your memory — did anything launch last week? Any campaigns paused?

2. Trigger the skill by saying:
   - "Investigate metric anomaly: weekly active users dropped 22% this week vs. last week. We launched a new notification settings page on Thursday."
   - Include any context you have — even partial context helps prioritise hypotheses

3. Review the Investigation Framework table
   - Look at the "Likelihood" column — start with High-priority hypotheses
   - Read the "How to validate" column — these are your next actions for the next 2 hours

4. Copy the Draft Stakeholder Narrative
   - Paste it into your Slack channel or prep email before the review
   - Replace `[owner]` with the relevant team member's name
   - Add one sentence about your ETA for root cause confirmation

**Expected result:**

You receive:
- An **Anomaly Summary** confirming what happened
- An **Investigation Framework** with 5–7 ranked hypotheses (e.g., tracking issue on the new settings page, notification opt-out spike, feature flag rollout affecting activation)
- **Priority Checks** with 2–3 specific actions tied to your context (e.g., "check event logs on new notification settings page first — it's the most likely source of tracking regression")
- A **Draft Narrative** ready to paste into Slack: "We noticed WAU dropped 22% this week. We're investigating and the most likely causes are X and Y. [Owner] is checking Z now. Update by 2pm."

**Why this works:** You walk into the review with a structured plan, not a blank stare. Even without a root cause yet, you demonstrate that investigation is underway and you know where to look.

---

### Scenario 2: Investigating a Spike to Understand if It's Real

**Situation:**
You are a growth PM. Your activation rate spiked 40% last Tuesday and Wednesday, then returned to baseline. Your leadership team is excited and wants to replicate it. But you're not sure if it was real or a data glitch — and you don't want to make decisions based on bad data.

**What to do:**

1. Describe the anomaly with the full context you have
   - "Activation rate spiked 40% on Tuesday and Wednesday, then returned to normal. No product changes that week. We ran a Facebook ad campaign Tuesday–Wednesday targeting a new audience segment."

2. Trigger the skill:
   - "Investigate metric anomaly: activation rate spiked 40% Tuesday and Wednesday only, then returned to baseline."
   - The skill will include "Data/Tracking" hypotheses at the top since a two-day spike with quick reversion is a classic signal for data issues or traffic mix anomalies

3. Check the Axis column in the Investigation Framework
   - Look for "Data/Tracking" hypotheses first — these explain two-day spikes that vanish
   - Look for "External" axis — the Facebook campaign is a natural candidate
   - Look for "Behaviour" axis — a new audience segment may define "activated" differently

4. Use the Priority Checks section as your validation order
   - "Data/Tracking: check if activation event definition captures the new audience segment correctly" → validates whether the spike was real
   - "External: check activation rate segmented by acquisition source on Tuesday–Wednesday" → confirms if it was campaign-driven

**Expected result:**

You receive a framework that distinguishes "real spike" vs. "measurement artefact" scenarios. The Priority Checks tell you exactly how to verify: check event definitions for the new audience segment, then segment by acquisition source. You bring a clear answer to leadership: either "the Facebook campaign drove real activation among the new segment — here's how to replicate" or "the spike was a tracking artefact — here's what was miscounted."

**Why this works:** Without a structured framework, it's easy to over-celebrate a data artefact or under-investigate a real growth signal. The skill surfaces both possibilities and tells you how to distinguish them fast.

---

### Scenario 3: Writing a Stakeholder Update Before Root Cause is Found

**Situation:**
You are a team lead. A critical metric — paying conversion — dropped 12% three days ago. You have a hypothesis but haven't confirmed it yet. Your VP of Product and the CEO are asking for an update. You need to communicate clearly without overpromising.

**What to do:**

1. Share what you know so far
   - "Paying conversion dropped 12% over the past 3 days. We suspect a checkout flow change released Monday, but haven't confirmed. Payment error rate is normal. Mobile/desktop split looks even."

2. Trigger the skill and focus on the Draft Narrative section
   - "Investigate metric anomaly: paying conversion –12% over 3 days. Possible cause: checkout flow change Monday."

3. Customise the Draft Narrative
   - Fill in `[owner]` with the engineer running the investigation
   - Set a realistic ETA ("We expect initial findings by 6pm today")
   - Add one sentence on what's been ruled out ("Payment errors and tracking issues have been checked and ruled out")

4. Send the narrative
   - Post in your leadership Slack channel or email directly
   - Pin the message so it's easy to find for follow-up

**Expected result:**

A clean, professional 5–7 sentence narrative that communicates:
- What happened (paying conversion –12%, 3 days)
- What's being done (checkout flow regression investigation)
- What's been ruled out (payment errors, tracking issues)
- Next steps and ETA

Your VP and CEO have the context they need, and you've set a clear expectation for when the next update will come.

**Why this works:** Stakeholders don't need certainty — they need confidence that someone is on top of the situation. The structured narrative conveys exactly that, without requiring you to have a root cause first.

---

## Tips

### Tip 1: Always Include the Time Period and the Comparison Baseline

"Conversion dropped 15%" is less useful than "conversion dropped 15% week-over-week starting Monday." The time period helps the skill identify whether this is a sharp event (likely one cause) or a gradual trend (likely structural). Specifying the baseline (week-over-week, vs. 4-week average, vs. same period last year) also tells you whether seasonality is a candidate.

**Pro tip:** If you don't know the comparison baseline, say so — the skill will add seasonality and cohort-mix hypotheses to account for uncertainty.

### Tip 2: The Data/Tracking Axis Should Always Be Checked First

Even if you're confident you know the cause, always validate the data first. A tracking break can perfectly mimic a product regression or a user behaviour shift. The skill will always include Data/Tracking hypotheses at the top of the framework — treat them as mandatory first steps, not optional ones.

**Pro tip:** If the spike or drop is perfectly correlated with a product deploy, it's tempting to assume product cause immediately. But many deploys coincide with code changes that break analytics events. Check both simultaneously.

### Tip 3: Use the Draft Narrative as a Template, Not a Final Answer

The Draft Stakeholder Narrative is a starting point. Personalise it: add your team's specific context, replace `[owner]` with real names, and set a realistic ETA. A narrative that says "we expect an update by 3pm today" is far more trustworthy than one that says "we'll update soon."

**Pro tip:** If you're running the investigation with a cross-functional team, share the Investigation Framework table in your investigation Slack thread — it gives everyone a shared view of what's being checked and prevents duplicate work.

---

**Version:** 1.0.0
**Last updated:** 2026-05-25
