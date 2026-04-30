> [Версия на русском языке](README.ru.md)

# claude-skills-kit

![GitHub stars](https://img.shields.io/github/stars/KirKruglov/claude-skills-kit?style=flat-square)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
![Skills](https://img.shields.io/badge/skills-35-informational?style=flat-square)
![Last commit](https://img.shields.io/github/last-commit/KirKruglov/claude-skills-kit?style=flat-square)

35 curated agent skills for Claude — designed for non-technical users: PMs, managers, and team leads.

> 28 standalone skills + 7 nested skills in `project-management-kit`

---

## Quick Start

**Step 1.** Find a skill in the catalog below.

**Step 2.** Copy the skill folder to your workspace:

- **Cowork** — copy the skill folder into your Cowork workspace directory. Claude detects it automatically.
- **Claude.ai / Projects** — open the skill's `SKILL.md`, copy its content, and paste it into Project Instructions.

**Step 3.** Use Claude as usual. The skill activates based on your message — no commands needed.

> See [INSTALL.md](INSTALL.md) / [INSTALL.ru.md](INSTALL.ru.md) for step-by-step setup.

---

## Why Claude Skills Kit?

Most skill repositories contain only a `SKILL.md` file.
Claude Skills Kit ships a **complete package** per skill:

| What's included                | Why it matters                                           |
| ------------------------------ | -------------------------------------------------------- |
| `SKILL.md` — core instructions | Claude activates the skill                               |
| `README.md` (EN + RU)          | You know what the skill does before installing           |
| `docs/USER-GUIDE.md`           | How to use the skill with examples (where applicable)    |
| `INSTALL.md` (EN + RU)         | Common setup guide in the repo root                      |

**Designed for non-technical users.** No code, no CLI, no configuration.
**Bilingual EN/RU.** Claude detects the language of your request automatically.

---

## What is a skill?

A skill is a folder containing a `SKILL.md` file with structured instructions for Claude. Add it to Claude.ai or Cowork — and Claude gains a new, reproducible capability without writing code.

Skills are:
- **Interface-agnostic** — work in Claude.ai, Projects, API, and Cowork
- **Self-contained** — each skill folder includes everything needed
- **Composable** — multiple skills can be combined in a single setup

---

## Skills

### Project Management

| Skill                     | Link                                   | Description                                                                                                                                                                                                         |
| ------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| project-management-kit    | [→](skills/project-management-kit/)    | AI Project Manager agent — 7 skills for project documentation (charter, risk register, project plan, communication plan, meeting protocol, plan-vs-actual report, closure report). PMBoK 8 + Agile. Bilingual EN/RU |
| project-onboarding        | [→](skills/project-onboarding/)        | Full project onboarding for Cowork: generates context.md, folder rules, file map, and starter prompts in one session. Bilingual EN/RU                                                                               |
| weekly-digest-synthesizer | [→](skills/weekly-digest-synthesizer/) | Compiles status updates from multiple .md/.txt files into a structured weekly digest — by project, with action items and blockers. Bilingual EN/RU                                                                  |
| context-builder-cowork    | [→](skills/context-builder-cowork/)    | Generates a structured `project-context.md` file via interactive interview                                                                                                                                          |
| okr-progress-narrator     | [→](skills/okr-progress-narrator/)     | Transforms raw OKR data (tables, lists, CSV, or pasted text) into a narrative stakeholder update: executive summary, per-objective narrative, KR status table, risks, and next steps. Bilingual EN/RU               |
| retro-pattern-analyzer    | [→](skills/retro-pattern-analyzer/)    | Analyzes sprint retrospective files to surface recurring pain points, unresolved action items, and positive patterns across sprints. Bilingual EN/RU                                                                |

#### Project Management Kit — 7 nested skills

| Skill                         | Link                                                               | Description                                                                                                                           |
| ----------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| generate-charter              | [→](skills/project-management-kit/generate-charter/)              | Generates a project charter — the foundational document of the Initiation phase. Bilingual EN/RU                                     |
| generate-risk-register        | [→](skills/project-management-kit/generate-risk-register/)        | Generates or updates a risk register with probability/impact scoring and response strategies. Bilingual EN/RU                         |
| generate-project-plan         | [→](skills/project-management-kit/generate-project-plan/)         | Generates a project plan with WBS, milestones, dependencies, and resource map. Bilingual EN/RU                                        |
| generate-comm-plan            | [→](skills/project-management-kit/generate-comm-plan/)            | Generates a communication plan with stakeholder matrix, communication schedule, and escalation rules. Bilingual EN/RU                 |
| generate-meeting-protocol     | [→](skills/project-management-kit/generate-meeting-protocol/)     | Generates a structured meeting protocol from free-form notes. Bilingual EN/RU                                                         |
| generate-plan-fact-report     | [→](skills/project-management-kit/generate-plan-fact-report/)     | Generates a plan-vs-actual variance report comparing planned and actual project data. Bilingual EN/RU                                 |
| generate-closure-report       | [→](skills/project-management-kit/generate-closure-report/)       | Generates a project closure report — the final artifact of the project lifecycle. Bilingual EN/RU                                     |

### Productivity & Workflow

| Skill                           | Link                                         | Description                                                                                                                                                                                                                |
| ------------------------------- | -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| workspace-health-monitor        | [→](skills/workspace-health-monitor/)        | Audits a manager's workspace files to find orphaned files, forgotten action items, duplicates, and plan-to-reality drift. Bilingual EN/RU                                                                                  |
| delegation-brief                | [→](skills/delegation-brief/)                | Generates a structured task brief via 5-question interview — ready to paste into a new Cowork session. Bilingual EN/RU                                                                                                     |
| one-to-one-prep                 | [→](skills/one-to-one-prep/)                 | Generates a structured prep document for monthly 1-on-1 meetings: action item tracking, prioritized discussion topics, and wellbeing questions. Bilingual EN/RU                                                            |
| decision-log                    | [→](skills/decision-log/)                    | Extracts structured decisions from meeting notes, Slack threads, or email chains — builds a clean log separate from action items. Two modes: new log and append with deduplication. Bilingual EN/RU                        |
| weekly-competitor-tracker       | [→](skills/weekly-competitor-tracker/)       | Tracks weekly competitor changes from your markdown notes — compares current vs. last-week snapshot and generates a delta-report with significance flags. No APIs required. Bilingual EN/RU                                |
| stakeholder-adapter             | [→](skills/stakeholder-adapter/)             | Adapts any document into audience-specific versions: Leadership (business impact, decision-focused), Engineering/Team (technical depth, actionable), Client (outcome language, no jargon). Bilingual EN/RU                 |
| hiring-pipeline-reviewer        | [→](skills/hiring-pipeline-reviewer/)        | Generates a structured weekly status report for all candidates in your hiring pipeline from interview notes and evaluation sheets. Flags stuck candidates, consolidates scores, and recommends next steps. Bilingual EN/RU |
| morning-standup-brief-generator | [→](skills/morning-standup-brief-generator/) | Compiles local notes, tasks, and project files into a structured daily standup brief — Yesterday / Today / Blockers / Questions. No connectors required. Bilingual EN/RU                                                   |
| team-update-aggregator          | [→](skills/team-update-aggregator/)          | Aggregates weekly updates from team members into a people-centric status report — organized by person, not by project. Progress, plans, blockers, capacity, and manager attention flags per team member. Bilingual EN/RU   |
| cowork-session-planner          | [→](skills/cowork-session-planner/)          | Generates a pre-session brief for Cowork by scanning project files — current status, session goal, and prioritised work plan before your first message. Bilingual EN/RU |
| meeting-prep-briefer            | [→](skills/meeting-prep-briefer/)            | Generates a structured per-meeting brief for every call in your day — participants, context from local files, open questions, and suggested agenda. Paste your schedule or point to a file. No integrations required. Bilingual EN/RU |

### AI & Claude Mastery

| Skill                     | Link                                   | Description                                                                                                                                                                              |
| ------------------------- | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| feature-guide             | [→](skills/feature-guide/)             | Instantly explains any Claude feature or capability: what it is, where it's available, required plan, how to activate, limitations, and an applicability verdict. Bilingual EN/RU        |
| memory-auditor-chat       | [→](skills/memory-auditor-chat/)       | Audits and cleans Claude.ai native memory: finds contradictions, outdated entries, duplicates, and noise in Memory Edits and Memory Summary. Bilingual EN/RU                             |
| memory-auditor-cowork     | [→](skills/memory-auditor-cowork/)     | Audits and cleans file-based memory in Cowork: auto-memory, CLAUDE.md, User Preferences, and Project Instructions. Bilingual EN/RU                                                       |
| session-handoff-composer  | [→](skills/session-handoff-composer/)  | Composes a structured handoff block from the current session when context fills up — decisions, tasks, open questions, and next steps ready to paste into a new session. Bilingual EN/RU |
| prompt-builder            | [→](skills/prompt-builder/)            | Builds a structured prompt for any task via interactive Q&A                                                                                                                              |
| weekly-ai-workflow-review       | [→](skills/weekly-ai-workflow-review/)       | Analyzes weekly notes about Claude-delegated tasks to surface delegation patterns, effective prompts, and optimization areas — with reusable prompt templates. Bilingual EN/RU           |
| context-window-health-check     | [→](skills/context-window-health-check/)     | Assesses current Claude session health and gives a plain-language status (🟢/🟡/🔴) with one concrete recommendation: keep working, create a handoff, or start fresh. No technical metrics. Bilingual EN/RU |

### Analysis & Review

| Skill                     | Link                                   | Description                                                                                                                                                                                               |
| ------------------------- | -------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| legal-matter-tracker      | [→](skills/legal-matter-tracker/)      | Scans workspace files by client or case name and assembles a chronological timeline of events with key facts — no integrations required. Bilingual EN/RU                                                  |
| report-analyzer             | [→](skills/report-analyzer/)             | Analyzes large PDF/PPTX reports and produces a structured summary with key data and insights                                                                                                              |
| research-folder-synthesizer | [→](skills/research-folder-synthesizer/) | Synthesizes a folder of mixed local files into a structured thematic report with themes, key findings, and gaps. Bilingual EN/RU                                                                          |
| prd-review-challenger     | [→](skills/prd-review-challenger/)     | Devil's advocate for PRDs, feature specs, and product decisions — surfaces weak assumptions, open questions, implementation risks, and logical gaps before the document goes to the team. Bilingual EN/RU |
| user-feedback-synthesizer | [→](skills/user-feedback-synthesizer/) | Synthesizes user interview transcripts and feedback files (.md, .txt, .csv) into a prioritized insight report with themes, quotes, and open questions. Bilingual EN/RU                                    |

---

## How to install a skill

### Option 1 — Git clone (full kit)

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

The skill folder will be at `skills/skill-name/`.

See [INSTALL.md](INSTALL.md) for sparse-checkout, single-skill download, and more options.

---

## How to add a skill to Claude.ai

> Requires a Pro, Max, Team, or Enterprise plan with Code Execution enabled.

1. Go to **Settings → Capabilities** and make sure **Code Execution and File Creation** is enabled
2. Take the skill folder (e.g., `context-builder-cowork/`) and compress it into a ZIP file
   - The ZIP must contain the folder itself as the root, not the files directly
3. Go to **Customize → Skills**
4. Click **"+"** → **"Upload a skill"**
5. Select the ZIP file
6. The skill will appear in the list — enable the toggle

Claude will automatically activate the skill when a request matches its purpose.

---

## How to add a skill to Claude Cowork

1. Open Claude Cowork (desktop app)
2. Go to **Settings → Skills**
3. Click **"+"** → **"Upload a skill"**
4. Select a ZIP file prepared as described above
5. Enable the toggle

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to suggest a skill, report a bug, or improve documentation.

---

## Community

| File | Purpose |
| ---- | ------- |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to suggest skills, report bugs, improve docs |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | Community standards |
| [SECURITY.md](SECURITY.md) | How to report security issues |
| [GitHub Discussions](https://github.com/KirKruglov/claude-skills-kit/discussions) | Questions, ideas, general discussion |

Issue templates and PR template are active automatically via `.github/`.

---

## License

MIT
