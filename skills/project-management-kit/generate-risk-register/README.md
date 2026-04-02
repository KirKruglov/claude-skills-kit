# generate-risk-register

Generates or updates a risk register with probability/impact scoring and response strategies.

## Overview

The risk register identifies project risks, assesses their probability and impact, calculates risk levels, and defines response strategies. Operates in two modes: initial (from charter) and detailed (enriched with project plan data).

**Phase:** 1 — Initiation (initial), 2 — Planning (detailed)
**Output:** `risk-register.md`

## Triggers

| Language | Commands |
|----------|----------|
| English | "generate risk register", "create risk register", "update risk register" |
| Russian | «сформируй реестр рисков», «подготовь risk register», «обнови реестр рисков» |

## Modes

**Initial** (Phase 1): analyzes the charter to identify 5-10 risks across categories (Technical, Resource, External, Organizational, Financial). Owners default to PM.

**Detailed** (Phase 2): uses the project plan to add new risks, link all risks to work packages (WP-xxx), assign specific owners, and update assessments.

## Required Inputs

| Data | Required | Mode | Notes |
|------|:--------:|------|-------|
| Project charter | yes | both | Primary context |
| Project plan | yes | detailed | WBS, timeline, resources — source of new risks |
| Risk register v1 | yes | detailed | Base for update |

## Output Structure

Register table with 10 columns (ID, Risk, Category, Probability, Impact, Level, Strategy, Actions, Owner, Status) plus a visual risk matrix. Assessment scale: H/M/L for probability and impact; levels: Critical, High, Medium, Low.

## Dependencies

**Requires:**

- Initial: `generate-charter` (approved charter)
- Detailed: `generate-charter` + `generate-project-plan` + initial risk register

**Unlocks after approval:**

- Initial → `generate-project-plan`
- Detailed → `generate-comm-plan`

## Example

**Initial mode:**

> Generate the risk register. Project charter is in knowledge.

**Detailed mode:**

> Update the risk register. Project plan and current register are in knowledge.
