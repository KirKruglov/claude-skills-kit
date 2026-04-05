# memory-auditor-cowork — User Guide

Audit all layers of Claude's file-based memory in Cowork to find and fix contradictions, outdated entries, duplicates, and noise.

---

## How to Start

Open a Cowork session and use one of these phrases:

- "audit memory"
- "memory health check"
- "review my memory entries"
- "check memory for issues"

Claude will recognize the skill and begin the workflow.

---

## Step-by-Step Walkthrough

1. **Context detection** — Claude automatically identifies your Cowork environment (project or standalone) and determines which memory layers are available: auto-memory files, CLAUDE.md, User Preferences, and Project Instructions.

2. **Overview** — Claude shows a structured summary: how many auto-memory files you have (broken down by type), key blocks in CLAUDE.md, and whether User Preferences and Project Instructions exist. You'll see a count of potential issues. You can stop here if you just want a quick check.

3. **Deep analysis** — If you confirm, Claude examines each entry across all available layers and classifies problems into four categories: contradictions, outdated data, duplicates, and noise. It also verifies MEMORY.md index consistency (broken links, orphaned files).

4. **Actions** — Claude presents findings grouped by priority in a fixed-format report. For auto-memory files, it proposes specific edit, delete, or merge operations. For other layers (CLAUDE.md, User Preferences, Project Instructions), it provides step-by-step manual instructions.

5. **Confirmation** — No changes happen without your explicit approval. You can approve actions one by one or say "apply all" (Claude will show the full list before executing). After each operation, MEMORY.md is automatically updated.

---

## What Gets Checked

| Layer | What Claude looks at | Can Claude fix it? |
|-------|---------------------|-------------------|
| auto-memory | MEMORY.md index, individual .md files (frontmatter + content) | Yes — edit, delete, merge files |
| CLAUDE.md | Global and project instructions | No — provides manual instructions |
| User Preferences | Personal settings in system prompt | No — instructions for Settings > Profile |
| Project Instructions | Project-specific instructions | No — instructions for project settings |

---

## Examples

### Example 1: Quick audit in a Cowork project

**You say:**
> audit memory

**Claude responds:**
> ### Cowork project Memory Audit
> **Context:** Cowork project
>
> | Layer | Status | Entries/Size | Notes |
> |-------|--------|-------------|-------|
> | auto-memory | found | 8 files: 3 user, 2 feedback, 2 project, 1 reference | ... |
> | CLAUDE.md | found | 45 lines | workspace setup, navigation rules |
> | User Preferences | found | present | language: Russian, style: direct |
> | Project Instructions | found | present | project rules, naming conventions |
>
> Found 5 potential issues. Proceed to detailed analysis?

### Example 2: Fixing auto-memory issues

**You say:**
> yes, show me the issues

**Claude responds:**
> | # | Layer | Category | Priority | Issue | Proposed Action |
> |---|-------|----------|----------|-------|-----------------|
> | 1 | auto-memory | Duplicate | Warning | feedback_style.md and user_preferences.md both state "direct communication style" | Merge into user_preferences.md |
> | 2 | auto-memory | Outdated | Error | project_status.md says "Phase 1" but Project Instructions say "Phase 3" | Delete project_status.md |
>
> **auto-memory (can modify):**
> - [#1] Merge feedback_style.md content into user_preferences.md, delete feedback_style.md, update MEMORY.md
> - [#2] Delete project_status.md, remove from MEMORY.md
>
> Confirm actions? (yes for all / yes for #N / reject #N)

---

## Tips for Best Results

- Run the audit periodically — auto-memory files accumulate over time, especially in active projects.
- Start with the overview to gauge the scope before diving into the full analysis.
- Check MEMORY.md index health — orphaned files and broken links are common after manual edits.
- Use "apply all" only after reviewing the full list.

---

## FAQ

**Q: Will the audit delete anything without my permission?**
A: No. Every change to auto-memory files requires your explicit "yes" or "apply all". For other layers, the skill only provides instructions — you make the changes yourself.

**Q: What if I don't have auto-memory set up yet?**
A: The skill will still audit other available layers (CLAUDE.md, User Preferences, Project Instructions). If none are available, it will inform you and end the audit.

**Q: How is this different from the regular memory-auditor?**
A: Regular memory-auditor works with Claude.ai native memory (Memory Edits, Memory Summary) using `memory_user_edits`. This version works with Cowork file-based memory (auto-memory, CLAUDE.md) using file tools (Read, Write, Edit).

**Q: What if I want to reset all memory at once?**
A: The skill will refuse this request. Full memory reset is irreversible. Instead, the skill helps you make targeted fixes to specific entries.

---

## Limitations

- Cannot directly edit CLAUDE.md, User Preferences, or Project Instructions — provides manual instructions instead.
- Does not analyze native Claude.ai memory (Memory Edits, Memory Summary) — use memory-auditor for that.
- Does not analyze or delete chat history.
- Works only in Cowork environments (desktop app or Claude Code).

---

## Need Help?

If the skill isn't working as expected, check the [installation guide](INSTALL.md) to make sure everything is set up correctly.
