# User Guide — Content Performance Reporter

## What This Skill Does

Content Performance Reporter reads your weekly analytics CSV exports and turns them into a structured narrative: which content performed best, which underperformed, what pattern emerged, and what to prioritize next week.

You get an editorial report — not a spreadsheet, not a dashboard. Claude does the sorting, aggregating, and interpreting so you can focus on decisions.

---

## Step-by-Step Guide

### 1. Export your analytics data as CSV

Each platform has its own export flow:

- **YouTube:** YouTube Studio → Analytics → Export icon (top right) → CSV
- **Google Analytics:** Reports → select date range → Download → CSV
- **LinkedIn:** LinkedIn Analytics → Export (top right) → Posts export
- **TikTok:** TikTok Business Center → Analytics → Download
- **Twitter/X:** Analytics.twitter.com → Tweets tab → Export data

### 2. Upload the file to Cowork

Drag and drop your CSV file into the Cowork chat, or confirm it's already in your selected workspace folder.

### 3. Trigger the skill

Type one of these phrases:
- "content performance report"
- "what worked this week"
- "compile my analytics"

Or in Russian:
- «отчёт по контенту»
- «что сработало на этой неделе»
- «скомпилируй аналитику»

### 4. Review the report

Claude returns a structured report:

- **Metrics table** — total reach/views, average engagement rate, comparison to last week (if previous data is available)
- **Top 3 Posts** — highest-performing content with key metrics
- **Bottom 3 Posts** — lowest-performing content
- **What Worked** — specific findings with numbers
- **What Didn't Work** — specific findings with numbers
- **Pattern of the Week** — the common thread among top performers
- **Recommendation for Next Week** — 1–2 concrete actions

---

## Tips

**Run multiple platforms at once.** Upload Instagram, YouTube, and GA4 CSV files together — Claude generates a separate section for each platform plus a combined summary.

**Compare two weeks.** If your platform exports comparison data in a single file (this week vs. last week columns), Claude will calculate the delta automatically. If you have two separate weekly files, upload both and mention which is current: "use file A as this week, file B as last week."

**No content column? That's fine.** If your CSV doesn't have a title or post name column (some raw GA4 exports), Claude uses row numbers as identifiers and flags it in Notes.

**Too much data?** For files with over 1,000 rows, Claude analyzes all rows for aggregate metrics but limits Top/Bottom selection to the top 100 by primary metric (noted in the report).

---

## Frequently Asked Questions

**Q: My CSV has an unusual format — will it work?**
Claude can read most standard CSV exports. If the file has no numeric metric columns, it will be skipped with a note. If the platform isn't recognized, Claude uses generic mode (first numeric columns as metrics).

**Q: Can I get a chart?**
Not in this mode — Claude doesn't generate visual charts. Paste the metrics table into Google Sheets or Excel to create visuals.

**Q: What if I don't have last week's data?**
Claude builds the report with current-week data only and skips the delta column. No comparison numbers are invented.

**Q: Can I save the report to a file?**
Yes — just ask: "save the report as a file." Claude will write it as a markdown document to your workspace.

**Q: Will it change my original CSV?**
No. The skill reads files only — it never writes to or overwrites your source data.
