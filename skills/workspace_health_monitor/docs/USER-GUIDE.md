# workspace_health_monitor — User Guide

Audit your manager's workspace: find forgotten tasks, orphaned files, and conflicting information
across your notes, plans, and logs — in one structured report.

---

## How to Start

Open a conversation with Claude and use one of these phrases:

- "Run a workspace health check on my notes"
- "Find forgotten action items in my files"
- "Audit my workspace — I'll paste my meeting notes"
- "Weekly cleanup — check for orphaned files"
- "Workspace hygiene check"

Claude will recognize the skill and begin the workflow.

---

## Step-by-Step Walkthrough

**Step 1 — Provide your files**
Claude will ask how you want to share your files. Choose one:
- In Cowork: grant folder access and Claude reads files directly
- Upload files to the conversation
- Paste file contents as text

**Step 2 — Provide active projects (optional)**
Claude may ask: "List your currently active projects — just names is enough."
This helps Claude distinguish orphaned files from active ones. You can skip this step — Claude will infer projects from your files.

**Step 3 — Claude scans and analyzes**
Claude reads all provided files and runs four analyses:
- Which files aren't connected to any active project
- Which action items in notes were never transferred to a task tracker
- Which files duplicate or conflict with each other
- What's the overall clutter level

**Step 4 — Receive the report**
Claude delivers a formatted audit report with five sections and an overall clutter score.

---

## Examples

### Example 1: Weekly note audit

**You say:**
> "Here are my meeting notes from the past 3 weeks. Run a workspace health check."

**Claude responds:**
> "I've scanned 12 files. Here's the audit report:
> **Score: Moderate** — several forgotten commitments found.
> Orphaned files (2): 'Q1-planning-draft.md', 'team-offsite-ideas.md' — no link to active projects.
> Forgotten action items (4): 'Follow up with Dima on budget approval' (meeting-2026-03-18.md), ...
> Duplicates (1): 'roadmap-v2.md' and 'roadmap-final.md' — nearly identical content, recommend keeping the newer one.
> Recommendations: ..."

### Example 2: Quick check before quarter review

**You say:**
> "Before the Q2 planning, audit my workspace. Active projects: Discovery Phase, Onboarding Redesign, Q2 OKRs."

**Claude responds:**
> "Running audit against 3 active projects...
> Score: Clean — workspace is in good shape.
> 1 orphaned file found: 'competitor-analysis-jan.md' — likely from a completed initiative.
> No forgotten action items detected.
> Recommend archiving the competitor analysis file."

---

## What You Get

A structured audit report containing:

- **Orphaned files** — name, last date mentioned, reason flagged
- **Forgotten action items** — exact wording, source file, date if available
- **Duplicates and conflicts** — which files overlap, which is likely more current
- **Cleanup recommendations** — prioritized: Critical (commitments with names) → Important (conflicts) → Suggested (archiving)
- **Clutter score** — Clean / Moderate / Cluttered / Chaos with one-line summary

---

## Tips for Best Results

- The more complete the files you provide, the more accurate the audit
- Include files from the past 2–4 weeks for the most useful results
- If you list active projects explicitly, the orphaned file detection becomes much more precise
- Run this weekly — 10–15 minutes of audit saves hours of confusion later
- After the audit, ask Claude: "Help me draft the action item transfers to [task tracker]"

---

## FAQ

**Q: What if I don't have many files — is the skill useful?**
A: Yes. Even 3–5 files can contain forgotten action items or conflicting information. The skill scales to input size.

**Q: Can Claude delete or move files after the audit?**
A: No. The skill produces recommendations only. All file operations are your decision.

**Q: What if all my files are connected to active projects?**
A: Claude will report "no orphaned files found" and focus on action items and conflicts. A clean result is still useful.

---

## Limitations

- Does not connect to Jira, Asana, Linear, or other task trackers
- Does not analyze binary files (images, archives) without readable text content
- With more than 50 files, Claude prioritizes by date and file type
- Detection quality depends on how much context is in the files themselves
- Does not retain file state between sessions — run fresh each time

---

## Need Help?

If the skill isn't working as expected, check the [installation guide](INSTALL.md) to make sure everything is set up correctly.
