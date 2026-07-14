> [Версия на русском языке](README.ru.md)

# North Star Metric Auditor

Audit your North Star Metric against 4 standard criteria and get 2–3 business-model-fit alternatives if you need to switch.

---

## Overview

North Star Metric Auditor evaluates a given NSM against 4 criteria — customer value, revenue predictability, team actionability, and leading-indicator quality — and delivers a clear Strong / Acceptable / Weak verdict with specific justifications. It then proposes 2–3 alternative metric candidates calibrated to your business model, each with a trade-off explanation. Use this skill when defining your first NSM, suspecting your current metric drives wrong team behaviours, or preparing a strategy review where leadership questions your measurement approach.

---

## Requirements

- Your current North Star Metric (metric name; optionally, how you measure it)
- A brief business model description: product type, revenue model, and core user value (1–3 sentences)
- Optional: strategic focus area (growth / retention / monetisation)

No additional tools or files required.

---

## How to Use

1. **Identify your current NSM**
   - Note the metric name and, if possible, how you define it (e.g., "weekly active users who complete at least one task")

2. **Trigger the skill**
   - Say: "Audit north star metric" or "Is my NSM correct?"
   - In Russian: "Аудит north star metric" or "Проверь нашу NSM"

3. **Describe your business model**
   - Provide your product type and revenue model in 1–3 sentences
   - Example: "B2C freemium task manager; revenue from Pro subscriptions; core value is task completion"

4. **Review the audit report**
   - Get a criteria table with 4 ratings, an overall verdict, and 2–3 alternative candidates
   - Use the recommendation to decide whether to keep or replace your NSM

---

## Examples

### Example 1: B2C Freemium App — Weak NSM

**Input:**
```
NSM: Monthly Active Users (MAU)
Business model: B2C freemium habit tracker; revenue from Premium subscriptions; core value = forming lasting habits.
```

**Output:**
```markdown
## North Star Metric Audit: Monthly Active Users (MAU)

### Criteria Assessment

| Criterion | Rating | Justification |
|-----------|--------|---------------|
| Customer Value | Acceptable | MAU captures users opening the app but not whether they formed a habit. A user who opens the app once a month counts the same as a daily engaged user. |
| Revenue Predictability | Acceptable | MAU correlates with revenue at a high level but doesn't predict subscription conversion — many monthly users never convert to Premium. |
| Team Actionability | Strong | Product teams can directly influence MAU through notifications, onboarding, and re-engagement campaigns. |
| Leading Indicator | Weak | MAU is a broad trailing count, not a signal of habit formation. It doesn't predict churn or long-term retention. |

### Overall Verdict: Acceptable
MAU is actionable but too shallow — it doesn't capture whether users are building habits, which is the core value of the product.

---

### Alternatives (Business model: B2C freemium habit tracker)

#### 1. Weekly Habit Completions per User
- **Why it fits:** Directly measures habit formation (core value), predicts subscription conversion better than MAU, and is a leading indicator of long-term retention.
- **Potential downside:** Requires instrumentation of a "habit completion" event in analytics — may need 2–4 weeks of setup.

#### 2. 7-Day Streak Users
- **Why it fits:** Captures habitual daily behaviour, strongly predicts Premium conversion, and can be influenced through streak mechanics.
- **Potential downside:** Prone to gamification — users may maintain streaks without genuine value delivery.

#### 3. D30 Retention Rate
- **Why it fits:** Strong leading indicator of subscription revenue; users retained at Day 30 are far more likely to convert and stay.
- **Potential downside:** 30-day lag makes it slow to respond to product changes — harder to use in fast iteration cycles.

---

### Recommendation
Switch to **Weekly Habit Completions per User** — instrument the "habit completion" event in your analytics tool within the next 2 weeks.
```

---

### Example 2: B2B SaaS — Strong NSM (brief)

**Input:**
```
NSM: Seats with at least one active user per week
Business model: B2B SaaS project management tool; seat-based subscriptions; core value = team coordination.
```

**Output excerpt:**
```markdown
### Overall Verdict: Strong
Captures team adoption (not just individual usage), aligns with seat-based revenue, and is directly actionable through onboarding and collaboration features.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Audit north star metric | Аудит north star metric |
| North star metric review | Проверь нашу north star метрику |
| Is my NSM correct? | Правильная ли у нас NSM? |
| Help me choose a better north star metric | Помоги выбрать лучшую метрику роста |
| NSM audit | Оцени нашу метрику роста |

---

**Version:** 1.0.0  
**Last updated:** 2026-06-09

📖 User scenarios: [docs/USER-GUIDE.md](docs/USER-GUIDE.md)
