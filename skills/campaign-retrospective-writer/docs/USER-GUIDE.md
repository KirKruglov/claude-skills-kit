# Campaign Retrospective Writer — User Guide

Learn how to turn raw campaign data into a structured marketing debrief using Campaign Retrospective Writer.

---

## Quick Start

Here's the fastest way to get a retrospective:

1. Finish your campaign and collect any metrics or notes you have
2. Say: `write campaign retrospective` and paste your data
3. Get back a six-section Markdown debrief with goal vs. result, channel breakdown, what worked/didn't, recommendations, and a trend line

**Result:** A structured, shareable document ready to send to your team or leadership.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Wrapping Up an Email Campaign for the Team

**Situation:**
You are a marketing manager. Your quarterly newsletter campaign just ended. You have the numbers from your email platform (open rate, CTR, unsubscribes) and a few notes from the A/B test you ran on subject lines. You need to send a quick debrief to the team before the next campaign starts.

**What to do:**

1. Open your email platform and copy the campaign metrics
   - Include: open rate, CTR, unsubscribe rate, list size
   - Add any A/B test results and qualitative observations in plain text below

2. Trigger the skill by saying: `write campaign retrospective`
   - Paste your metrics and notes
   - If you forgot to mention the goal or period, the skill will ask in one short prompt

3. Review the output
   - Check the **Goal vs. Result** table — does it correctly reflect your target vs. actual?
   - Read through **What Worked / What Didn't** — confirm the hypotheses match your intuition
   - Edit the **Trend Line** to match your internal naming convention

4. Share with the team
   - Copy the Markdown into Notion, Confluence, or a Slack message
   - The **Recommendations** section gives your team an immediate action list for the next campaign

**Expected result:**

You receive a clean six-section debrief showing performance against goal, channel verdict, hypothesis-backed analysis, and a one-line trend entry. Your team has clear takeaways in under 5 minutes without a single slide or spreadsheet.

**Why this works:** Instead of writing a debrief from scratch (30–60 min), you paste raw data and get a structured document instantly. Hypotheses are labelled so the team knows what's confirmed vs. what's a best guess.

---

### Scenario 2: Reviewing a Paid Campaign Before Planning the Next One

**Situation:**
You are a growth lead at a startup. Your paid acquisition campaign (Facebook + Instagram) just ended. You have CPL, lead volume, creative performance notes, and budget spend. In two days you have a planning meeting to decide whether to scale this channel. You need a concise retrospective to bring to the meeting.

**What to do:**

1. Gather your campaign data
   - Pull CPL, lead volume, budget spent from your ads manager
   - Note which creatives performed best and which underperformed
   - Add any contextual notes (audience fatigue, seasonal effects, landing page issues)

2. Say: `campaign debrief` and paste everything
   - Dump all the data at once — the skill handles unstructured input
   - Include your stated goal (e.g., "500 leads at CPL ≤ $20")

3. Review the **Channel Breakdown** and **Recommendations** sections
   - The ✅/❌ verdict per channel gives you immediate signal on what to scale or cut
   - The **Repeat / Adjust / Drop** framework maps directly to budget reallocation decisions

4. Bring the retrospective to the planning meeting
   - Share the document link or paste the **Goal vs. Result** table into your planning deck
   - Use the **Trend Line** as the single line in your "Campaign History" tracker

**Expected result:**

You get a decision-ready retrospective with clear channel verdicts and actionable recommendations. The planning meeting has a shared starting point — no conflicting interpretations of the data.

**Why this works:** The **Recommendations** section structures the "what should we do next" conversation before the meeting starts, saving 20+ minutes of discussion.

---

### Scenario 3: Building a Campaign Archive for the Quarter

**Situation:**
You are a content lead. Three campaigns ran in Q2 (an email series, a LinkedIn organic push, and a webinar). You want to create a lightweight archive of learnings before Q3 planning. You have scattered notes in Slack, a spreadsheet with numbers, and vague memories of what felt right.

**What to do:**

1. Run the skill three times — once per campaign
   - For each, paste whatever you have: Slack snippets, spreadsheet rows, or just a sentence summary
   - The skill works with partial data; it marks missing fields as «н/д» / «n/a»

2. Use the **Trend Line** from each retrospective
   - Collect the three Trend Lines into a single "Q2 Campaign Summary" note
   - Example archive entry:
     ```
     Email Q2: CTR 2.4%, +0.4pp vs. goal — subject line A/B was the driver
     LinkedIn Q2: 12 leads, CPL $45 — organic underperforms; needs paid boost
     Webinar Q2: 180 registrants, 62% show rate — topic resonated; repeat format
     ```

3. Share the archive before Q3 planning
   - One page, three campaign summaries, clear pattern of what channels to invest in

**Expected result:**

Three structured retrospectives plus a one-page trend archive. Q3 planning starts with data, not guesswork.

**Why this works:** The Trend Line is designed for exactly this use case — one line per campaign that stays scannable as the archive grows.

---

## Tips

### Tip 1: Dump Everything — The Skill Handles Messy Input

You don't need to format your data before pasting. Raw numbers from a spreadsheet, a Slack thread recap, bullets from a post-mortem call — all of it works. The skill extracts what it can and marks anything missing as «н/д» / «n/a». A perfect retrospective from imperfect notes beats no retrospective.

### Tip 2: Label Your Hypotheses and Edit Them

The skill marks every cause-and-effect claim as a **(hypothesis)**. This is intentional — retrospectives often confuse correlation with causation. Review the hypotheses and edit any you can confirm with data (e.g., "A/B test result p < 0.05, confirmed") or dispute ("the dip was due to a platform outage, not creative fatigue"). The label becomes a quality signal for your team.

### Tip 3: Use the Trend Line as a Living Tracker

Copy the **Trend Line** from each retrospective into a single running document (Notion page, Confluence table, Google Doc). After 4–6 campaigns, patterns become visible: which channels consistently hit goal, where CPL is drifting, which content formats keep winning. The line is short enough that a full quarter fits in one screenful.

---

**Version:** 1.0.0  
**Last updated:** 2026-06-26
