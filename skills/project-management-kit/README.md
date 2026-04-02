# AI Project Manager Agent for Claude

An AI agent that automates project management documentation for IT product development teams. Built as a set of skills for Claude.ai Projects.

## What It Does

The agent generates structured project documents through a conversational interface. You provide project data — the agent asks clarifying questions, applies PMBoK 8 and Agile methodology, and produces ready-to-use documents.

**MVP covers 7 skills and 8 project management tasks:**

| Document | Project Phase | Description |
|----------|---------------|-------------|
| Project Charter | Initiation | Defines goals, scope, timeline, budget, team, and constraints |
| Risk Register (initial) | Initiation | Identifies risks with probability/impact scoring and response strategies |
| Project Plan | Planning | WBS, milestones, timeline, resource allocation |
| Communication Plan | Planning | Stakeholder matrix, communication schedule, escalation rules |
| Risk Register (detailed) | Planning | Enriches initial register with plan-based risks and refined assessments |
| Meeting Protocol | Any phase | Structures meeting notes into decisions, action items, and plan changes |
| Plan vs Actual Report | Closing | Compares planned and actual timelines, budget, and deliverables |
| Closure Report | Closing | Aggregates outcomes, deviations, realized risks, and lessons learned |

## Who It's For

Project managers, CPOs, product leads, and team leads who manage IT product development or launch projects and want to reduce time spent on routine documentation.

No technical background required. The agent works through natural language conversation in Claude.ai.

## How It Works

1. **Start a session** — tell the agent your project phase and current task.
2. **Provide project data** — brief, stakeholder answers, constraints, or any unstructured notes.
3. **Agent generates the document** — following the skill algorithm and template.
4. **Review and approve** — request revisions or approve the result.
5. **Move to the next task** — the agent suggests what's available based on the dependency map.

Skills are chained: the output of one skill feeds into the next. For example, the approved charter unlocks risk register and project plan generation.

## Methodology

The agent applies a hybrid of PMBoK 8 (process structure, artifact types, risk management) and Agile (iterative delivery, lightweight documentation, adaptive planning). Focused specifically on IT product development and launch projects.

## Supported Languages

The agent automatically detects the language of your request:

- **Russian** request → documents and responses in Russian
- **English** request → documents and responses in English

All templates are bilingual (RU/EN).

## Requirements

- Claude Pro or Max subscription
- Claude.ai Projects feature enabled

## Documentation

- [Installation Guide](docs/INSTALL.md) — step-by-step setup instructions
- [User Guide](docs/USER-GUIDE.md) — usage scenarios, commands, and examples
- [Русская версия](README.ru.md)

## License

MIT

---

**Keywords:** AI project manager, Claude AI skills, project management automation, PMBoK AI agent, project charter generator, risk register automation, project documentation AI, Claude.ai project management
