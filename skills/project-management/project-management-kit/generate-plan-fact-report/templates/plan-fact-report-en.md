# Plan-vs-Actual Report: {{project_name}}

**Version:** 1.0
**Date:** {{date}}
**File:** `plan-fact-report.md`
**Document status:** `draft`
**Period:** {{start_date}} — {{end_date}}
**Report type:** {{report_type}}
**Planned data source:** {{source_plan}}
**Actual data source:** {{source_fact}}

*Allowed values for "Report type": `interim` / `final`.*

---

## 1. Summary

Overall project variance across three dimensions.

| Parameter | Plan | Actual | Variance | Variance, % | Status |
|-----------|------|--------|----------|-------------|--------|
| Timelines (days) | {{planned_duration}} | {{actual_duration}} | {{delta_time}} | {{delta_time_pct}} | {{status_time}} |
| Budget ({{currency}}) | {{planned_budget}} | {{actual_budget}} | {{delta_budget}} | {{delta_budget_pct}} | {{status_budget}} |
| Scope (deliverable count) | {{planned_scope}} | {{delivered_scope}} | {{delta_scope}} | {{delta_scope_pct}} | {{status_scope}} |

---

## 2. Timelines

Row-by-row comparison of planned and actual milestone dates.

| # | Milestone | Planned Date | Actual Date | Variance (days) | Variance Reason |
|---|-----------|--------------|-------------|-----------------|-----------------|
| 1 | {{milestone_name}} | {{planned_date}} | {{actual_date}} | {{delta_days}} | {{reason}} |

*Milestones sourced from `project-plan.md`. If a milestone is not complete — enter `not complete` in "Actual Date." Variance: positive = delay, negative = ahead of schedule.*

---

## 3. Budget

Row-by-row comparison of planned and actual costs by budget line.

| # | Cost Line | Plan ({{currency}}) | Actual ({{currency}}) | Variance | Variance, % | Comment |
|---|-----------|---------------------|-----------------------|----------|-------------|---------|
| 1 | {{cost_item}} | {{planned_cost}} | {{actual_cost}} | {{delta}} | {{delta_pct}} | {{comment}} |
| | **Total** | **{{total_plan}}** | **{{total_fact}}** | **{{total_delta}}** | **{{total_delta_pct}}** | |

*If a cash flow plan is unavailable — use linear distribution and enter `estimated` in the Comment column.*

---

## 4. Recommendations / Next Steps

| # | Issue / Observation | Recommended Action | Owner | Deadline |
|---|--------------------|--------------------|-------|----------|
| 1 | {{issue_1}} | {{action_1}} | {{owner_1}} | {{deadline_1}} |

---

## Changelog

| Date | Version | Change |
|------|---------|--------|
| {{date}} | 1.0 | Created by agent based on {{source_plan}} and actual data |
| 2026-03-24 | 1.1 | Added "File" and "Document status" fields based on template analysis |
| 2026-03-25 | 1.2 | Revised per Option A: template converted from xlsx specification to full .md artifact. Added "Recommendations" section and "Report type" field. xlsx specification retained in SKILL.md |
