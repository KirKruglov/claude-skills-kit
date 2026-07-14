# User Guide: Changelog Narrator

## Quick Start

Here's the fastest way to get a changelog:

1. Place two versions of your document in the Cowork workspace (e.g., `prd-v1.md` and `prd-v2.md`)
2. Say: "What changed between versions?" — Claude will find the files automatically
3. Review the changelog: Summary tells you the big picture; Added / Removed / Modified give you the details

**Result:** A structured changelog you can paste into a Slack message, email, or meeting notes.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Reviewing an updated PRD before a sprint planning meeting

**Situation:** Your product team just sent you PRD v2 before tomorrow's sprint planning. You have 10 minutes and need to understand what changed since v1 to run the meeting effectively.

**What to do:**
1. Save both files to your Cowork workspace: `prd-v1.md` and `prd-v2.md`
2. Type: "What changed between versions?" (or just "generate a changelog")
3. Claude reads both files, identifies v1 vs. v2 from the filenames, and outputs the changelog
4. Scan the Summary first — it tells you the scope in 2–3 sentences
5. Review Modified entries for changes to timelines, metrics, and scope
6. Check Added for new sections (new requirements, new risks) and Removed for dropped items

**Expected result:** A changelog you can use directly in the meeting: "Since v1, the timeline shifted to Q3, the target metric was raised to 15%, and a new Risk Register section was added."

---

### Scenario 2: Tracking changes in a vendor contract across drafts

**Situation:** You're negotiating a vendor contract. Legal sent you a revised draft (`contract-draft-2.md`) alongside the original (`contract-draft-1.md`). You want to know what changed before the call.

**What to do:**
1. Convert the contract text to `.txt` or `.md` and place both files in the Cowork workspace
2. Type: "Compare these two documents — contract-draft-1.md is the older version"
3. Claude reads both files, uses your hint to set version order, and generates the changelog
4. Focus on the Modified section: changed clauses, updated payment terms, revised liabilities
5. Check Removed: clauses that disappeared from the new draft

**Expected result:** A plain-language summary of which clauses changed and how — no legal jargon in the changelog itself, just the facts ("Payment terms: Net 30 → Net 60", "SLA guarantee removed from Section 4").

---

### Scenario 3: Auditing a revised SOP for one specific section

**Situation:** Operations sent an updated SOP. You only care about the Escalation Procedures section — it's the one your team owns.

**What to do:**
1. Place both SOP files in the Cowork workspace
2. Type: "Compare only the Escalation Procedures section in sop-v1.md and sop-v2.md"
3. Claude scopes the comparison to that section only — the rest of the document is ignored
4. Review the scoped changelog

**Expected result:** A focused changelog for just the Escalation Procedures section, with a note confirming the scope limitation.

---

## Tips

**Name your files clearly.** Files like `strategy-v1.md` / `strategy-v2.md` or `policy-old.md` / `policy-new.md` let Claude determine version order automatically. Ambiguous names (like `strategy-a.md` / `strategy-b.md`) require a short clarification from you.

**Use the focus-area option for long documents.** If your document has 20 sections and you only care about 2, say so upfront: "Compare only the Goals and Risks sections." This gives you a tighter, more useful output.

**Paste the Summary into your update.** The 2–3 sentence Summary is designed to be copy-paste ready for Slack, email, or meeting agendas. You don't have to rephrase it.
