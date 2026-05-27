# Experiment Results Interpreter

Turn raw A/B test results into a clear go/no-go decision — with a plain-language explanation and a ready-to-paste stakeholder summary.

---

## Overview

Experiment Results Interpreter takes an A/B test description and results from any analytics tool and returns three things: a plain-language assessment of whether the result is statistically significant, a ship/rollback/extend recommendation with a documented rationale, and a stakeholder summary you can copy straight into Slack or email.

No statistics background needed. Paste your numbers, describe what was tested, and get a decision in one message.

---

## Requirements

Provide at minimum:
- What was tested (feature or change name)
- The primary metric (e.g., "checkout conversion rate", "7-day retention")
- Results — one of:
  - p-value or confidence interval from your analytics tool
  - Lift % and significance status
  - Raw counts: visitors and conversions per variant

Optional (improves the recommendation):
- Guardrail metrics (secondary metrics you want to protect)
- Test duration and sample size per variant
- Variant names and what changed

No files, tools, or external integrations required. Plain text paste from Amplitude, Optimizely, LaunchDarkly, GA4, or any other tool works fine.

---

## How to Use

1. **Trigger the skill:**
   - "Interpret experiment results: [paste your results]"
   - "Should I ship this experiment? [describe test + results]"
   - "Help me read my A/B test results"

2. **Paste or describe your results.** Examples of valid input:
   - "Checkout conversion: control 3.1%, treatment 3.4%, p=0.03, n=12,000 per variant, 14 days"
   - "We tested a new onboarding modal. Activation rate went up 8% (p=0.07). Retention was flat."
   - "Control: 450 conversions / 14,200 visitors. Treatment: 510 conversions / 14,100 visitors."

3. **Get your output:**
   - **Test Summary** — structured recap of the test setup
   - **Results Interpretation** — plain-language significance verdict with the numbers
   - **Recommendation** — Ship / Rollback / Extend / Hold / Inconclusive with 3-bullet rationale
   - **Draft Stakeholder Summary** — copy-paste ready for Slack or email

---

## Examples

### Example 1: Pre-computed Results

**Input:**
```
We tested a simplified checkout form (removed 3 optional fields). Primary metric: checkout completion rate. Control: 3.1%, Treatment: 3.6%, lift +16%, p=0.02. Sample: 11,500 per variant over 14 days. Guardrail: average order value — control $84, treatment $82.
```

**Output:**
```markdown
## Test Summary
- Feature: Simplified checkout form (removed 3 optional fields)
- Hypothesis: Reducing form friction will increase checkout completion
- Variants: Control (original form) vs. Treatment (simplified form)
- Primary metric: Checkout completion rate
- Guardrail metric: Average order value (AOV)
- Duration: 14 days | Sample: 11,500 per variant

## Results Interpretation
The result is **statistically significant** (p = 0.02, well below the 0.05 threshold). Treatment improved checkout completion from 3.1% to 3.6% — a +16% relative lift. With 11,500 users per variant over 14 days, the sample is adequate and the test captured a full two-week cycle.

⚠️ **Guardrail flag:** Average order value declined slightly from $84 to $82 (–2.4%). This difference is small but worth noting before shipping.

## Recommendation: HOLD
- The primary metric result is strong and significant: a +16% lift in checkout completion with p = 0.02.
- However, AOV declined by $84 → $82 (–2.4%). Before shipping, confirm whether this guardrail shift is statistically significant and what the revenue impact is at scale.
- Next action: run significance test on the AOV delta; if AOV decline is not significant or the revenue gain from higher completion outweighs the AOV dip, proceed to Ship.

## Draft Stakeholder Summary
We ran a 14-day test of a simplified checkout form (removed 3 optional fields). Checkout completion improved +16% (3.1% → 3.6%, p = 0.02), which is a strong and statistically significant result. However, average order value dipped slightly from $84 to $82, so we are doing a quick revenue impact check before shipping. We expect a final go/no-go decision within one business day.
```

---

### Example 2: Raw Counts, No p-value

**Input:**
```
Tested a new empty state in the dashboard. Metric: feature activation (users who clicked at least one item in the first session).
Control: 1,820 activations out of 9,400 visitors.
Treatment: 2,050 activations out of 9,300 visitors.
Test ran 10 days.
```

**Output:**
```markdown
## Test Summary
- Feature: New empty state in the dashboard
- Hypothesis: Improved empty state will increase first-session feature activation
- Variants: Control (original empty state) vs. Treatment (new empty state)
- Primary metric: Feature activation rate (clicked at least one item in first session)
- Duration: 10 days | Sample: 9,400 (control) / 9,300 (treatment)

## Results Interpretation
Computing significance from raw counts:
- Control rate: 1,820 / 9,400 = 19.36%
- Treatment rate: 2,050 / 9,300 = 22.04%
- Lift: +13.8%
- z-score ≈ 5.1 → p < 0.001 — **statistically significant**

The result is highly significant. The treatment improved activation by approximately +14% relative, with a very large sample that leaves no ambiguity about the direction of the effect.

⚠️ **Maturation note:** 10 days is slightly below the recommended 14-day window. However, with a z-score this large and a stable conversion product, extending is unlikely to change the conclusion.

## Recommendation: SHIP
- The result is highly significant (p < 0.001) with a +13.8% lift in feature activation across 18,700 users.
- No guardrail metrics were provided; if you track session length or downstream engagement, spot-check those before closing the experiment.
- Next action: ship to 100%, close experiment, and set a 2-week post-ship monitoring alert on the activation metric.

## Draft Stakeholder Summary
We tested a new empty state design in the dashboard over 10 days with 18,700 users. First-session feature activation improved +14% (19.4% → 22.0%), a highly significant result. The recommendation is to ship. We will close the experiment and monitor activation and downstream engagement metrics for two weeks post-launch.
```

---

## Triggers

| English | Russian |
|---------|---------|
| Interpret experiment results | Интерпретируй результаты эксперимента |
| Read my A/B test results | Помоги прочитать результаты A/B теста |
| Should I ship this experiment | Шипать ли этот эксперимент |
| Help me interpret test results | Разбери результаты теста |
| Experiment results interpreter | Интерпретатор результатов эксперимента |

---

**Version:** 1.0.0
**Last updated:** 2026-05-27
