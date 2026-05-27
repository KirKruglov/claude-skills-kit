# User Guide: Experiment Results Interpreter

## What This Skill Does

Takes your A/B test results and tells you: is this significant, should you ship, and how do you explain it to stakeholders.

You paste your numbers. The skill reads them, assesses whether the result is statistically significant (in plain English), gives you a decision, and drafts the message to your team.

---

## Before You Start

You need at minimum two things:
1. **What you were measuring** — the primary metric (e.g., "checkout conversion rate", "sign-up rate", "7-day retention")
2. **The result** — any of:
   - p-value from your analytics tool (e.g., "p = 0.03")
   - Confidence interval (e.g., "95% CI: 0.8% to 4.2% lift")
   - Raw numbers: visitors and conversions for each variant

If you only have "conversion rate went up 5%" without any significance data, the skill will ask for visitor counts so it can compute significance for you.

---

## How to Trigger It

Use any of these in a message:

**English:**
- "Interpret experiment results: [paste results]"
- "Should I ship this experiment? [describe test + results]"
- "Help me read my A/B test results"

**Russian:**
- "Интерпретируй результаты эксперимента: [вставьте результаты]"
- "Шипать ли этот эксперимент? [опишите тест + результаты]"
- "Помоги прочитать результаты A/B теста"

---

## What to Paste

Paste your results from any tool. Plain text is fine. Examples of valid inputs:

**From Amplitude / Mixpanel:**
```
Experiment: New checkout button colour
Primary: checkout_started event rate
Control: 4.2% | Treatment: 4.7% | Lift: +11.9% | p-value: 0.04
Sample: 8,200 control / 8,350 treatment | Duration: 21 days
```

**From Optimizely / LaunchDarkly:**
```
Experiment name: Simplified signup flow
Winner: Variation A
Conversion rate: Baseline 12.3%, Variation A 14.1%
Statistical significance: 97%
```

**Raw counts (if your tool doesn't show significance):**
```
Control: 3,100 visitors, 186 conversions
Treatment: 3,050 visitors, 225 conversions
Test ran 14 days
```

---

## What You Get Back

**Test Summary** — a structured recap of the test so you can confirm the skill understood correctly.

**Results Interpretation** — plain-language explanation of whether the result is significant, borderline, or inconclusive. If you gave raw counts, the skill computes the z-score and explains what it means.

**Recommendation** — one of:
- **Ship** — result is significant and positive, safe to launch
- **Rollback** — result is significant and negative
- **Extend** — result is borderline or sample too small; collect more data
- **Hold** — primary metric improved but a guardrail metric degraded; investigate before shipping
- **Inconclusive** — result is not significant; do not ship based on this data

Every recommendation includes 3 bullet points explaining the rationale and the concrete next action.

**Draft Stakeholder Summary** — 3–4 sentences ready to paste into Slack, email, or a document.

---

## Tips for Better Results

**Include guardrail metrics.** If you track secondary metrics that must not degrade (average order value, session length, error rate), include them. The skill will flag if they moved.

**Mention test duration.** Tests under 7 days miss weekly seasonality patterns. The skill will flag this and may recommend extending even if the result looks significant.

**One primary metric.** If you paste results for several metrics, the skill will ask you to designate one as the primary decision metric. Decide this before running the skill to save a round-trip.

**Conflicts are fine to mention.** If your analytics tool says significant but your experiment platform disagrees, mention both. The skill will note the conflict and give conservative guidance.

---

## Common Questions

**The skill asked me for more data. What does it need?**
Usually either the visitor counts per variant (to compute significance) or the primary metric name. Paste the missing piece and it will proceed.

**My p-value is 0.06. Is that significant?**
The skill will classify this as "borderline" — leaning significant but uncertain. The typical recommendation is to extend the test to collect more data. The skill will explain the tradeoff clearly.

**What if I have 5 variants?**
Designate one as the primary comparison (usually the most important treatment vs. control). The skill handles pairwise comparisons; for multi-armed experiments, mention which pair you want the decision on.

**The test only ran 5 days. Should I still use this?**
Yes — the skill will flag the short duration and recommend extending, even if the result looks significant. Weekly seasonality can reverse short-window results.
