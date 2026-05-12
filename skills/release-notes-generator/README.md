# Release Notes Generator

Turn a plain-language sprint summary into polished, user-facing release notes — no git, no CLI, no technical knowledge required.

Write your sprint results in a markdown file the way you normally would, and get 4 ready-to-send formats: a changelog entry, an email announcement, an in-app push notification, and a social post.

---

## Requirements

- A sprint summary or product update file (`.md` or `.txt`) in your Cowork workspace
- Works with: sprint retrospectives, product update notes, feature lists, handoff docs
- No API keys, no git access, no developer tools needed

---

## How to Use

1. Write your sprint results or product update in a `.md` or `.txt` file (plain language — no special format needed)
2. Place the file in your Cowork workspace
3. Trigger the skill with one of the phrases below
4. Claude reads the file, filters out internal/technical items, and generates 4 output formats
5. Copy and paste each format where you need it

---

## Examples

**Example 1: Sprint results → 4 ready formats**

> "Generate release notes from sprint-23-results.md"

Claude reads the file, filters out a "database migration" item and a "refactor auth module" item (not user-facing), and produces: a changelog entry for `v2.4.0`, an email with subject "Sprint 23: new report filters, faster CSV exports, and a small fix", a push notification "New in Reports: 3 filter options + faster exports. Check it out →", and a LinkedIn post opening with "Our Reports section just got a lot more useful."

**Example 2: Hotfix release**

> "Write release notes from hotfix-notes.md"

Claude detects the hotfix context from the filename, adjusts all 4 formats to a reassurance-first tone, and produces a push notification reading "Fixed: login error affecting some users. All systems normal."

---

## Triggers

| Language | Trigger Phrase |
|----------|---------------|
| EN | `generate release notes` |
| EN | `write release notes` |
| EN | `create release notes from` |
| EN | `turn sprint results into release notes` |
| EN | `release notes for version` |
| RU | `сгенерируй release notes` |
| RU | `напиши release notes` |
| RU | `создай релизные заметки` |
| RU | `оформи итоги спринта` |
| RU | `релизные заметки для версии` |

---

## What This Skill Does and Doesn't Do

**Does:**
- Reads plain `.md` or `.txt` sprint summaries — no special format required
- Filters out internal/technical items (refactors, infrastructure) and lists them separately
- Generates 4 output formats from one source: changelog, email, push notification, social post
- Adjusts tone for hotfix/patch releases (reassurance-first)
- Works entirely from local files — no git, no API calls

**Doesn't:**
- Work with `.docx` or `.pdf` files (export to `.txt` first)
- Pull from git commit history or Jira/Linear (file-based only)
- Auto-post to any channel (copy-paste workflow)
- Generate a blog post automatically (offers to add one after the 4 standard formats)
