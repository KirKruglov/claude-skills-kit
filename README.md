> [Русская версия](README.ru.md)

# claude-skills-kit

![GitHub stars](https://img.shields.io/github/stars/KirKruglov/claude-skills-kit?style=flat-square)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
![Skills](https://img.shields.io/badge/skills-2-informational?style=flat-square)


A growing collection of reusable skills for Claude — ready-to-use instruction files that extend Claude's behavior across any interface: Claude.ai, Claude Projects, API, or Cowork.

---

## What is a skill?

A skill is a folder containing a `SKILL.md` file with structured instructions for Claude. Add it to Claude.ai or Cowork — and Claude gets a new, repeatable capability without any code.

Skills are:
- **Interface-agnostic** — work in Claude.ai, Projects, API, or Cowork
- **Self-contained** — each skill folder includes everything Claude needs
- **Composable** — combine multiple skills in one setup

---

## Skills

Each skill is available in two language versions. Claude triggers the skill based on the language of your request — use the EN version for English, the RU version for Russian.

| Skill | EN | RU | Description |
|-------|----|----|-------------|
| context-builder-cowork | [EN](skills/context-builder-cowork/) | [RU](skills/context-builder-cowork-ru/) | Generates a structured `project-context.md` file via interactive interview |
| prompt-builder | [EN](skills/prompt-builder/) | [RU](skills/prompt-builder-ru/) | Builds a structured prompt for any task via interactive Q&A |

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
│   └── prompt-builder-ru/            # RU
│       └── SKILL.md
├── README.md
└── README.ru.md
```

---

## How to install a skill

### Option 1 — Git clone (recommended)
```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

The skill folder you need will be at `skills/skill-name/`.

### Option 2 — Download a single skill folder

1. Open the skill folder in this repository
2. Download the `SKILL.md` file
3. Create a local folder named after the skill (e.g. `context-builder-cowork`)
4. Place `SKILL.md` inside that folder

---

## How to add a skill to Claude.ai

> Requires Pro, Max, Team, or Enterprise plan with Code Execution enabled.

1. Go to **Settings → Capabilities** and make sure **Code Execution and File Creation** is on
2. Take the skill folder (e.g. `context-builder-cowork/`) and compress it into a ZIP file
   - The ZIP must contain the folder itself as root — not just the files inside it
3. Go to **Customize → Skills**
4. Click **"+"** → **"Upload a skill"**
5. Select the ZIP file
6. The skill will appear in your Skills list — toggle it on

Claude will automatically invoke the skill when your request matches its purpose.

---

## How to add a skill to Claude Cowork

1. Open Claude Cowork (desktop app)
2. Go to **Settings → Skills**
3. Click **"+"** → **"Upload a skill"**
4. Select the ZIP file prepared the same way as described above
5. Toggle the skill on

---

## Contributing

Skills are currently authored and maintained by the repository owner.

To suggest a skill or report an issue — open a GitHub Issue with:
- A short description of what the skill does
- Example trigger phrase
- Expected output

Pull requests are welcome once contribution guidelines are published.

---

## License

MIT
