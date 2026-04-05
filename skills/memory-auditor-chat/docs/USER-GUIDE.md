# memory-auditor-chat — User Guide

Audit all layers of Claude's native memory in Claude.ai to find and fix contradictions, outdated entries, duplicates, and noise.

---

## How to Start

Open a conversation with Claude and use one of these phrases:

- "audit memory"
- "memory health check"
- "review my memory entries"
- "check memory for issues"

Claude will recognize the skill and begin the workflow.

---

## Step-by-Step Walkthrough

1. **Tool & context detection** — Claude checks whether `memory_user_edits` is available, then identifies your environment (Claude.ai project or general chat) and determines which memory layers are accessible.

2. **Overview** — Claude shows a structured summary: how many Memory Edits you have, key themes in Memory Summary, and whether Project Summary or Project Instructions exist. You'll see a count of potential issues. You can stop here if you just want a quick check.

3. **Deep analysis** — If you confirm, Claude examines each entry across all available layers and classifies problems into four categories: contradictions, outdated data, duplicates, and noise. Cross-layer verification catches conflicts between Memory Edits, Memory Summary, Project Summary, and Project Instructions.

4. **Actions** — Claude presents findings in a structured report grouped by priority. For Memory Edits: specific delete or replace operations. For other layers: step-by-step manual instructions since these cannot be edited programmatically.

5. **Confirmation** — No changes happen without your explicit approval. You can approve actions one by one or say "apply all" (Claude will show the full list before executing).

---

## Examples

### Example 1: Quick audit in a project

**You say:**
> audit memory

**Claude responds:**
> ### Claude.ai Project Memory Audit
> **Context:** Claude.ai project
> **Date:** 2026-04-05
>
> | Layer | Status | Entries | Notes |
> |-------|--------|---------|-------|
> | Memory Edits | found | 12 entries | ... |
> | Memory Summary | found | present | brand voice, content calendar, team roles |
> | Project Summary | found | present | ... |
> | Project Instructions | found | present | ... |
>
> Found 4 potential issues. Proceed to detailed analysis?

### Example 2: Fixing contradictions

**You say:**
> yes, show me the issues

**Claude responds:**
> | # | Layer | Category | Priority | Issue | Proposed Action |
> |---|-------|----------|----------|-------|-----------------|
> | 1 | Memory Edits | Contradiction | Error | Entry #3 "Preferred tone: formal" contradicts #8 "Use casual tone" | Replace #3 with "Tone: casual for content, formal for external" |
>
> **Memory Edits (can modify):**
> - [#1] Replace entry #3. Confirm?

---

## What You Get

A structured audit report following a fixed template: layer overview, prioritized issue table (errors first, then warnings, then recommendations), concrete actions for Memory Edits (delete/replace with confirmation), and manual instructions for layers that cannot be edited programmatically.

---

## Tips for Best Results

- Run the audit periodically — memory accumulates noise over time, especially in active projects.
- Start with the overview to gauge the scope before diving into the full analysis.
- Use "apply all" only after reviewing the full list — it saves time but make sure every proposed change is correct.
- In a project, all four layers are audited. In general chat, only Memory Edits and Memory Summary are available.

---

## FAQ

**Q: Will the audit delete anything without my permission?**
A: No. Every change to Memory Edits requires your explicit "yes" or "apply all". For other memory layers, the skill only provides instructions — you make the changes yourself.

**Q: Can I run the audit in a general chat (no project)?**
A: Yes. The audit will cover global Memory Edits and Memory Summary. Project-specific layers won't be available.

**Q: What if I want to reset all memory at once?**
A: The skill will refuse this request. Full memory reset is irreversible. Instead, the skill helps you make targeted fixes to specific entries.

**Q: What happens if `memory_user_edits` is not available?**
A: The skill switches to read-only mode automatically. It will analyze all visible layers and provide manual instructions for fixes instead of auto-applying changes.

---

## Limitations

- Cannot directly edit Memory Summary, Project Summary, or Project Instructions — provides manual instructions instead.
- Limited to 5 `conversation_search` queries per audit to avoid excessive context usage.
- Works only with Claude.ai native memory layers — does not work with file-based auto-memory, CLAUDE.md, or local files (use memory-auditor-cowork for that).
- Cannot delete chats — only flags them with recommendations.

---

## Need Help?

If the skill isn't working as expected, check the [installation guide](INSTALL.md) to make sure everything is set up correctly.
