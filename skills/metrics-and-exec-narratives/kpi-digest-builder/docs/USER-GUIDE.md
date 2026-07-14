# KPI Digest Builder — User Guide

Learn how to use KPI Digest Builder to turn your metric files into a structured weekly snapshot.

---

## Quick Start

Here's the fastest way to get a KPI digest:

1. Put your metrics file (or two files — current and previous week) in your Cowork workspace folder
2. Say: "Build KPI digest" — or point to specific files: "Build KPI digest from metrics.md and metrics-prev.md"
3. Get a KPI snapshot table with delta and trend, plus a 2–3 sentence summary

**Result:** A ready-to-paste weekly KPI digest with Previous / Current / Δ / Δ% / Trend for every metric.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Weekly Status Report for Leadership

**Situation:**
You are a product manager who tracks 6–8 metrics every week (revenue, active users, churn, NPS, support tickets). You keep a simple markdown file where you paste numbers at the end of each week. Every Monday you need to send a "last week metrics" update to leadership — currently you're copying numbers and calculating deltas manually in your head.

**What to do:**

1. Keep two markdown files in your workspace:
   - `metrics-current.md` — this week's numbers
   - `metrics-previous.md` — last week's numbers (or rename last week's file)
   - Format can be simple: `- Revenue: 45,000` or a markdown table

2. Trigger the skill by saying: "Build KPI digest from metrics-current.md and metrics-previous.md"
   - Claude reads both files, matches metric names, and calculates deltas automatically

3. Review the output
   - Check the KPI table for any unexpected movements
   - Read the Summary — it highlights the 2–3 biggest changes in plain language
   - Check Notes for any flags (e.g., a metric name mismatch between files)

4. Copy the output into your leadership email or Slack message
   - Paste the full table for detail-oriented readers
   - Paste the Summary paragraph alone for executives who want the short version

**Expected result:**

You receive a formatted KPI table showing all your metrics with calculated deltas — zero arithmetic on your end. The Summary gives you a ready-made paragraph for the "highlights" section of your report. What used to take 10–15 minutes of manual work takes 2 minutes.

**Why this works:** You maintain your existing metric files in whatever format you already use. The skill adapts to your format, not the other way around.

---

### Scenario 2: Snapshot from a CSV Dashboard Export

**Situation:**
You are an operations lead. Every Friday, your analytics tool (Amplitude, GA, or a custom report) lets you export a CSV with this week's KPIs next to last week's values. You need to turn this raw CSV into a readable digest to share with your team lead by EOD.

**What to do:**

1. Export the CSV from your dashboard and place it in the Cowork folder
   - The CSV should have a column for KPI names and two value columns (e.g., "Last Week" and "This Week")
   - Column headers don't need to be exact — the skill infers current vs. previous from context

2. Say: "Weekly KPI snapshot from export.csv"
   - Claude reads the CSV, maps the columns, normalizes values (strips $, %, commas)
   - Calculates deltas for all rows

3. Review the digest
   - The Notes section will list any format normalizations (e.g., "$38,000" → "38000")
   - If a KPI had a 0 value in the previous week, delta % will be marked "—" to avoid division-by-zero

4. Share the digest
   - Forward the markdown output to your team lead or paste into your weekly ops report
   - Use the trend arrows (↑ ↓ →) for a quick visual scan in Slack

**Expected result:**

You receive a clean KPI table built directly from the CSV — with delta and trend for every row. Metrics are labeled exactly as in the export (column headers preserved). Any edge cases (zero values, format quirks) are flagged in Notes so you know what to double-check.

**Why this works:** You don't need to clean the CSV or build formulas. The skill reads it directly and handles normalization — you just paste the result.

---

### Scenario 3: Tracking a Single File with Two Time Periods

**Situation:**
You are a team lead who maintains one rolling metrics document. Every week you add a new section with the current week's data, keeping the previous week's section above it. You want a digest without creating separate files each week.

**What to do:**

1. Keep your rolling file structured with clear date sections:
   ```
   ## Week of 2026-04-28
   - Revenue: 40,000
   - DAU: 9,200

   ## Week of 2026-05-05
   - Revenue: 45,000
   - DAU: 9,800
   ```

2. Say: "Build KPI digest from my-metrics.md"
   - Claude identifies the two most recent date sections
   - Uses the more recent one as Current and the older one as Previous

3. If the file has more than two sections, Claude uses only the two most recent ones and notes this in the Summary

**Expected result:**

A digest built from a single file — no need to maintain two separate files. The skill infers which section is current and which is previous based on dates. You maintain one document; the digest handles the comparison automatically.

**Why this works:** The skill adapts to your existing file structure, including single-file rolling trackers.

---

## Tips

### Tip 1: Keep KPI Names Consistent Across Files

The skill matches metrics between "current" and "previous" by name. If you call a metric "Revenue" one week and "Monthly Revenue" the next, the skill won't match them and will list them as separate rows. Use the same name every week — even a minor difference causes a split.

**Pro tip:** If you spot two rows that look like the same metric with different names, the Notes section will flag them as a possible duplicate. Use that as a signal to standardize your naming.

### Tip 2: Any Format Works — Keep It Consistent

The skill reads bullet lists, markdown tables, and CSV exports. It doesn't require a specific format. What matters is consistency: use the same structure from week to week so that the metric names and positions match. A simple bullet list (`- Revenue: 45,000`) works just as well as a full markdown table.

### Tip 3: Use the Summary Paragraph Directly in Reports

The 2–3 sentence Summary is written in plain business language — it's designed to be copy-pasted as the "highlights" section of a report or leadership email without editing. If you find the summary is missing a key metric you care about, mention it in your trigger: "Build KPI digest from metrics.md — pay attention to NPS movement." The skill will weight that metric in the summary.

---

**Version:** 1.0.0
