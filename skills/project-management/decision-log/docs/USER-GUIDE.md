# decision-log — User Guide

Extract structured decisions from meeting notes, Slack threads, and email chains. Build a clean decision log that separates decisions from action items — with full context, alternatives, and participants.

---

## How to Start

Open a conversation with Claude and use one of these phrases:

- `"Extract decisions from this meeting: [paste notes]"`
- `"Decision log from these meeting notes"`
- `"Log decisions from this Slack thread"`
- `"Update my decision log with decisions from today's call"`
- `"Capture decisions from this email chain"`

Claude will recognize the skill and begin the workflow.

---

## Step-by-Step Walkthrough

**Step 1 — Paste your text.** Share your meeting notes, Slack thread, or email chain. The format doesn't matter — any unstructured text works.

**Step 2 — Choose a format (if not specified).** Claude will ask whether you want output as a table (one row per decision) or cards (one block per decision). If you already mentioned a preference, it will skip this question.

**Step 3 — Review extracted decisions.** Claude scans the text for decision points — moments where a choice was made, a direction was set, or an approach was agreed upon. Action items and informational statements are excluded.

**Step 4 — Append mode (optional).** If you paste an existing decision log along with new notes, Claude adds only new decisions and flags any duplicates.

---

## Examples

### Example 1: New log from meeting notes

**You say:**
> "Extract decisions from this meeting: We agreed to postpone the mobile release by two weeks due to the authentication bug. Denis suggested keeping the web release on schedule — everyone agreed. Backend team will use Redis for session caching going forward."

**Claude responds:**
> Found 2 decisions. Here is your decision log (cards format):
>
> **Decision 1: Postpone mobile release by two weeks**
> - Decision: Postpone the mobile release by two weeks
> - Context: Authentication bug not resolved
> - Alternatives: —
> - Participants: —
> - Date: —
> - Related: Authentication bug
>
> **Decision 2: Keep web release on schedule**
> - Decision: Web release proceeds as planned
> - Context: Denis proposed, team agreed
> - Alternatives: Postponing web release (rejected)
> - Participants: Denis + team
> - Date: —
> - Related: —

### Example 2: Append to existing log

**You say:**
> "Update my decision log with decisions from today's call:
> [existing log content]
> ---
> Today's notes: We decided to migrate to the new API gateway by end of Q2."

**Claude responds:**
> Found 1 new decision. 0 duplicates detected.
>
> Appended to your log:
>
> **Decision 4: Migrate to new API gateway by end of Q2**
> - Decision: Migrate to the new API gateway
> - Context: —
> - Alternatives: —
> - Participants: —
> - Date: —
> - Related: Q2 deadline

---

## What You Get

A structured decision log in your chosen format, ready to paste into:

- Confluence or Notion pages
- GitHub wikis or README files
- Project documentation folders
- Standalone `.md` files (use the template from `templates/decision-log-template.md`)

Each decision record includes up to six fields. Fields not mentioned in the source text are left blank — Claude does not invent information.

---

## Tips for Best Results

- The more context in your notes, the richer the output. Notes like "we decided X because of Y" produce better records than just "decided X."
- In append mode, paste the existing log first, then add a separator (`---`) before the new notes.
- If you want a specific date on all records, mention it once in your message: "Meeting on 2026-04-08."
- Use the table format if you plan to paste into Notion databases or spreadsheets. Use cards for Markdown documents.

---

## FAQ

**Q: Will Claude extract action items too?**
A: No. The skill focuses exclusively on decisions. Action items are a separate domain and intentionally excluded.

**Q: What if my notes are in Russian?**
A: The skill detects the language automatically and responds in the same language.

**Q: What if the text has no decisions?**
A: Claude will tell you clearly that no decisions were found — it will not generate placeholder records.

---

## Limitations

- Text input only — audio, video, and images are not supported
- Does not connect to Slack, email, or task trackers directly; you paste the text manually
- Does not assess the quality or correctness of decisions
- Does not make recommendations or suggest alternatives
- Fields left blank if the information is not present in the source text
