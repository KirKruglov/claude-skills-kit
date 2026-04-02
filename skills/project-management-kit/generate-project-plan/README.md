# generate-project-plan

Generates a project plan with WBS, milestones, dependencies, and resource map.

## Overview

The project plan decomposes the charter's scope into work packages, establishes timelines and dependencies, defines milestones with completion criteria, and maps resource allocation. This is the core planning artifact.

**Phase:** 2 — Planning
**Output:** `project-plan.md`

## Triggers

| Language | Commands |
|----------|----------|
| English | "generate project plan", "create project plan", "build plan", "prepare project plan" |
| Russian | «сформируй план проекта», «подготовь план», «составь project plan», «нужен план проекта» |

## Required Inputs

| Data | Required | Notes |
|------|:--------:|-------|
| Approved project charter | yes | Source of goal, scope, dates, budget, team, constraints |
| Duration estimates | no | Work package estimates. If absent — agent estimates and marks as assumptions |
| Team availability | no | Load by period, vacations, part-time. If absent — even distribution assumed |

## Output Structure

The plan contains: project summary, phases and work packages table (max 20 WPs), milestones with completion criteria, dependency matrix, resource map (load % by period), and assumptions/constraints.

**Key rules:** duration unit is consistent (working days for projects up to 3 months, weeks for longer); no dates beyond the charter deadline (flagged if unavoidable); milestones are checkpoints, not tasks.

## Dependencies

**Requires:** `generate-charter` (approved charter)

**Unlocks after approval (parallel):**

- `generate-risk-register` (mode: detailed)
- `generate-comm-plan`

## Example

> Generate a project plan. The charter is approved and in knowledge. No duration estimates — assess based on scope.

Agent produces a plan with estimated durations (marked as assumptions), resource allocation, and flags any schedule conflicts.
