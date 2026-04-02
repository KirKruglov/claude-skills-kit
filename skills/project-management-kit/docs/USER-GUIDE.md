# User Guide

How to use the AI Project Manager agent: workflows, commands, and practical examples.

## Getting Started

### Session Start

The agent does not retain context between sessions. At the start of each chat, provide:

```
Project name: Mobile Fitness App
Current phase: Planning
Approved artifacts: project-charter.md
Current task: generate project plan
```

If you skip this — the agent will ask for it before starting work.

### Providing Project Data

You can provide data in any format: a structured brief, free-form notes, bullet points, or answers to questions. The agent extracts and structures the information independently.

For best results, include at minimum: project goal, timeline, and at least one of: budget, scope, or team composition.

## Project Lifecycle

The agent supports six project phases. In the MVP, four phases have active skills:

```
Phase 1: Initiation
  └─ generate-charter → generate-risk-register (initial)

Phase 2: Planning
  └─ generate-project-plan → generate-risk-register (detailed) ‖ generate-comm-plan

Phase 3: Prototyping / Development
  └─ generate-meeting-protocol (independent, any phase)

Phase 6: Closing
  └─ generate-plan-fact-report → generate-closure-report
```

The `‖` symbol means skills can run in parallel — order does not matter.

After each approved result, the agent tells you which tasks are now available. You always decide what to do next.

## Skills Reference

### generate-charter

Creates a project charter — the foundational document that defines goals, scope, timeline, budget, team, constraints, and key risks.

**When to use:** At the very beginning of a project when you have initial project data.

**How to invoke:**

- "Generate a project charter"
- "Сформируй устав проекта"
- "Create project charter based on the brief in knowledge"

**What to prepare:** Project data in any form — brief, stakeholder answers, meeting notes, or a free-form description.

**What you get:** A structured charter with 8 sections: goal, scope (included/excluded), timeline with milestones, budget, team and roles, constraints and assumptions, top-3 risks, approval block.

**What happens next:** After approval, the agent suggests generating the initial risk register.

---

### generate-risk-register

Creates or updates a risk register with probability/impact scoring, risk matrix, and response strategies.

**Two modes:**

- **Initial** (Phase 1) — based on the charter. Produces 5-10 risks across multiple categories. Owners set to PM by default.
- **Detailed** (Phase 2) — enriches the initial register with risks from the project plan. Links risks to work packages, assigns specific owners.

**How to invoke:**

- "Generate risk register" / "Сформируй реестр рисков" (initial)
- "Update risk register" / "Обнови реестр рисков" (detailed)

**What to prepare:**

- Initial: approved charter in knowledge.
- Detailed: charter + project plan + risk register v1 in knowledge.

**What you get:** A register table (ID, risk, category, probability, impact, level, strategy, actions, owner, status) + visual risk matrix.

**What happens next:**

- After initial → agent suggests generating the project plan.
- After detailed → agent suggests generating the communication plan.

---

### generate-project-plan

Creates a project plan with WBS (work breakdown structure), milestones, dependencies, and resource map.

**How to invoke:**

- "Generate project plan" / "Сформируй план проекта"
- "Create project plan, I don't have duration estimates — assess based on scope"

**What to prepare:** Approved charter in knowledge. Optionally: duration estimates for work packages and team availability data.

**What you get:** A plan with sections: project summary, phases and work packages table (ID, phase, WP, owner, duration, start/end dates, dependencies), milestones with completion criteria, dependency matrix, resource map, assumptions and constraints.

**Key behaviors:**

- If no duration estimates provided — the agent estimates and marks each as an assumption.
- If dates exceed the charter deadline — the agent flags affected work packages and asks for your decision.
- Work packages are limited to 20 for readability.
- Duration units are consistent: working days (projects ≤3 months) or weeks (>3 months).

**What happens next:** After approval, two tasks become available in parallel: detailed risk register and communication plan.

---

### generate-comm-plan

Creates a communication plan with a stakeholder matrix, communication schedule, and escalation rules.

**How to invoke:**

- "Generate communication plan" / "Сформируй план коммуникаций"
- "Create comm plan"

**What to prepare:** Approved charter and project plan in knowledge. Optionally: additional stakeholder data and channel preferences (Slack, Email, Meets, etc.).

**What you get:** A plan with: stakeholder matrix (influence/interest), communication matrix (who, what, when, how), escalation rules, and templates references.

---

### generate-meeting-protocol

Structures free-form meeting notes into a formal protocol with decisions, action items, and proposed plan changes.

**How to invoke:**

- "Generate meeting protocol" / "Оформи протокол встречи"
- "Process these meeting notes"

**What to prepare:** Meeting notes in any format — bullet points, free text, chat copy, voice dictation transcript. Optionally: current project plan (for linking changes to work packages).

**What you get:** A protocol with: attendees, date, agenda, key discussion points, decisions made, action items (who, what, by when), and proposed plan/document changes.

**Note:** This skill is independent — it can be used in any project phase, as often as needed.

---

### generate-plan-fact-report

Compares planned and actual project data across three dimensions: timelines, budget, and deliverables.

**How to invoke:**

- "Generate plan-fact report" / "Сформируй план-факт"
- "Plan vs actual comparison"

**What to prepare:** Project plan in knowledge + actual data provided in chat (actual completion dates, actual costs, deliverable statuses). The agent will ask for specific data if not provided.

**What you get:** A variance report with: timeline deviations per milestone, budget variance by line item (if budget data exists), deliverable status summary, and overall assessment.

**What happens next:** After approval, the agent suggests generating the closure report.

---

### generate-closure-report

Aggregates all project data into a final closure report: outcomes, deviations, realized risks, and lessons learned.

**How to invoke:**

- "Generate closure report" / "Сформируй отчёт о закрытии"
- "Close the project"

**What to prepare:** Charter, plan-fact report, and lessons learned (provided in chat — retrospective results, team feedback, or PM observations). Optionally: risk register (for realized risks analysis) and open items list.

**What you get:** A comprehensive report with: project summary, goal achievement assessment, deviation analysis, realized risks, lessons learned (categorized), and open items/handover notes.

## Working with the Agent

### Revision Workflow

After the agent presents a document:

1. **Approve** — the agent produces the final version and suggests the next task.
2. **Request changes** — describe what to fix. The agent revises and presents the updated version.
3. After 3 revision cycles — the agent asks whether to continue revising or finalize the current version.

### Language Switching

Write in Russian — the agent responds and generates documents in Russian. Write in English — everything switches to English. Templates are bilingual, so switching mid-project works seamlessly.

### Data Handoff Between Skills

In the MVP, you mediate data transfer:

1. The agent generates a document.
2. You approve it.
3. Upload the approved document to the project's Knowledge section.
4. Start the next task — the agent reads the document from knowledge.

### Project State Tracking

Maintain a `project-state.md` file to track artifact statuses. After each task, the agent proposes ready-to-paste text for updating this file and the project log (`log.md`).

## Tips

**Prepare input data in advance.** The more context you provide upfront, the fewer clarifying questions the agent asks and the better the first draft quality.

**Use knowledge files.** Upload approved documents to knowledge so the agent can reference them directly. This is faster and more reliable than pasting into chat.

**Start with the charter.** The charter is the foundation — all other skills depend on it. Even if you have a mature project, generating a charter first ensures consistency across all subsequent documents.

**Review assumptions carefully.** The agent explicitly labels every assumption it makes. These are the most likely points of error — verify each one against your actual project context.
