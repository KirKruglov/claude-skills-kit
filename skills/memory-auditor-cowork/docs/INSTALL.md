# How to Install memory-auditor-cowork

A step-by-step guide to adding **memory-auditor-cowork** to your Claude Cowork setup.

---

## What You Need

- A Claude account (free or paid)
- Claude Cowork desktop app

---

## Option 1: Claude Cowork (Desktop App)

1. Open the Claude desktop app
2. Navigate to **Settings > Skills** (or the skills folder)
3. Create a new folder named `memory-auditor-cowork`
4. Copy `SKILL.md` into this folder
5. Restart Claude or open a new session — the skill is now available

---

## Option 2: Claude Code (CLI)

1. In your project directory, create the skills folder if it doesn't exist:
   ```
   mkdir -p .claude/skills/memory-auditor-cowork
   ```
2. Copy `SKILL.md` into `.claude/skills/memory-auditor-cowork/`
3. The skill will be automatically picked up in your next Claude Code session

---

## Verify Installation

Start a new Cowork session and try one of these phrases:

- "audit memory"
- "memory health check"
- "аудит памяти"

If Claude responds with a memory overview showing layers (auto-memory, CLAUDE.md, User Preferences, Project Instructions), the installation is successful.

---

## Important Notes

This skill is designed specifically for **Cowork environments**. It works with file-based memory (auto-memory, CLAUDE.md) rather than native Claude.ai memory. If you use Claude.ai web interface, install [memory-auditor-chat](../memory-auditor-chat/) instead.

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Skill doesn't activate | Make sure you copied the **entire** SKILL.md content, including the YAML header |
| No auto-memory found | The `.auto-memory/` directory must exist with at least a `MEMORY.md` file |
| Wrong language | The skill supports both English and Russian — try your phrase in the other language |
| Skill suggests using memory_user_edits | You may have installed the wrong version — this skill uses file tools (Read/Write/Edit), not memory_user_edits |
