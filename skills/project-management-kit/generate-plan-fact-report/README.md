# generate-plan-fact-report

Generates a plan-vs-actual variance report comparing planned and actual project data.

## Overview

Compares planned and actual data across three dimensions: timelines (milestones), budget (line items), and scope (deliverables). Used in the Closing phase to assess project performance before the final closure report.

**Phase:** 6 — Closing
**Output:** `plan-fact-report.md`

## Triggers

| Language | Commands |
|----------|----------|
| English | "generate plan-fact report", "plan vs actual", "variance report" |
| Russian | «сформируй план-факт», «подготовь отчёт план/факт», «сравни план и факт» |

## Required Inputs

| Data | Required | Notes |
|------|:--------:|-------|
| Project plan | yes | Source of planned milestones, budget, deliverables |
| Actual data | yes | Provided by user in chat: actual dates, costs, deliverable statuses |
| Project charter | no | For deliverables list. If unavailable — agent requests from user |
| Report type | no | `interim` or `final` (default: interim). Affects header label only |

## Output Structure

The report contains up to three sections: timeline variance (planned vs actual dates per milestone with deviation), budget variance (planned vs actual per line item, if budget data exists), and deliverable status summary (completed, in progress, not started, cancelled).

## Dependencies

**Requires:** `generate-project-plan` (approved plan) + actual data from user

**Unlocks after approval:** `generate-closure-report`

## Example

> Generate a plan-fact report. Project plan is in knowledge. Here are the actuals: M1 completed on April 15 (planned April 10), M2 on May 20 (planned May 15), total spend $48K out of $50K budget.
