> [Версия на русском языке](README.ru.md)

# claude-skills-kit

![GitHub stars](https://img.shields.io/github/stars/KirKruglov/claude-skills-kit?style=flat-square)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
![Skills](https://img.shields.io/badge/skills-11-informational?style=flat-square)


A growing collection of reusable skills for Claude — ready-to-use instruction files that extend Claude's behavior across any interface: Claude.ai, Claude Projects, API, or Cowork.

---

## What is a skill?

A skill is a folder containing a `SKILL.md` file with structured instructions for Claude. Add it to Claude.ai or Cowork — and Claude gains a new, reproducible capability without writing code.

Skills are:
- **Interface-agnostic** — work in Claude.ai, Projects, API, and Cowork
- **Self-contained** — each skill folder includes everything needed
- **Composable** — multiple skills can be combined in a single setup

---

## Skills

Each skill is available in two language versions. Claude activates the skill based on the language of the request — use the EN version for English, the RU version for Russian.

Example: the RU version of `prompt-builder` triggers on **"напиши промт"**, the EN version — on **"create a prompt"**.

| Skill | EN | RU | Description |
|-------|----|----|-------------|
| context-builder-cowork | [EN](skills/context-builder-cowork/) | [RU](skills/context-builder-cowork-ru/) | Generates a structured `project-context.md` file via interactive interview |
| prompt-builder | [EN](skills/prompt-builder/) | [RU](skills/prompt-builder-ru/) | Builds a structured prompt for any task via interactive Q&A |
| report-analyzer | [EN](skills/report-analyzer/) | [RU](skills/report-analyzer-ru/) | Analyzes large PDF/PPTX reports and produces a structured summary with key data and insights |
| project-onboarding | [EN/RU](skills/project-onboarding/) | — | Full project onboarding for Cowork: generates context.md, folder rules, file map, and starter prompts in one session. Bilingual EN/RU |
| project-management-kit | [Details](skills/project-management-kit/) | — | AI Project Manager agent — 7 skills for project documentation (charter, risk register, project plan, communication plan, meeting protocol, plan-vs-actual report, closure report). PMBoK 8 + Agile. Bilingual EN/RU |

More skills coming.

---

## Repository structure

```
claude-skills-kit/
├── skills/
│   ├── context-builder-cowork/       # EN
│   │   └── SKILL.md
│   ├── context-builder-cowork-ru/    # RU
│   │   └── SKILL.md
│   ├── prompt-builder/               # EN
│   │   └── SKILL.md
│   ├── prompt-builder-ru/            # RU
│   │   └── SKILL.md
│   ├── report-analyzer/              # EN
│   │   └── SKILL.md, README.md, ...
│   ├── report-analyzer-ru/           # RU
│   │   └── SKILL.md, README.md, ...
│   ├── project-onboarding/           # EN/RU (bilingual)
│   │   ├── SKILL.md
│   │   ├── README.md
│   │   ├── README.ru.md
│   │   └── resources/
│   └── project-management-kit/       # Skill kit (EN/RU)
│       ├── README.md
│       ├── system-prompt.md
│       ├── project-instructions.md
│       ├── docs/                     # INSTALL, USER-GUIDE
│       ├── generate-charter/         # 7 skills, each with
│       ├── generate-risk-register/   #   SKILL.md, README.md,
│       ├── generate-project-plan/    #   README.ru.md, templates/
│       ├── generate-comm-plan/
│       ├── generate-meeting-protocol/
│       ├── generate-plan-fact-report/
│       └── generate-closure-report/
├── README.md
└── README.ru.md
```

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
