# User Guide: Prompt Library Curator

## Quick Start

1. Type one of these phrases: `organize my prompts`, `prompt library`, or `tag my prompts`
2. Paste your prompts — or say which file they're in
3. Done. You receive a structured `prompt-library.md` catalog

---

## Scenario 1: Organising a Growing Prompt Collection

**Situation:** You've been collecting Claude prompts for months — some in a notes app, some saved in a `.txt` file. The collection has grown to 30+ prompts and you can't find things quickly anymore.

**What to do:**
1. Copy all your prompts into one text block (separate them with blank lines)
2. Say: *"organize my prompts"* and paste the block
3. The skill assigns a category, 2–4 tags, a one-line summary, and a complexity rating to each prompt
4. You receive `prompt-library.md` with an index table and prompts grouped by category

**Expected result:**
- Index table sorted by category and complexity
- Each prompt named and tagged for easy scanning
- Duplicates flagged — you decide which to keep

---

## Scenario 2: Building a Team Prompt Library

**Situation:** You're preparing a shared prompt reference for your team. You have a `team-prompts.md` file with 15 prompts your team uses regularly, but it's unsorted and has no descriptions.

**What to do:**
1. Say: *"structure my prompt collection — the file is team-prompts.md"*
2. The skill reads the file, categorises and tags each prompt
3. It preserves your original prompt text exactly — no edits to the wording

**Expected result:**
- A structured catalog ready to share
- Quick Find navigation (if >20 prompts)
- Template prompts (those with `{{variables}}`) automatically tagged `template`

---

## Scenario 3: Periodic Library Refresh

**Situation:** Your prompt library exists but has grown stale — you've added new prompts as comments at the bottom without categorising them.

**What to do:**
1. Paste only the new, uncategorised prompts
2. Say: *"tag my prompts"*
3. Receive a catalog for the new batch — then manually merge it with your existing library

**Tip:** You can re-run the skill on your full library at any time to regenerate the index table and recheck for duplicates.

---

## Tips

- **Separate prompts clearly** — blank lines or `---` between prompts gives the best split results
- **Include placeholder variables** — prompts like `"Summarise {{document}} for {{audience}}"` are detected as templates and tagged automatically
- **Don't edit existing prompts before running** — paste raw; the skill organises without touching your wording
- **Use the Duplicates section** — when two prompts serve the same purpose, the skill flags them so you can decide which to keep or merge

---

## Output File Structure

The skill produces `prompt-library.md` with this structure:

```
# Prompt Library
Last updated: YYYY-MM-DD | Total prompts: N | Categories: X | Duplicates: Y

## Quick Find (if N > 20)
[Writing] · [Research] · [Coding] · ...

## Index
| # | Category | Summary | Tags | Complexity |

## Writing
### [Prompt name]
tags: ... | complexity: ...
[original prompt text]

## Duplicates
[flagged near-duplicates, or "No duplicates detected."]
```
