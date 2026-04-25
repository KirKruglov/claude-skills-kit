> [Версия на русском языке](INSTALL.ru.md)

# How to Install a Skill

Step-by-step guide to getting a skill and adding it to Claude.

---

## Part 1 — Get the skill files

Choose any option that fits your setup.

### Option 1 — Git clone (full kit)

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

All skill folders will be at `skills/<skill-name>/`.

### Option 2 — Git sparse-checkout (one skill, no full clone)

```bash
git clone --filter=blob:none --sparse https://github.com/KirKruglov/claude-skills-kit.git
cd claude-skills-kit
git sparse-checkout set skills/<skill-name>
```

For skills inside `project-management-kit`, use the nested path:

```bash
git sparse-checkout set skills/project-management-kit/generate-charter
```

### Option 3 — Browser download, no CLI

Open this URL in your browser (replace `<skill-name>` with the actual folder name):

```
https://download-directory.github.io/?url=https://github.com/KirKruglov/claude-skills-kit/tree/main/skills/<skill-name>
```

A ZIP with only that skill folder will download. Recommended for non-technical users.

### Option 4 — Single `SKILL.md` via curl

```bash
curl -O https://raw.githubusercontent.com/KirKruglov/claude-skills-kit/main/skills/<skill-name>/SKILL.md
```

Or: open the file on GitHub → click **Raw** → **Save As** in your browser.

### Option 5 — Full repo ZIP via GitHub UI

GitHub → **Code** → **Download ZIP** → extract the skill folder you need.

Simplest option, but downloads the entire repository.

---

## Part 2 — Add to your platform

### Claude.ai — Projects (recommended, any plan)

1. Open [claude.ai](https://claude.ai) and sign in
2. Click **Projects** in the left sidebar
3. Open or create a project
4. Click the **Project settings** icon → **Custom instructions**
5. Copy the entire contents of the skill's `SKILL.md` and paste it in
6. Click **Save**
7. Start a new conversation inside the project — the skill is active

### Claude.ai — Skills tab (ZIP upload)

> Requires a Pro, Max, Team, or Enterprise plan with Code Execution enabled.

1. Go to **Settings → Capabilities** and enable **Code Execution and File Creation**
2. Compress the skill folder into a ZIP file — the folder itself must be the root of the ZIP, not the files directly
3. Go to **Customize → Skills** → **"+"** → **"Upload a skill"**
4. Select the ZIP file
5. Enable the toggle — Claude will activate the skill automatically when a request matches

### Claude Cowork

**Option A — Auto-detection (recommended):**
Copy the skill folder into your Cowork workspace directory. Claude detects it automatically.

**Option B — Manual upload:**
1. Open Claude Cowork (desktop app)
2. Go to **Settings → Skills** → **"+"** → **"Upload a skill"**
3. Select a ZIP file prepared as described in the Skills tab section above
4. Enable the toggle

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Skill doesn't activate | Make sure you copied the **entire** `SKILL.md` content, including the YAML header at the top |
| Wrong behavior compared to README description | Some skills are platform-specific — check the skill's `README.md` for supported platforms |
| Wrong language | Skills support both EN and RU — try your trigger phrase in the other language |
| "Tool unavailable" message in Claude.ai | The skill will switch to read-only mode automatically; this is expected in some environments |
