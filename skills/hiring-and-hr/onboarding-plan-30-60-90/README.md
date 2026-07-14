> [Версия на русском языке](README.ru.md)

# Onboarding Plan 30-60-90

Generate a structured 30-60-90 day onboarding plan for a new hire from the manager's perspective — three phases, each with goals, key contacts, learning milestones, and a concrete success metric.

---

## Overview

Onboarding Plan 30-60-90 generates a phased onboarding document for a new hire from the manager's perspective. It takes a role description and 3–5 key priorities as input and produces a structured plan covering three phases: Orient (first 30 days), Contribute (days 31–60), and Own (days 61–90). Use this skill when you've just confirmed a hire and need to plan their first 90 days, when you want a consistent onboarding structure for every new team member, or when you're onboarding without a dedicated HR specialist or onboarding system.

---

## Requirements

- New hire role title and level (required)
- 3–5 must-learn priorities or key areas for the role (required)
- Optional: new hire name, start date, work format (Remote / Hybrid / Onsite), team context

No additional tools or integrations required. Works with notes pasted directly into Claude.

---

## How to Use

1. **Gather your input**
   - Have the role title, level, and 3–5 key priorities ready
   - Optionally note the new hire's name, start date, work format, and key teammates

2. **Trigger the skill by saying:**
   - "Create a 30-60-90 day plan for [role]"
   - "Onboarding plan for new hire"
   - In Russian: "Создай план адаптации 30-60-90" or "План онбординга нового сотрудника"

3. **Provide the role details**
   - Paste your notes or describe the role and priorities in a few sentences
   - The skill structures the inputs into three phases

4. **Get your onboarding plan**
   - Receive a markdown document with three phase sections, each containing goals, key contacts, learning milestones, and a success metric
   - Share directly with the new hire or save in your project folder

---

## Examples

### Example 1: Junior Product Manager (Hybrid)

**Input:**
```
Role: Junior Product Manager, Level: Junior
Work format: Hybrid
Priorities: learn the product roadmap process, understand user research workflow, shadow sprint ceremonies, learn Jira and Confluence, understand our 3 core customer segments
```

**Output (excerpt — Phase 1):**
```markdown
# Onboarding Plan: Junior Product Manager — New Hire

**Start Date:** TBD
**Work Format:** Hybrid

---

## Phase 1 — First 30 Days: Orient

**Goals:**
- Learn how the product roadmap is built and how prioritization decisions are made
- Understand how user research outputs feed into product planning
- Performance goal: shadow 3 sprint ceremonies and write a summary after each

**Key Contacts:**
| Name / Role | Purpose | When |
|-------------|---------|------|
| Product Lead (Manager) | Clarify expectations and success criteria | Week 1 |
| UX Researcher | Learn the user research workflow and active studies | Week 2 |
| Engineering Lead | Understand tech constraints that affect the roadmap | Week 2–3 |
| Customer Success Manager | Map the 3 core customer segments | Week 3–4 |

**Learning Milestones:**
- [ ] Complete Jira and Confluence onboarding (read and create tickets)
- [ ] Review the current product roadmap and understand 3 active initiatives
- [ ] Understand the user research workflow: how studies are run and how outputs are used
- [ ] Map the 3 core customer segments with 2–3 defining characteristics each

**Success Metric:** Can describe the product roadmap process and explain 3 current initiatives independently — without prompting from the manager.
```

---

### Example 2: Senior Backend Engineer (Remote)

**Input:**
```
Role: Senior Backend Engineer, Level: Senior
Work format: Remote
Priorities: learn service architecture, understand on-call rotation and incident response, learn CI/CD pipeline, understand data models for core services, shadow team code reviews
```

**Output (excerpt — Phase 1):**
```markdown
# Onboarding Plan: Senior Backend Engineer — New Hire

**Start Date:** TBD
**Work Format:** Remote

---

## Phase 1 — First 30 Days: Orient

**Goals:**
- Map the service architecture and understand which services the team owns
- Understand on-call rotation expectations and the incident response playbook
- Performance goal: submit 2 substantive code reviews with specific comments

**Key Contacts:**
| Name / Role | Purpose | When |
|-------------|---------|------|
| Engineering Manager | Clarify role expectations and success criteria | Week 1 (virtual) |
| Tech Lead | Walk through service architecture and team-owned components | Week 1–2 (async + sync) |
| On-call Buddy | Shadow a handoff and review the on-call runbook | Week 2–3 (async) |
| Senior Engineer (adjacent team) | Understand cross-service dependencies | Week 3–4 (virtual) |

**Learning Milestones:**
- [ ] Read architecture docs and draw a service dependency map for team-owned services
- [ ] Review CI/CD pipeline: understand how deploys are triggered and rolled back
- [ ] Shadow 3 code reviews and internalize team review standards
- [ ] Read the incident response runbook and on-call playbook

**Success Metric:** Can describe team-owned services and their data flow to any team member without preparation.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Create a 30-60-90 day plan | Создай план адаптации 30-60-90 |
| Onboarding plan for new hire | План онбординга нового сотрудника |
| I need to onboard a new team member | Мне нужно подготовить онбординг |
| Help me plan the first 90 days | Помоги спланировать первые 90 дней |
| Write an onboarding plan for [role] | Напиши план адаптации для [должность] |

---

> See [docs/USER-GUIDE.md](docs/USER-GUIDE.md) for detailed usage scenarios and tips.

**Version:** 1.0.0
**Last updated:** 2026-06-18
