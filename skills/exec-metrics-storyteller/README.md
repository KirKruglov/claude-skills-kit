# Exec Metrics Storyteller

Turn your metrics snapshot into a board-ready executive narrative — with revenue framing, LTV linkage, and strategic outlook — in one step.

---

## Overview

Exec Metrics Storyteller converts a raw metrics snapshot into a formal executive report for C-suite, board, or investor audiences. It structures your numbers into five sections — Headline KPIs, Executive Summary, Revenue & Unit Economics, Trend Analysis, and Next Period Outlook — with business interpretation for each metric. Use this skill when you need to prepare a board deck narrative, write a C-suite monthly review, or translate product KPIs into a revenue-linked story for leadership.

---

## Requirements

- A metrics snapshot in any format:
  - Paste/table: `| MAU | 120k | +12% MoM |`
  - Key-value list: `MAU: 120k (+12% MoM), ARR: $2.4M (+8% QoQ), Churn: 2.1%`
- Business context (optional but recommended):
  - Reporting period: monthly or quarterly
  - Audience type: board / C-suite / investors
  - Product stage: early / growth / scale
  - Targets or benchmarks (if you have them)
- No external tools, files, or integrations required

**Best results:** 5–15 KPIs covering growth, retention, and revenue metrics. Pure text with no numbers is not supported.

---

## How to Use

1. **Gather your metrics**
   - Copy your KPI table from your dashboard, spreadsheet, or weekly report
   - Note the reporting period (e.g., "May 2026, monthly") and audience (e.g., "board")

2. **Trigger the skill by saying:**
   - "Exec metrics report"
   - "Write executive metrics narrative"
   - "Turn my metrics into a board report"
   - In Russian: "Отчёт по метрикам для борда" or "Подготовь executive-отчёт по метрикам"

3. **Paste your metrics snapshot and context**
   - Include deltas (e.g., `+12% MoM`) where available — they enable Watch/Alert flags
   - Mention targets if you have them for more precise status labels

4. **Receive and use the report**
   - Get a structured markdown narrative with 5 sections, ready to paste
   - Use the Headline KPIs table for board slides
   - Use the Executive Summary for email subject or opening paragraph
   - Use Revenue & Unit Economics for the financial section of a board deck

---

## Examples

### Example 1: Monthly Board Report (Growth Stage)

**Input:**
```
Period: May 2026 (monthly), audience: board
MAU: 120k (+12% MoM), target 130k
ARR: $2.4M (+8% QoQ)
Churn: 2.1% (+0.3pp MoM)
CAC: $42 | LTV: $310
Activation rate: 38% (-4pp MoM)
```

**Output:**
```markdown
## Executive Metrics Report — May 2026 | Board

### Headline KPIs
| Metric | Value | Delta | Status |
|--------|-------|-------|--------|
| MAU | 120k | +12% MoM (vs. target 130k) | ⚠️ Watch |
| ARR | $2.4M | +8% QoQ | ✅ On track |
| Churn | 2.1% | +0.3pp MoM | ⚠️ Watch |
| LTV:CAC | 7.4x | — | ✅ On track |
| Activation rate | 38% | -4pp MoM | 🔴 Alert |

### Executive Summary
May delivered solid revenue growth (+8% QoQ), with ARR on track and unit economics remaining healthy at 7.4x LTV:CAC. Growth, however, is running below target: MAU reached 120k against a 130k goal, and activation rate dropped 4pp — a signal that new user onboarding may be limiting top-of-funnel conversion. Churn ticked up modestly, which warrants monitoring but is not yet structural. The strategic question for the board: is the activation gap an execution issue or a product-market fit signal?

### Revenue & Unit Economics
**ARR: $2.4M (+8% QoQ).** Revenue growth is healthy and compound trajectory is on plan. At current pace, the $10M ARR milestone is reachable within 5 quarters.

**LTV: $310 | CAC: $42 | LTV:CAC: 7.4x.** Unit economics are strong — a 7.4x ratio well above the 3x benchmark indicates efficient acquisition. Payback period is approximately 5 months.

### Trend Analysis
Notable shifts this month:
- Activation rate dropped 4pp MoM (**🔴 Alert**) — largest single-month decline this year
- Churn rose 0.3pp (**⚠️ Watch**) — second consecutive monthly increase

> **⚠️ Tension to address:** MAU is growing (+12% MoM) while activation rate and churn are moving in the wrong direction simultaneously. Two readings:
> 1. **Growth-led tension:** New user volume is outpacing onboarding capacity — a solvable execution problem.
> 2. **Fit signal:** Recent acquisition cohorts may be lower-quality — warrants cohort-level analysis before next board meeting.

### Next Period Outlook
June focus: stabilize activation rate above 40% through onboarding improvements and reduce churn to pre-April baseline. If activation recovers, MAU should reach 130k–135k by month-end. Key metrics to watch: activation rate by cohort week and churn by acquisition channel.
```

---

### Example 2: Quarterly C-Suite Review (Minimal Snapshot)

**Input:**
```
Q1 2026 review for C-suite.
Revenue: $1.8M (+22% YoY)
NPS: 61 (+5 pts)
Churn: 1.4%
```

**Output:**
```markdown
## Executive Metrics Report — Q1 2026 | C-Suite

> **Assumptions:** Period inferred as Q1 2026, audience C-suite as stated. Deltas vs. prior year or period used where provided.

### Headline KPIs
| Metric | Value | Delta | Status |
|--------|-------|-------|--------|
| Revenue | $1.8M | +22% YoY | ✅ On track |
| NPS | 61 | +5 pts | ✅ On track |
| Churn | 1.4% | — | ✅ On track |

> **Note:** Report based on limited metrics (3 KPIs) — add MAU, LTV, and CAC data for a complete executive picture.

### Executive Summary
Q1 2026 was a strong quarter: revenue grew 22% year-over-year and customer satisfaction (NPS 61) reached a new high. Churn at 1.4% indicates a stable, healthy customer base. With no major risk metrics flagged, the business is on a solid trajectory heading into Q2.

### Revenue & Unit Economics
**Revenue: $1.8M (+22% YoY).** Double-digit annual growth indicates strong product-market demand and effective go-to-market execution.

> [LTV/CAC not provided — add for full unit economics view]

### Trend Analysis
All three reported metrics are trending positively. No anomalies or contradictions flagged. NPS improvement (+5 pts) alongside revenue growth suggests satisfaction and monetization are moving together — a healthy signal.

### Next Period Outlook
Q2 focus: maintain NPS above 60 and sustain revenue growth pace. Recommend adding MAU and retention cohort data to Q2 reporting for a more complete picture ahead of mid-year review.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Exec metrics report | Отчёт по метрикам для борда |
| Write executive metrics narrative | Нарратив метрик для C-suite |
| Turn my metrics into a board report | Переведи метрики в отчёт для руководства |
| Prepare C-suite metrics story | Подготовь executive-отчёт по метрикам |
| Board metrics narrative | Метрики для борда |

---

**Version:** 1.0.0
**Last updated:** 2026-06-02

📘 [User Guide](docs/USER-GUIDE.md) · [Руководство пользователя](docs/USER-GUIDE.ru.md)
