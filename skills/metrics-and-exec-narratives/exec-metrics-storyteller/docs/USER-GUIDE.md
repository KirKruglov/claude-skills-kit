# Exec Metrics Storyteller — User Guide

Learn how to turn your metrics snapshot into a board-ready executive narrative in minutes.

---

## Quick Start

Here's the fastest way to get an executive report:

1. Copy your top 5–10 KPIs from your dashboard or weekly report
2. Say: "Exec metrics report" and paste the metrics with the reporting period
3. Get back a markdown narrative with Headline KPIs, Executive Summary, Revenue & Unit Economics, Trend Analysis, and Outlook

**Result:** A structured executive narrative ready to paste into a board deck, email, or document.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Monthly Board Deck Narrative

**Situation:**
You are a Head of Product preparing next week's board deck. You have your monthly KPI dashboard open (MAU, ARR, churn, activation, LTV:CAC) and need to write the metrics narrative — the section where you explain what the numbers mean and what they signal strategically. Writing this from scratch typically takes 30–45 minutes. You want to get a draft in under 5 minutes.

**What to do:**

1. Open your KPI dashboard and note the 5–8 most important metrics for the month
   - Include period-over-period deltas (MoM or QoQ) where available
   - Note your monthly targets for the top 2–3 metrics

2. Trigger the skill:
   - Say: "Turn my metrics into a board report"
   - Then paste: period, audience type, and your KPI list

3. Review the output sections:
   - **Headline KPIs table** → copy directly into your board slide
   - **Executive Summary** → use as your opening paragraph or speaker notes
   - **Revenue & Unit Economics** → use in the financial section of the deck
   - **Trend Analysis** → use to drive the "What we're watching" board discussion slide

4. Adjust framing if needed
   - If the skill surfaces a "Tension to address" callout, decide which framing to use before the board meeting

**Expected result:**

A complete 5-section executive narrative that takes a data-driven PM from "numbers in a dashboard" to "story-ready board slide" in one step. The Headline KPIs table is paste-ready for slides. The Executive Summary is already in board-appropriate prose tone.

**Why this works:** Instead of translating numbers into sentences manually, the skill interprets each metric in business terms and structures them into the sections boards expect. You still control the framing; the skill eliminates the blank-page problem.

---

### Scenario 2: C-Suite Weekly Metrics Digest

**Situation:**
You are a product manager and your CPO receives a weekly metrics email every Monday morning. Each week you paste numbers into a template and write 2–3 sentences per metric. It's repetitive and time-consuming. You want to automate the first draft so you spend time on insights, not formatting.

**What to do:**

1. Each Monday, pull your weekly KPIs from your dashboard
   - MAU, weekly active users, key feature engagement, revenue (if weekly), support volume

2. Trigger the skill:
   - Say: "Write executive metrics narrative"
   - State: "weekly digest for CPO" and paste your metrics

3. Review the draft
   - The Executive Summary becomes your email opening
   - Headline KPIs table goes in the body
   - Trim the Outlook section if you prefer to write that yourself

4. Add your own commentary on 1–2 metrics where you have additional context
   - The draft handles routine interpretation; you add the strategic color

**Expected result:**

A weekly digest draft ready in under 2 minutes, covering all 5 sections. Your CPO gets a consistent, well-structured update. You spend your time on the 20% of metrics that need custom commentary.

**Why this works:** The skill handles the boilerplate (structuring, labeling, interpreting standard KPI movements). You focus on context and judgment that only you have.

---

### Scenario 3: Investor Update — Minimal Snapshot

**Situation:**
You are a startup founder preparing a monthly investor update. You only track 4–5 core metrics (MRR, churn, NPS, CAC). You need to write a narrative that frames these as a coherent story, not just a table of numbers. You also want the skill to flag if any metric looks unusual so you can address it proactively.

**What to do:**

1. Gather your 4–5 metrics with period and deltas
   - Example: `MRR: $85k (+6% MoM), Churn: 1.8%, NPS: 52 (+3 pts), CAC: $38`

2. Trigger the skill:
   - Say: "Prepare C-suite metrics story"
   - Add: "audience: investors, period: May 2026, monthly"

3. Review the output
   - The skill will note "limited metrics" if LTV or growth data is absent — useful signal for what to add next month
   - The Trend Analysis will flag any metric with >15% deviation
   - The "Tension to address" callout (if triggered) helps you anticipate investor questions

4. Use the output as the narrative body of your investor update email

**Expected result:**

A narrative-first investor update with honest interpretation of your 4–5 metrics. Any data gaps are surfaced as placeholders, not silently omitted. The Outlook section gives investors a forward-looking signal, not just a rearview snapshot.

**Why this works:** Investors read hundreds of updates. A structured narrative with clear status signals (✅/⚠️/🔴) and an honest "Tension to address" callout builds more trust than a polished but opaque table of numbers.

---

## Tips

### Tip 1: Include Deltas Wherever Possible

The skill's Watch/Alert flagging only activates when deltas are provided. Without deltas (e.g., `MAU: 120k` vs. `MAU: 120k (+12% MoM)`), the skill generates the report but cannot assign status labels. Adding even rough deltas — vs. prior period, vs. target, or vs. year-ago — significantly improves the output.

**Pro tip:** If you only have absolute values, mention your targets explicitly: "MAU: 120k, target was 130k." The skill will infer the delta.

### Tip 2: Name the Audience Explicitly

"Board," "C-suite," and "investors" produce different tone and emphasis. Board reports focus on strategic implications and risk. C-suite updates are more operational. Investor narratives emphasize unit economics and growth trajectory. If you don't specify, the skill defaults to "board."

**Pro tip:** Add one line at the start: "This is a monthly report for [audience]." That's enough context.

### Tip 3: Use "Tension to Address" as Prep for Hard Questions

When the skill flags contradictory signals (e.g., "MAU is growing but churn is also rising"), it offers two narrative framings. This is not a bug — it's a reflection of real ambiguity in your data. Read both framings before your board meeting: they typically map to the two questions a board member might raise. Choosing your framing in advance helps you lead the discussion instead of reacting to it.

---

**Version:** 1.0.0
**Last updated:** 2026-06-02
