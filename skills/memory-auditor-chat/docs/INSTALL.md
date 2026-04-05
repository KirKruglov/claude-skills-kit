# How to Install memory-auditor-chat

A step-by-step guide to adding **memory-auditor-chat** to your Claude.ai setup.

---

## What You Need

- A Claude account (free or paid)
- Access to Claude.ai (web interface)

> **Note:** This skill is designed for Claude.ai. For Cowork, use [memory-auditor-cowork](../../memory-auditor-cowork/).

---

## Option 1: Claude.ai (Projects) — Recommended

1. Open [claude.ai](https://claude.ai) and sign in
2. Click **Projects** in the left sidebar
3. Create a new project or open an existing one
4. Click the **Project settings** icon
5. Scroll to **Custom instructions**
6. Copy the entire contents of the `SKILL.md` file and paste it into the instructions field
7. Click **Save**
8. Start a new conversation inside the project — the skill is now active

---

## Option 2: Claude.ai (General Chat)

1. Open [claude.ai](https://claude.ai) and sign in
2. Start a new conversation
3. Paste the entire contents of the `SKILL.md` file as your first message
4. Follow it with your trigger phrase (e.g., "audit memory")

> In general chat mode, the skill audits global Memory Edits and Memory Summary only. Project layers are not available.

---

## Verify Installation

Start a new conversation and try one of these phrases:

- "audit memory"
- "memory health check"
- "check my memory for issues"

If Claude responds with a memory overview showing your context and memory stats, the installation is successful.

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Skill doesn't activate | Make sure you copied the **entire** SKILL.md content, including the YAML header |
| Partial behavior | Verify you're using the skill in Claude.ai (web interface), not in Cowork |
| Wrong language | The skill supports both English and Russian — try your phrase in the other language |
| "Tool unavailable" message | The skill will switch to read-only mode automatically; this is expected in some environments |
