> [Версия на русском языке](README.ru.md)

# Weekly Metrics Story Writer

Turn dashboard numbers into a polished stakeholder narrative — email or Slack, ready to send in minutes.

---

## Overview

Weekly Metrics Story Writer takes raw metrics (pasted text, a table, or a `.md` file) plus a line of context and generates a copy-paste-ready weekly update for leadership or your team. It classifies each metric as a positive, negative, or neutral signal, prioritises the most important changes, and writes a narrative in plain language — no filler words, no blank-page struggle.

Use this skill every time you turn dashboard numbers into a written update: weekly OKR check-ins, product health reports, marketing performance emails, or team Slack digests.

---

## Requirements

- Metrics data in any text format: table, list, CSV lines, or plain prose with numbers
- Optional but recommended: a one-line note about what happened this week (launch, incident, experiment)
- No connectors, no database access, no code required

---

## How to Use

1. **Trigger the skill** — say "weekly metrics story" or paste your numbers directly
2. **Provide your metrics** — any format works; the skill parses it automatically
3. **Answer 1–2 quick questions** — audience (leadership / team) and format (email / Slack / both)
4. **Add context** — one line about notable events; skip if nothing happened
5. **Receive your narrative** — copy and send

---

## Examples

### Example 1: Leadership email from a paste

**Input:**
```
DAU: 48,200 (was 44,100)
7-day Retention: 34% (was 36%)
Revenue: $182k (was $175k)
Context: Launched onboarding redesign on Tuesday
Audience: leadership, email
```

**Output:**
```
Subject: Weekly Metrics Update — Week of May 26

DAU grew 9.3% to 48,200 following Tuesday's onboarding redesign, and revenue reached $182k (+4%). The early signal is positive — more users are activating. The one number to watch is 7-day Retention, which dipped from 36% to 34%; it's worth tracking whether the new cohort retains at the same rate by next week.

**Key Numbers**
• DAU: 48,200 (+9.3%) — onboarding redesign driving new activations
• Revenue: $182k (+4%) — in line with DAU growth
• 7-day Retention: 34% (–2pp) — slight decline; monitor new cohort

**What to Watch**
• Retention vs. new cohort: growth and retention are moving in opposite directions — confirm by day 14.

**Context**
Onboarding redesign launched Tuesday May 20.
```

---

### Example 2: Slack team digest

**Input:**
```
Signups: 1,240 (last week: 1,180)
Activation rate: 61% (last week: 58%)
Churn: 2.1% (last week: 2.0%)
Format: Slack, team
```

**Output:**
```
:bar_chart: *Weekly Metrics — May 26*

Solid week: signups and activation both up, churn holding steady.

*Highlights*
• Signups: 1,240 (+5.1%) — continued organic growth
• Activation rate: 61% (+3pp) — more users hitting the key action

*Watch This*
• Churn: 2.1% (+0.1pp) — marginal uptick; not alarming yet but worth watching

Any ideas on what's driving the activation improvement? 👆
```

---

## Triggers

| English | Russian |
|---------|---------|
| Weekly metrics story | Недельный нарратив по метрикам |
| Write metrics narrative | Напиши нарратив по метрикам |
| Metrics to email | Метрики в email |
| Turn numbers into story | Переведи цифры в текст |
| Write weekly report from dashboard | Напиши обновление по метрикам из дашборда |
| Metrics update for stakeholders | Обновление по метрикам для стейкхолдеров |

---

**Version:** 1.0.0  
**Last updated:** 2026-05-26
