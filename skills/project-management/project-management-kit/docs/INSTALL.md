# Installation Guide

Step-by-step instructions for setting up the AI Project Manager agent in Claude.ai.

## Prerequisites

- **Claude Pro or Max subscription** — required for the Projects feature
- **Claude.ai Projects** — available at [claude.ai](https://claude.ai) in the left sidebar

## Setup Steps

### Step 1. Create a New Project

1. Open [claude.ai](https://claude.ai).
2. In the left sidebar, click **Projects** → **New Project**.
3. Name the project (e.g., "Project Manager Agent").

### Step 2. Set Project Instructions

1. Open the project settings.
2. In the **Project Instructions** field, paste the contents of `project-instructions.md`.
3. Save.

This is the core prompt that tells Claude how to behave as a project manager.

### Step 3. Upload Knowledge Files

Upload the following files to the project's **Knowledge** section. Order matters — upload in the sequence listed.

**Required files:**

| # | File | Purpose |
|---|------|---------|
| 1 | `system-prompt.md` | Full agent instructions: task protocol, skills, file structure, communication rules |
| 2 | `skills/generate-charter/SKILL.md` | Skill: project charter generation |
| 3 | `skills/generate-charter/templates/project-charter-en.md` | Template: charter (EN) |
| 4 | `skills/generate-charter/templates/project-charter-ru.md` | Template: charter (RU) |
| 5 | `skills/generate-risk-register/SKILL.md` | Skill: risk register generation |
| 6 | `skills/generate-risk-register/templates/risk-register-en.md` | Template: risk register (EN) |
| 7 | `skills/generate-risk-register/templates/risk-register-ru.md` | Template: risk register (RU) |
| 8 | `skills/generate-project-plan/SKILL.md` | Skill: project plan generation |
| 9 | `skills/generate-project-plan/templates/project-plan-en.md` | Template: project plan (EN) |
| 10 | `skills/generate-project-plan/templates/project-plan-ru.md` | Template: project plan (RU) |
| 11 | `skills/generate-comm-plan/SKILL.md` | Skill: communication plan generation |
| 12 | `skills/generate-comm-plan/templates/comm-plan-en.md` | Template: communication plan (EN) |
| 13 | `skills/generate-comm-plan/templates/comm-plan-ru.md` | Template: communication plan (RU) |
| 14 | `skills/generate-meeting-protocol/SKILL.md` | Skill: meeting protocol generation |
| 15 | `skills/generate-meeting-protocol/templates/meeting-protocol-en.md` | Template: meeting protocol (EN) |
| 16 | `skills/generate-meeting-protocol/templates/meeting-protocol-ru.md` | Template: meeting protocol (RU) |
| 17 | `skills/generate-plan-fact-report/SKILL.md` | Skill: plan vs actual report |
| 18 | `skills/generate-plan-fact-report/templates/plan-fact-report-en.md` | Template: plan-fact report (EN) |
| 19 | `skills/generate-plan-fact-report/templates/plan-fact-report-ru.md` | Template: plan-fact report (RU) |
| 20 | `skills/generate-closure-report/SKILL.md` | Skill: closure report generation |
| 21 | `skills/generate-closure-report/templates/closure-report-en.md` | Template: closure report (EN) |
| 22 | `skills/generate-closure-report/templates/closure-report-ru.md` | Template: closure report (RU) |

**Optional files (improve session continuity):**

| File | Purpose |
|------|---------|
| `project-state.md` | Artifact status registry — helps the agent understand which documents are already approved |

### Step 4. Verify the Setup

Start a new chat within the project and send:

```
Generate a project charter. Here is the brief: we are building a mobile app for tracking personal fitness goals. Timeline: 4 months. Budget: $50,000. Team: 1 PM, 2 developers, 1 designer, 1 QA.
```

**Expected behavior:**

1. The agent reads `system-prompt.md` and the charter skill.
2. It may ask clarifying questions (stakeholders, constraints, success criteria).
3. It generates a structured charter document following the template.
4. It presents the result and asks for approval.

If the agent does not follow the template or ignores the skill instructions, verify that all knowledge files were uploaded correctly.

## File Structure Reference

```
project-name/
├── system-prompt.md          — full agent instructions
├── project-instructions.md   — compact prompt for Project Instructions field
├── skills/
│   └── {skill-name}/
│       ├── SKILL.md           — skill algorithm
│       └── templates/
│           ├── {name}-en.md   — English template
│           └── {name}-ru.md   — Russian template
├── input/                     — your project data (brief, answers, constraints)
├── output/                    — agent-generated documents
├── logs/
│   └── log.md                 — project log
└── project-state.md           — artifact status registry
```

## Troubleshooting

**Agent ignores skill instructions.** The most common cause is that the SKILL.md file was not uploaded to knowledge. Verify all files are listed in the project's Knowledge section.

**Agent produces unstructured output.** Make sure `system-prompt.md` is uploaded. It contains the task execution protocol that enforces structured output.

**Agent responds in the wrong language.** The agent detects language from your message. If you write in Russian, it responds in Russian. Switch language by writing your next message in the desired language.

**Knowledge file limit reached.** Claude.ai Projects have a knowledge file limit. If you hit it, prioritize: `system-prompt.md` first, then the skill files for the phase you are currently working on. You can swap skill files between phases.

## Next Steps

See the [User Guide](USER-GUIDE.md) for detailed usage scenarios, example commands, and workflow tips.
