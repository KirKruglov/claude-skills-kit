> [Версия на русском языке](README.ru.md)

# claude-skills-kit

![GitHub stars](https://img.shields.io/github/stars/KirKruglov/claude-skills-kit?style=flat-square)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
![Skills](https://img.shields.io/badge/skills-24-informational?style=flat-square)
![Last commit](https://img.shields.io/github/last-commit/KirKruglov/claude-skills-kit?style=flat-square)

24 curated agent skills for Claude — designed for non-technical users: PMs, managers, and team leads.

---

## Quick Start

**Step 1.** Find a skill in the catalog below.

**Step 2.** Copy the skill folder to your workspace:

- **Cowork** — copy the skill folder into your Cowork workspace directory. Claude detects it automatically.
- **Claude.ai / Projects** — open the skill's `SKILL.md`, copy its content, and paste it into Project Instructions.

**Step 3.** Use Claude as usual. The skill activates based on your message — no commands needed.

> Each skill folder includes a `docs/INSTALL.md` with step-by-step instructions for your platform.

---

## Why Claude Skills Kit?

Most skill repositories contain only a `SKILL.md` file.
Claude Skills Kit ships a **complete package** per skill:

| What's included                | Why it matters                                           |
| ------------------------------ | -------------------------------------------------------- |
| `SKILL.md` — core instructions | Claude activates the skill                               |
| `README.md` (EN + RU)          | You know what the skill does before installing           |
| `docs/INSTALL.md`              | Platform-specific setup in 3 steps                       |
| `docs/USER-GUIDE.md`           | How to use the skill with examples                       |

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

| Skill | Link | Description |
| --- | --- | --- |
| project-management-kit | [→](skills/project-management-kit/) | AI Project Manager agent — 7 skills for project documentation (charter, risk register, project plan, communication plan, meeting protocol, plan-vs-actual report, closure report). PMBoK 8 + Agile. Bilingual EN/RU |
| project-onboarding | [→](skills/project-onboarding/) | Full project onboarding for Cowork: generates context.md, folder rules, file map, and starter prompts in one session. Bilingual EN/RU |

### Productivity & Workflow

| Skill                     | Link                                   | Description                                                                                                                                                                                         |
| ------------------------- | -------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| workspace-health-monitor  | [→](skills/workspace_health_monitor/)  | Audits a manager's workspace files to find orphaned files, forgotten action items, duplicates, and plan-to-reality drift. Bilingual EN/RU                                                           |
| delegation-brief          | [→](skills/delegation-brief/)          | Generates a structured task brief via 5-question interview — ready to paste into a new Cowork session. Bilingual EN/RU                                                                              |
| one-to-one-prep           | [→](skills/one-to-one-prep/)           | Generates a structured prep document for monthly 1-on-1 meetings: action item tracking, prioritized discussion topics, and wellbeing questions. Bilingual EN/RU                                     |
| decision-log              | [→](skills/decision-log/)              | Extracts structured decisions from meeting notes, Slack threads, or email chains — builds a clean log separate from action items. Two modes: new log and append with deduplication. Bilingual EN/RU |
| weekly-digest-synthesizer | [→](skills/weekly-digest-synthesizer/) | Compiles status updates from multiple .md/.txt files into a structured weekly digest — by project, with action items and blockers. Bilingual EN/RU                                                  |
| stakeholder-adapter       | [→](skills/stakeholder-adapter/)       | Adapts any document into audience-specific versions: Leadership (business impact, decision-focused), Engineering/Team (technical depth, actionable), Client (outcome language, no jargon). Bilingual EN/RU |
| hiring-pipeline-reviewer  | [→](skills/hiring-pipeline-reviewer/)  | Generates a structured weekly status report for all candidates in your hiring pipeline from interview notes and evaluation sheets. Flags stuck candidates, consolidates scores, and recommends next steps. Bilingual EN/RU |
| retro-pattern-analyzer    | [→](skills/retro-pattern-analyzer/)    | Analyzes sprint retrospective files to surface recurring pain points, unresolved action items, and positive patterns across sprints. Bilingual EN/RU |

### AI & Claude Mastery

| Skill | Link | Description |
| --- | --- | --- |
| feature-guide | [→](skills/feature-guide/) | Instantly explains any Claude feature or capability: what it is, where it's available, required plan, how to activate, limitations, and an applicability verdict. Bilingual EN/RU |
| memory-auditor-chat | [→](skills/memory-auditor-chat/) | Audits and cleans Claude.ai native memory: finds contradictions, outdated entries, duplicates, and noise in Memory Edits and Memory Summary. Bilingual EN/RU |
| memory-auditor-cowork | [→](skills/memory-auditor-cowork/) | Audits and cleans file-based memory in Cowork: auto-memory, CLAUDE.md, User Preferences, and Project Instructions. Bilingual EN/RU |

### Analysis & Review

| Skill | Link | Description |
| --- | --- | --- |
| report-analyzer | [→](skills/report-analyzer/) | Analyzes large PDF/PPTX reports and produces a structured summary with key data and insights |
| prd-review-challenger | [→](skills/prd-review-challenger/) | Devil's advocate for PRDs, feature specs, and product decisions — surfaces weak assumptions, open questions, implementation risks, and logical gaps before the document goes to the team. Bilingual EN/RU |
| prompt-builder | [→](skills/prompt-builder/) | Builds a structured prompt for any task via interactive Q&A |
| context-builder-cowork | [→](skills/context-builder-cowork/) | Generates a structured `project-context.md` file via interactive interview |
| user-feedback-synthesizer | [→](skills/user-feedback-synthesizer/) | Synthesizes user interview transcripts and feedback files (.md, .txt, .csv) into a prioritized insight report with themes, quotes, and open questions. Bilingual EN/RU |

---

## How to install a skill

### Option 1 — Git clone (recommended)

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

The skill folder will be at `skills/skill-name/`.

### Option 2 — Download a single skill folder

1. Open the skill folder in the repository
2. Download the `SKILL.md` file
3. Create a local folder with the skill name (e.g., `context-builder-cowork`)
4. Place `SKILL.md` inside that folder

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

Skills are currently authored and maintained by the repository owner.

To suggest a skill or report an issue — open a GitHub Issue with:
- A brief description of what the skill does
- An example trigger phrase
- The expected output

Pull requests are welcome once contributor guidelines are published.

---

## License

MIT
