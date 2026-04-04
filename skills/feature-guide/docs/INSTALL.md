# How to Install feature-guide

A step-by-step guide to adding **feature-guide** to your Claude setup.

---

## What You Need

- A Claude account (free or paid)
- Access to one of: Claude.ai Projects, Claude Cowork, or Claude Code

---

## Option 1: Claude.ai (Projects)

1. Open [claude.ai](https://claude.ai) and sign in
2. Click **Projects** in the left sidebar
3. Create a new project or open an existing one
4. Click the **⚙ Project settings** icon
5. Scroll to **Custom instructions**
6. Copy the entire contents of the `SKILL.md` file and paste it into the instructions field
7. Click **Save**
8. Start a new conversation inside the project — the skill is now active

---

## Option 2: Claude Cowork (Desktop App)

1. Open the Claude desktop app
2. Navigate to **Settings → Skills** (or the skills folder)
3. Create a new folder named `feature-guide`
4. Copy `SKILL.md` into this folder
5. Restart Claude or open a new session — the skill is now available

---

## Option 3: Claude Code (CLI)

1. In your project directory, create the skills folder if it doesn't exist:
   ```
   mkdir -p .claude/skills/feature-guide
   ```
2. Copy `SKILL.md` into `.claude/skills/feature-guide/`
3. The skill will be automatically picked up in your next Claude Code session

---

## Verify Installation

Start a new conversation and try one of these phrases:

- "Does Claude have memory?"
- "What is the Projects feature?"
- "Can Claude create files?"

If Claude responds with a structured feature card (name, availability, how to use, limitations, status, verdict), the installation is successful.

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Skill doesn't activate | Make sure you copied the **entire** SKILL.md content, including the YAML header |
| Outdated information in cards | Ensure web search is enabled in your Claude session |
| Wrong language | The skill supports both English and Russian — try your phrase in the other language |
