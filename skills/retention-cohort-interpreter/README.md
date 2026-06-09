> [Версия на русском языке](README.ru.md)

# Retention Cohort Interpreter

Turn raw cohort retention tables into actionable plain-language diagnostics — no data tools required.

---

## Overview

Retention Cohort Interpreter analyzes cohort retention tables and produces a structured diagnosis: curve health assessment, key drop-off windows, industry benchmark comparison, root-cause hypotheses, and prioritized next steps. It translates retention percentages into plain language any stakeholder can act on. Use this skill when reviewing weekly or monthly retention data, preparing investor updates, running post-launch health checks, or diagnosing unexpected churn in a specific cohort.

---

## Requirements

- A cohort retention table pasted directly into the chat:
  - Accepted formats: CSV rows, markdown table, or space-separated numbers with headers
  - Rows = cohorts (signup week/month, acquisition channel, etc.)
  - Columns = time periods (D1, D7, D30 or Week 1, Week 4, etc.)
  - Values = retention % (0–100 or 0–1) or absolute user counts
- Optional: product type (mobile app / SaaS / marketplace / consumer), cohort definition, current focus (reduce churn / raise floor / improve D1)

**No file uploads needed** — paste the table directly. Works with any cohort table regardless of data source.

---

## How to Use

1. **Prepare your retention table**
   - Export from your analytics tool (Amplitude, Mixpanel, Looker, etc.) as a CSV or copy the table from a dashboard
   - Ensure rows are cohorts, columns are time periods, values are retention % or counts

2. **Trigger the skill by saying:**
   - "Analyze retention cohort" and paste the table
   - Or in Russian: "Проанализируй таблицу удержания"

3. **Optionally provide context**
   - Product type: "This is a B2B SaaS" or "Mobile consumer app"
   - Goal: "We want to improve D7 retention" or "Diagnosing a drop we saw in March cohort"

4. **Review the diagnosis**
   - Get curve health label (Healthy / Needs Work / Critical) with specific data points
   - See the primary churn window with 3 actionable hypotheses
   - Use the Recommended Next Steps to plan your investigation

---

## Examples

### Example 1: Mobile App — Diagnosing Poor Early Retention

**Input:**
```
Cohort  | D1  | D7  | D14 | D30
Jan W1  | 38% | 18% | 12% | 8%
Jan W2  | 41% | 20% | 13% | 9%
Feb W1  | 35% | 16% | 10% | 7%
Feb W2  | 39% | 19% | 12% | 8%
```

**Action:** Skill parses the table, detects mobile/daily-period pattern, computes drops (D1→D7 avg −21 pp as dominant window), compares to mobile app benchmarks.

**Output:**
```markdown
## Cohort Retention Diagnosis

**Product type:** Mobile / Consumer app (inferred from D1–D30 periods)
**Cohorts analyzed:** 4
**Periods covered:** D1–D30

### Curve Health: Needs Work

Average D7 retention (18%) is below the mobile app benchmark of 20–25%. The curve shows no sign of flattening by D30 (8%), suggesting the long-term floor has not been reached. No significant cohort-to-cohort improvement across January–February.

### Key Drop-off Points

| Period  | Avg Retention | Drop vs Previous | Severity |
|---------|---------------|------------------|----------|
| D1→D7   | 18%           | -21 pp           | High     |
| D7→D14  | 12%           | -7 pp            | Medium   |
| D14→D30 | 8%            | -4 pp            | Low      |

### Benchmark Comparison

- **Reference:** Mobile / Consumer app — typical D30 retention: 10–15%
- **Your curve:** At benchmark at D30: 8% (slightly below lower bound)
- D7 gap is the primary concern; D30 is borderline.

### Hypotheses for Primary Churn Window (D1→D7)

1. **Onboarding does not deliver core value in first session:** Users activate but don't reach the "aha moment" before Day 7, leading to high early abandonment.
2. **Push notification or re-engagement strategy is absent or ineffective:** No mechanism pulls users back after Day 1.
3. **Core use case requires habit formation not supported by app structure:** The product assumes daily use but lacks habit triggers (reminders, streaks, social cues).

### Recommended Next Steps

1. Instrument "aha moment" event (first key action); measure % of D1 users who reach it vs. D7 churners
2. Segment D1→D7 drop by acquisition source to check if one channel drives disproportionate churn
3. Review push notification opt-in rate and Day 2–6 campaign performance
```

---

### Example 2: B2B SaaS — Healthy Curve Validation

**Input:**
```
Cohort   | M1  | M2  | M3  | M6
Q1 2026  | 82% | 76% | 71% | 65%
Q4 2025  | 79% | 74% | 69% | 62%
Q3 2025  | 81% | 75% | 70% | 64%
```

**Action:** Skill detects B2B SaaS pattern (monthly periods, high retention), compares to B2B benchmarks, notes stable cohort-over-cohort trend.

**Output:**
```markdown
### Curve Health: Healthy

M3 retention (70%) meets the B2B SaaS benchmark of 65–70%. Curve is flattening between M3 and M6 (drop of only 6 pp), suggesting a durable long-term floor around 60–65%. Cohort performance is stable quarter-over-quarter — no regression detected.

### Hypotheses for Primary Churn Window (M1→M3)

1. **Seat consolidation after initial rollout:** Teams reduce seat count 1–2 months after onboarding once initial expansion phase ends.
2. **Champion departure in small accounts:** Loss of the internal champion drives cancellation before the product is embedded in workflows.
3. **Feature adoption plateau:** Users activate core features quickly but don't discover advanced capabilities that drive renewal commitment.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Analyze retention cohort | Проанализируй таблицу удержания |
| Interpret cohort table | Интерпретируй когортный анализ |
| What does my retention curve show | Что показывает кривая удержания |
| Diagnose retention drop | Диагностируй отвал по когортам |
| Cohort retention analysis | Анализ когортного удержания |

---

**Version:** 1.0.0
**Last updated:** 2026-06-03
