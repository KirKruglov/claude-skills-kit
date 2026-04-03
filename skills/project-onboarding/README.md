# project-onboarding

Full project onboarding for Claude Cowork in one session.

Generates a complete working environment: `context.md`, folder instructions, file map, and starter prompt templates — based on an interactive interview and automatic folder scanning.

## Problem

Setting up a new project in Claude Cowork requires manually creating context files, writing rules, mapping file structures, and preparing prompt templates. This is repetitive and easy to do inconsistently.

## Solution

One skill that handles the entire onboarding flow:

1. **Interactive interview** — captures project goals, structure, constraints, and stakeholders
2. **Automatic file map** — scans the project folder and generates a structured file index
3. **Folder instructions** — generates project rules based on project type (analytics, content, business, personal)
4. **Starter prompts** — creates reusable prompt templates matched to the project type

## Modes

| Mode | Triggers | Output |
|------|----------|--------|
| `new` | «создай проект», «новый проект», «настрой проект» / "create project", "new project", "set up project" | Full interview → context.md + folder-instructions.md + file map + prompts |
| `quick` | «быстрый контекст», «создай контекст проекта» / "quick context", "create project context" | Blocks 1–3 + auto-scan → context.md |
| `scan` | «обнови карту файлов», «пересканируй» / "update file map", "rescan files" | File map update only → patches existing context.md |

## Output files

```
project-folder/
├── context.md                  # Project context with auto-generated file map
├── folder-instructions.md      # Rules tailored to project type
└── resources/
    └── prompts/
        ├── analyze-data.md     # Example for analytics projects
        ├── write-post.md       # Example for content projects
        └── ...
```

## Installation

### Claude.ai (Skills)

1. Download `project-onboarding.zip` from [Releases](../../releases)
2. Go to **Settings → Capabilities → Skills**
3. Upload the zip file
4. The skill appears in your Skills list

### Claude Cowork / Claude Code

Copy the skill folder to your personal skills directory:

```bash
cp -r project-onboarding ~/.claude/skills/project-onboarding
```

Or install from this repository:

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
cp -r claude-skills-kit/project-onboarding ~/.claude/skills/
```

## Skill structure

```
project-onboarding/
├── SKILL.md                        # Main skill instructions (English)
└── resources/
    ├── context-template-ru.md      # context.md template — Russian
    ├── context-template-en.md      # context.md template — English
    ├── rules-templates-ru.md       # Rule sets by project type — Russian
    ├── rules-templates-en.md       # Rule sets by project type — English
    ├── prompt-templates-ru.md      # Starter prompts by project type — Russian
    └── prompt-templates-en.md      # Starter prompts by project type — English
```

## Supported project types

| Type | Rules focus | Starter prompts |
|------|------------|-----------------|
| Analytics | Data integrity, source attribution, structured conclusions | `analyze-data.md`, `compare-sources.md` |
| Content | Brand voice, drafts workflow, platform adaptation | `write-post.md`, `adapt-post.md` |
| Business | Hypothesis tracking, decision logging, stakeholder communication | `research-topic.md`, `prepare-summary.md` |
| Personal | Minimal rules, speed-first | No prompts (too diverse — use `prompt-builder` instead) |

## Universal rules (included in all types)

- **File discovery** — Claude auto-finds files by description instead of requiring exact paths
- **Input protection** — input files are read-only, no modifications
- **Language & style** — matches the detected request language (Russian or English); direct, no unsolicited suggestions

## Usage examples

**Full onboarding:**
```
> создай проект
```
Claude runs the full interview (8 blocks), scans the folder, generates all files.

**Quick context:**
```
> быстрый контекст
```
3 blocks of questions + auto file scan → minimal `context.md`.

**Update file map after adding new files:**
```
> пересканируй файлы
```
Re-scans the folder and updates the file map section in existing `context.md`.

## Compatibility

- Claude.ai (Pro, Max, Team, Enterprise) — via Skills upload
- Claude Cowork — via `~/.claude/skills/`
- Claude Code — via `~/.claude/skills/` or `.claude/skills/`
- Follows the open [Agent Skills](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) standard (SKILL.md format)

## Language

The skill supports **English and Russian** natively.

- `SKILL.md` — English (skill instructions and triggers)
- Templates in `resources/` — available in both `-ru` and `-en` versions

At runtime, the skill detects the request language and selects the matching template set automatically. All generated output matches the detected language.

## Related skills

- **prompt-builder** — interactive generator for custom prompts (separate skill, no overlap)
- **report-analyzer** — analysis of large PDF/PPTX reports

## License

MIT
