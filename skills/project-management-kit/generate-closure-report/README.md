# generate-closure-report

Generates a project closure report — the final artifact of the project lifecycle.

## Overview

Aggregates all project data into a comprehensive closure document: outcomes vs goals, deviation analysis, realized risks, lessons learned, and handover notes. This is the last document produced by the agent.

**Phase:** 6 — Closing
**Output:** `closure-report.md`

## Triggers

| Language | Commands |
|----------|----------|
| English | "generate closure report", "close project", "project closure report", "prepare closure report" |
| Russian | «сформируй отчёт о закрытии», «закрой проект», «подготовь closure report», «отчёт о закрытии проекта» |

## Required Inputs

| Data | Required | Notes |
|------|:--------:|-------|
| Project charter | yes | Goal, deliverables, team, sponsor, budget, timeline |
| Plan-fact report | yes | Deviation summary, actual dates/budget/scope |
| Lessons learned | yes | Provided in chat: retrospective results, team feedback, PM observations |
| Risk register | no | For realized risks analysis |
| Open items | no | Tasks/questions remaining after closure |

## Output Structure

The report contains: project summary (from charter), goal achievement assessment, deviation analysis (from plan-fact report), realized risks and their impact, lessons learned (categorized), open items and handover notes, and final sign-off block.

## Dependencies

**Requires:** `generate-charter` + `generate-plan-fact-report` (both approved) + lessons learned from user

**Unlocks:** no downstream dependencies. This is the final skill in the project lifecycle.

## Example

> Generate a closure report. Charter and plan-fact report are in knowledge. Lessons learned: underestimated QA effort by 30%, should have started integration testing earlier; customer communication worked well with weekly demos; risk R003 (contractor delay) materialized but was mitigated within buffer.
