> [Версия на русском языке](README.ru.md)

# KPI Digest Builder

Turn your KPI files into a structured weekly snapshot — with deltas and a plain-language summary.

---

## Overview

KPI Digest Builder reads numeric metrics from your local files (.md, .txt, .csv) and assembles a weekly KPI snapshot table showing each metric's previous value, current value, delta, and trend arrow. It then writes a 2–3 sentence plain-language summary of the most significant movements. Use this skill when you need to consolidate scattered metrics into a weekly report, track week-over-week changes across multiple files, or prepare a status update for leadership without copying numbers manually.

---

## Requirements

- One or more local files containing KPI data: `.md`, `.txt`, or `.csv` format
  - Examples: a weekly metrics tracker, a CSV export from a dashboard, a markdown notes file with metric summaries
  - For delta calculation: two files (current week and previous week) or a single file with two date sections / a "last week" column
- No additional tools, plugins, or integrations required

**Works best when:** KPI names are consistent across current and previous files (e.g., "Revenue" matches "Revenue", not "Monthly Revenue").

---

## How to Use

1. **Prepare your KPI files**
   - Gather your metrics file(s) in your Cowork workspace folder
   - For delta: have a file for this week and a file for last week (or a single file with both periods)

2. **Trigger the skill**
   - Say: "Build KPI digest" or "Weekly KPI snapshot"
   - In Russian: "Собери KPI дайджест" or "Еженедельный снапшот KPI"
   - Point to your files if needed: "Build KPI digest from metrics.md and metrics-prev.md"

3. **Receive your digest**
   - Get a KPI snapshot table with Previous, Current, Δ, Δ%, and Trend columns
   - Review the plain-language Summary (2–3 sentences on key movements)
   - Check Notes for any assumptions or flags (missing data, format conversions, conflicts)

4. **Use the output**
   - Paste the digest into your weekly report, Slack status, or stakeholder email
   - Share the Summary paragraph directly with leadership

---

## Examples

### Example 1: Weekly metrics from two markdown files

**Input:**
```
File: metrics-this-week.md
- Revenue: 45,000
- Active Users: 1,150
- Support Tickets: 87
- Churn Rate: 3.2%

File: metrics-last-week.md
- Revenue: 40,000
- Active Users: 1,200
- Support Tickets: 87
- Churn Rate: 3.5%
```

**Action:** Skill reads both files, matches KPI names, normalizes values, calculates deltas.

**Output:**
```markdown
## KPI Digest — Week of 2026-05-05

| KPI | Previous | Current | Δ | Δ% | Trend |
|-----|----------|---------|---|----|-------|
| Revenue | 40,000 | 45,000 | +5,000 | +12.5% | ↑ |
| Active Users | 1,200 | 1,150 | -50 | -4.2% | ↓ |
| Support Tickets | 87 | 87 | 0 | 0% | → |
| Churn Rate | 3.5% | 3.2% | -0.3 | -8.6% | ↓ |

### Summary
Revenue grew 12.5% week-over-week, the strongest positive movement this week. Churn rate improved slightly, down 0.3 points. Active users declined by 50 — worth monitoring if the trend continues next week.
```

---

### Example 2: Single CSV file with current and previous columns

**Input:**
```
KPI,Last Week,This Week
MRR,$38,000,$41,500
DAU,9,200,9,800
NPS,42,45
Bug Backlog,134,118
```

**Action:** Skill reads the CSV, maps "Last Week" → Previous and "This Week" → Current, normalizes values ($, commas stripped).

**Output:**
```markdown
## KPI Digest — Week of 2026-05-05

| KPI | Previous | Current | Δ | Δ% | Trend |
|-----|----------|---------|---|----|-------|
| MRR | 38,000 | 41,500 | +3,500 | +9.2% | ↑ |
| DAU | 9,200 | 9,800 | +600 | +6.5% | ↑ |
| NPS | 42 | 45 | +3 | +7.1% | ↑ |
| Bug Backlog | 134 | 118 | -16 | -11.9% | ↓ |

### Summary
All four tracked metrics moved in a positive direction this week. MRR grew 9.2% and bug backlog shrank by 12% — a strong week overall. NPS uptick (+3 points) is worth highlighting in the leadership update.

### Notes
- MRR values normalized from '$38,000' and '$41,500' (currency symbol removed)
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Build KPI digest | Собери KPI дайджест |
| Weekly KPI snapshot | Еженедельный снапшот KPI |
| Show me my KPIs this week | Покажи мои метрики за неделю |
| Compile my metrics into a weekly summary | Сформируй еженедельный дайджест из файлов с метриками |

---

> **See also:** [User Guide](docs/USER-GUIDE.md) · [Руководство пользователя](docs/USER-GUIDE.ru.md)

**Version:** 1.0.0
