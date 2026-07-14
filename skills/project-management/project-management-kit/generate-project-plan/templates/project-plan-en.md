# Project Plan: {{project_name}}

**Version:** {{version}}
**Date:** {{date}}
**File:** `project-plan.md`
**Document status:** `draft`
**Source:** {{source_docs}}

---

## Project Summary

| Parameter | Value |
|-----------|-------|
| Project goal | {{project_goal}} |
| Dates | {{start_date}} — {{end_date}} ({{duration}}) |
| Budget | {{budget}} |
| Team | {{team_size}} people |
| Customer | {{customer}} |
| Project manager | {{pm}} |

---

## Phases and Work Packages

| ID | Phase | Work package | Owner | Duration | Start | End | Dependencies |
|----|-------|--------------|-------|----------|-------|-----|--------------|
| WP-001 | {{phase_name}} | {{work_package}} | {{owner}} | {{duration}} | {{start}} | {{end}} | — |
| WP-002 | {{phase_name}} | {{work_package}} | {{owner}} | {{duration}} | {{start}} | {{end}} | WP-001 |

---

## Milestones

| ID | Milestone | Date | Completion criterion | Status |
|----|-----------|------|----------------------|--------|
| M1 | {{milestone_name}} | {{date}} | {{done_criteria}} | not achieved |

---

## Dependencies

| Source block | Target block | Type | Comment |
|--------------|--------------|------|---------|
| WP-001 | WP-002 | FS | {{comment}} |

---

## Assumptions and Constraints

### Assumptions

- {{assumption_1}}
- {{assumption_2}}

### Constraints

- {{constraint_1}}
- {{constraint_2}}

---

## Resource Map

| Team member | Role | April | May | June | Constraints / Notes |
|-------------|------|-------|-----|------|---------------------|
| {{name_1}} | {{role_1}} | {{load_apr}} | {{load_may}} | {{load_jun}} | {{constraints_1}} |

---

## Changelog

| Date | Version | Change |
|------|---------|--------|
| {{date}} | 1.0 | Created by agent based on {{source_docs}} |
| 2026-03-24 | 1.1 | Added "File" and "Document status" fields following template analysis |
| 2026-03-25 | 1.2 | Added "Resource Map" section for team availability data by period. Removed "Timeline" section as redundant |
| 2026-03-25 | 1.3 | Removed "How to fill the table" sections and agent instructions (moved to SKILL.md generate-project-plan §3) |
