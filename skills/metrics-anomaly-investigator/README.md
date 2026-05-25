# Metrics Anomaly Investigator

Turn a confusing metric drop or spike into a structured investigation plan — in one message.

---

## Overview

Metrics Anomaly Investigator takes a plain-language description of an unexpected metric change and returns a ranked hypothesis framework plus a ready-to-paste stakeholder narrative. It covers four investigation axes — data/tracking issues, product changes, external factors, and user behaviour shifts — and prioritises hypotheses based on the context you provide. Use this skill when a dashboard number moves unexpectedly and you need to quickly figure out where to look, or when stakeholders are asking "what happened?" before you have an answer.

---

## Requirements

- A description of the anomaly (free-form text is fine):
  - Metric name (e.g., "weekly active users", "conversion rate", "Day-7 retention")
  - Time period and observed change (e.g., "dropped 23% week-over-week since Monday")
  - Any available context: recent releases, campaigns, experiments, external events (optional but improves hypothesis ranking)
- No files, tools, or external integrations required

---

## How to Use

1. **Notice an anomaly in your dashboard**
   - Identify the metric, the time period, and the magnitude of change

2. **Trigger the skill by saying:**
   - "Investigate metric anomaly: [your description]"
   - Or paste a message like: "Our Day-7 retention dropped 18% this week vs. last week — we shipped a new onboarding flow on Tuesday"
   - In Russian: "Расследуй аномалию метрики" or "У меня упала метрика"

3. **Provide context if you have it**
   - Recent product releases, A/B tests, marketing changes, or seasonality signals improve hypothesis ranking
   - No context? The skill proceeds with a full hypothesis set across all four axes

4. **Get your investigation plan**
   - Receive an Anomaly Summary, ranked Investigation Framework table, Priority Checks, and a Draft Stakeholder Narrative
   - Copy the narrative to Slack or email; work through Priority Checks with your team

---

## Examples

### Example 1: Sharp Drop with Context

**Input:**
```
Our checkout conversion rate dropped from 3.2% to 2.1% starting last Thursday. We deployed a new checkout page redesign on Wednesday evening. Mobile traffic is ~60% of our total.
```

**Output:**
```markdown
## Anomaly Summary
- Metric: Checkout conversion rate
- Period: Thursday onwards (vs. prior week)
- Change: -34% (3.2% → 2.1%)
- Type: drop — sharp — isolated
- Context provided: new checkout redesign deployed Wednesday evening; 60% mobile traffic

## Investigation Framework

| # | Hypothesis | Axis | Likelihood | How to validate |
|---|-----------|------|------------|-----------------|
| 1 | New checkout design has usability issue on mobile | Product | High | Split conversion rate by device type; compare mobile vs. desktop before/after deploy |
| 2 | Tracking pixel missing or broken on new checkout page | Data/Tracking | High | Check event firing in analytics debugger on new checkout URL |
| 3 | Payment provider error introduced by redesign | Product | Medium | Check payment error rate logs since Wednesday |
| 4 | A/B test traffic split causing segment skew | Product | Medium | Verify experiment assignment and conversion by variant |
| 5 | CSS/JS load issue on specific browsers | Product | Low | Check conversion by browser in analytics |

## Priority Checks

1. **Mobile usability issue** — Redesign deployed day before drop; 60% mobile share makes a mobile-specific regression the highest-probability cause.
2. **Tracking breakage** — New page URL or DOM changes commonly break analytics events; verify before drawing conclusions.
3. **Payment errors** — Any change to checkout flow can introduce payment flow regressions; check error rate logs.

## Draft Stakeholder Narrative

We noticed checkout conversion dropped from 3.2% to 2.1% (–34%) starting Thursday. This coincides with the checkout redesign deployed Wednesday evening. We are investigating two likely causes: a mobile usability regression and a potential tracking breakage on the new page. [Owner] is running device-split analysis and checking event logs now. We expect initial findings within 2 hours and will share an update by end of day. No action required from your side at this stage.
```

---

### Example 2: No Context Provided

**Input:**
```
Weekly active users dropped 15% this week. No idea why.
```

**Output:**
```markdown
## Anomaly Summary
- Metric: Weekly active users
- Period: Current week vs. prior week
- Change: -15%
- Type: drop — unknown shape — isolated
- Context provided: none — all four axes equally prioritised

## Investigation Framework

| # | Hypothesis | Axis | Likelihood | How to validate |
|---|-----------|------|------------|-----------------|
| 1 | Tracking or data pipeline issue | Data/Tracking | Medium | Compare raw event counts vs. processed WAU in analytics |
| 2 | Feature or experiment affecting activation | Product | Medium | Check if any A/B test or release went live this week |
| 3 | Traffic source drop (organic, paid, referral) | External | Medium | Check acquisition channel breakdown this week vs. last |
| 4 | Day-of-week or seasonal effect | Behaviour | Medium | Compare same week last year / 4 weeks ago |
| 5 | New user cohort size dropped | Behaviour | Medium | Split WAU into new vs. returning users |

## Priority Checks

1. **Tracking / data issue** — No context provided; always rule out data quality before investigating root cause.
2. **Traffic source change** — A 15% WAU drop often traces to an acquisition channel; check channel breakdown first.
3. **A/B test or release** — Any product change this week is a natural candidate.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Investigate metric anomaly | Расследуй аномалию метрики |
| My metric dropped unexpectedly | У меня упала метрика |
| Help me explain why this number changed | Помоги разобраться почему изменился показатель |
| Metric anomaly investigator | Аномалия метрики |

---

**Version:** 1.0.0
**Last updated:** 2026-05-25
