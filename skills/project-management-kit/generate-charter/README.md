# generate-charter

Generates a project charter — the foundational document of the Initiation phase.

## Overview

The charter defines the project's goal, scope, timeline, budget, team, constraints, and key risks. It is the first artifact created and serves as the basis for all subsequent skills.

**Phase:** 1 — Initiation
**Output:** `project-charter.md`

## Triggers

| Language | Commands |
|----------|----------|
| English | "generate charter", "create project charter", "build charter", "draft project charter" |
| Russian | «сформируй устав», «подготовь устав проекта», «создай charter», «нужен устав проекта» |

## Required Inputs

| Data | Required | Notes |
|------|:--------:|-------|
| Project data | yes | Brief, free-form description, stakeholder answers, or unstructured notes |
| Stakeholder answers | no | Completed questionnaire or free-form answers |
| Project constraints | no | Budget, timeline, technical, organizational |
| Team composition | no | If provided — fills team section; otherwise only Sponsor and PM |

**Minimum to start:** project goal + at least one of: timeline, budget, scope.

## Output Structure

The charter contains 8 sections: project goal, scope (included/excluded), timeline and milestones, budget, team and roles, constraints and assumptions, top-3 key risks with mitigation, and approval block.

## Dependencies

**Requires:** project data from the user (no prior skills needed).

**Unlocks after approval:**

- `generate-risk-register` (mode: initial) — Phase 1
- `generate-project-plan` — Phase 2

## Example

**Command:**

> Generate a project charter. We're building a mobile app for fitness tracking. Timeline: 4 months, budget $50K, team: PM + 2 devs + 1 designer + 1 QA.

**Agent produces:** a structured charter with all 8 sections filled from the provided data, assumptions labeled, ready for review and approval.
