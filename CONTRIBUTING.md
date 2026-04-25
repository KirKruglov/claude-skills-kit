# Contributing to claude-skills-kit

## Welcome

Skills in this repository are currently authored and maintained by the repository owner. The project is open to suggestions, bug reports, and documentation improvements from the community.

---

## How to suggest a new skill

Open a GitHub Issue using the **Skill Request** template. You'll be asked to provide:

- Skill name (kebab-case, e.g. `meeting-notes-summarizer`)
- What the skill does (1–2 sentences)
- Example trigger phrase
- Example input
- Expected output
- Target audience
- Existing alternatives (if any)

The issue is the right place to discuss and validate the idea before any implementation happens.

---

## How to report a bug

Open a GitHub Issue using the **Bug Report** template. You'll be asked to provide:

- Which skill
- Platform (Claude.ai / Cowork / Projects / API)
- Claude plan
- Steps to reproduce
- Expected vs. actual behavior
- Screenshots or output (optional)

---

## Documentation improvements

Open a GitHub Issue using the **Documentation** template if you find inaccurate, unclear, or missing content in any README, INSTALL, or USER-GUIDE file.

---

## Skill structure convention

If you submit a pull request with a new skill, follow this checklist:

- [ ] `SKILL.md` — required; contains the structured instructions Claude receives
- [ ] `README.md` (EN) — required; first line must be `> [Версия на русском языке](README.ru.md)`
- [ ] `README.ru.md` (RU) — required; first line must be `> [English version](README.md)`
- [ ] `docs/INSTALL.md` — only if setup for this skill differs from the root [INSTALL.md](INSTALL.md)
- [ ] `docs/USER-GUIDE.md` — where applicable
- [ ] Optional subdirectories: `templates/`, `resources/` — as needed

---

## Naming conventions

- Skill folder names: **kebab-case** (e.g. `decision-log`, `weekly-digest-synthesizer`)
- File names: **kebab-case**
- Language variants: `README.md` + `README.ru.md` (not `README-en.md`)

---

## Discussion & contact

For questions, ideas, and general discussion — use **[GitHub Discussions](https://github.com/KirKruglov/claude-skills-kit/discussions)** rather than Issues.

For Code of Conduct matters, see [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
For security issues, see [SECURITY.md](SECURITY.md).

---

## Review process

The author reviews issues and pull requests on a best-effort basis. There is no guaranteed response SLA.
