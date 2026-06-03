# Retention Cohort Interpreter User Guide

Learn how to get actionable insights from cohort retention data using plain language.

---

## Quick Start

Here's the fastest way to get a retention diagnosis:

1. Copy your retention table from any analytics tool (Amplitude, Mixpanel, Google Sheets, etc.)
2. Say: "Analyze retention cohort" and paste the table
3. Get a structured report: curve health, drop-off points, hypotheses, next steps

**Result:** A plain-language diagnosis you can share in a product review or investor meeting.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Weekly Product Review — Spotting a Retention Problem

**Situation:**
You are a product manager preparing for your weekly metrics review. You pull the cohort retention table from Amplitude and notice that the last three cohorts look worse than before, but you're not sure if it's a real trend or noise. You need to quickly assess whether to escalate this or wait another week.

**What to do:**

1. Export the retention table from Amplitude (or copy from your dashboard)
   - Include 3–6 recent cohorts and all available time periods
   - Copy as CSV or paste directly as a markdown/plain-text table

2. Trigger the skill by saying: "Analyze retention cohort" and paste the table
   - Add context if useful: "This is a B2C mobile app" or "We're focused on D7 improvement"

3. Review the Curve Health section
   - If labeled **Healthy**: data supports a "wait and watch" decision
   - If labeled **Needs Work** or **Critical**: escalation is justified; use the Hypotheses section to frame the conversation

4. Use the Hypotheses to structure the review discussion
   - Share the top 2 hypotheses with your team
   - Use Recommended Next Steps to assign investigation tasks

**Expected result:**

You receive a structured diagnosis with a clear label (Healthy / Needs Work / Critical), the specific period where churn is concentrated, and 3 testable hypotheses tied to that window.

**Why this works:** Instead of eyeballing numbers and debating whether a drop is "significant," you have a framework with specific drop values, benchmark comparisons, and actionable hypotheses. The review becomes focused and decisions are grounded in data.

---

### Scenario 2: Investor Update — Presenting Retention Health

**Situation:**
You are a founder preparing for a monthly investor update. Your B2B SaaS product has been live for 9 months and you have 6 cohorts of customer data. Investors expect a retention section, but you're not sure how to frame the numbers or what story to tell.

**What to do:**

1. Prepare your cohort retention table
   - Include monthly cohorts (M1–M6 for each cohort)
   - If values are absolute account counts, that's fine — the skill will convert them to percentages

2. Say: "Interpret cohort table — this is a B2B SaaS" and paste the data
   - Stating the product type ensures the skill uses the right benchmarks (B2B SaaS, not mobile)

3. Review the Benchmark Comparison section
   - Note whether your curve is above / at / below benchmark — this is your headline statement
   - Use the specific numbers for the investor slide

4. Use the Curve Health narrative in your update
   - Copy the 1–2 sentence summary from the Curve Health section
   - Pair it with the Recommended Next Steps to show you have a plan

**Expected result:**

You receive a benchmark comparison with specific percentages (e.g., "Your M3 retention of 71% is above the B2B SaaS benchmark of 65–70%"), a health label, and a narrative you can quote in the investor email.

**Why this works:** Investors want to see that you understand your retention data and can contextualize it. The benchmark comparison gives you an objective reference point, and the health narrative gives you a concise framing that doesn't require the investor to interpret raw numbers.

---

### Scenario 3: Post-Launch Health Check — Diagnosing a New Feature's Impact

**Situation:**
You are a growth analyst. Your team launched a new onboarding flow 6 weeks ago. You want to know whether the cohorts acquired after the launch have better retention than those before, and if there's still a problem to fix.

**What to do:**

1. Build a comparison table with pre-launch and post-launch cohorts side by side
   - Label rows clearly: "Pre-launch (Feb W1)", "Post-launch (Apr W1)", etc.
   - Include D1, D7, D14, D30 for each cohort

2. Trigger the skill: "Analyze retention cohort — we launched a new onboarding flow on March 15"
   - The context helps the skill flag whether the outlier cohort pattern aligns with the launch date

3. Look for the Edge Case flag about outlier cohorts
   - If post-launch cohorts are flagged as outliers (better or worse), the skill will separate their analysis
   - This tells you whether the launch had a measurable effect

4. Use the Hypotheses for the dominant churn window to identify residual problems
   - Even if the new flow improved D1, there may still be a D7 drop to address

**Expected result:**

You receive a cohort-by-cohort comparison, with outlier cohorts flagged and analyzed separately. The report clearly shows whether post-launch cohorts perform differently, and the Hypotheses point to remaining opportunities.

**Why this works:** The skill automatically highlights cohort outliers and separates their diagnosis from the aggregate trend, making it easy to attribute changes to specific product interventions without manual analysis.

---

## Tips

### Tip 1: Include Period Headers for Accurate Drop Calculation

When you paste your retention table, make sure column headers are present and clearly name the time periods (e.g., "D1", "Week 4", "Month 3"). Without headers, the skill may not correctly compute period-over-period drops. If your headers use non-standard names (like "Period 1", "Period 2"), add a note: "Periods are monthly — Period 1 = M1."

### Tip 2: State Your Product Type for Better Benchmarks

The skill infers product type from column naming patterns (daily periods → mobile; monthly → SaaS), but explicit context is more reliable. Adding "This is a B2B SaaS" or "Consumer marketplace" in your trigger phrase takes 3 seconds and ensures the benchmark comparison is accurate — the difference between "Healthy" and "Needs Work" labels can depend on which benchmark is applied.

### Tip 3: Use the Hypotheses as Your Investigation Brief

The 3 hypotheses in the report are designed to be directly actionable. Copy them into a Notion doc or Slack message to kick off an investigation sprint. Each hypothesis maps to a specific metric or event to instrument, a segment to isolate, or a user interview question to ask. Don't just read them — assign ownership and a due date to each one.

---

**Version:** 1.0.0
**Last updated:** 2026-06-03
