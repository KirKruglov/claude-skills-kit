# Changelog Narrator

Compare two versions of a business document and get a structured, human-readable changelog — no git, no CLI, no "Track Changes" required.

Designed for PMs, managers, operations leads, and freelancers who receive updated drafts and need to understand what changed without reading both documents side-by-side.

---

## Requirements

- Two document files in the Cowork workspace (`.md` or `.txt` format)
  - Old version (v1) and new version (v2) of the same document
  - Works with: PRDs, SOPs, strategy docs, contracts, meeting notes, policies, briefs
- No additional setup, API keys, or tools needed

---

## How to Use

1. Place both document versions in your Cowork workspace (or upload them)
2. Trigger the skill with one of the phrases below and mention the file names (or let Claude find them)
3. Claude identifies which file is v1 and which is v2 from the filenames — if ambiguous, it will ask
4. Claude compares both documents section-by-section and generates a structured changelog
5. Review the changelog: Summary → Added → Removed → Modified → Notes

---

## Examples

**Example 1: Comparing two PRD drafts**

> "What changed between versions?" + uploads `prd-v1.md` and `prd-v2.md`

Claude identifies `prd-v1.md` as the old version, reads both files, and outputs a changelog: Summary ("Scope was narrowed from 5 to 3 user segments; Success Metrics section fully rewritten; 2 risks added"), Added ("Risk Register" section with 2 new entries), Removed ("Out of Scope" bullet on mobile support), Modified ("Timeline: Q2 → Q3", "Target metric: 10% → 15% retention").

**Example 2: Comparing two SOP versions with a focus area**

> "Compare only the Escalation section in these two files" + `sop-draft.md` and `sop-final.md`

Claude reads both files, filters to the Escalation section, and outputs a scoped changelog covering only that section. A note in the output confirms: "Comparison limited to: Escalation."

---

## Triggers

| Language | Trigger Phrase |
|----------|---------------|
| EN | `compare these two documents` |
| EN | `what changed between versions` |
| EN | `generate a changelog` |
| EN | `show me the diff between these files` |
| RU | `сравни две версии документа` |
| RU | `что изменилось в документе` |
| RU | `сделай changelog` |
| RU | `покажи отличия между версиями` |

---

## What This Skill Does and Doesn't Do

**Does:**
- Compare any two `.md` or `.txt` files section-by-section
- Classify changes as Added, Removed, or Modified
- Describe what changed in plain language — no git diff syntax
- Handle tables (compares rows individually)
- Scope comparison to a specific section on request
- Document version-order assumptions in Notes

**Doesn't:**
- Produce visual or side-by-side diffs (use Diffchecker.com for that)
- Work with `.docx`, `.pdf`, or binary files
- Compare more than two documents at once
- Track who made the changes or when (no author/timestamp info without git)
