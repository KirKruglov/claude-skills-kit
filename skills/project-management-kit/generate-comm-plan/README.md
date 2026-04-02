# generate-comm-plan

Generates a communication plan with stakeholder matrix, communication schedule, and escalation rules.

## Overview

The communication plan maps stakeholders by influence and interest, defines what information each stakeholder receives, through which channel, and at what frequency, and establishes escalation procedures.

**Phase:** 2 — Planning
**Output:** `comm-plan.md`

## Triggers

| Language | Commands |
|----------|----------|
| English | "generate comm plan", "create communication plan", "build comm plan" |
| Russian | «сформируй план коммуникаций», «подготовь comm-plan», «кому и как коммуницировать» |

## Required Inputs

| Data | Required | Notes |
|------|:--------:|-------|
| Project charter | yes | Source of stakeholders, goals, scope, constraints |
| Project plan | yes | Source of milestones, phases — for binding communications to events |
| Stakeholder data | no | Additional stakeholders not in the charter |
| Channel preferences | no | Communication channels used by the team (Slack, Teams, Email, etc.) |

## Output Structure

The plan includes: stakeholder analysis matrix (influence/interest quadrant), communication matrix (stakeholder, information type, frequency, channel, responsible person), escalation rules, and key communication event templates.

## Dependencies

**Requires:** `generate-charter` + `generate-project-plan` (both approved)

**Unlocks:** no downstream dependencies in MVP.

## Example

> Generate a communication plan. Charter and project plan are in knowledge. We use Slack for daily comms and Google Meet for meetings.
