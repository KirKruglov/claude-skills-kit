# decision-log — Claude Skill for Extracting and Logging Decisions

> Automatically extract structured decisions from meeting notes, Slack threads, and email chains — and keep a clean decision log separate from action items.

---

## What It Does

**decision-log** scans any unstructured text (meeting notes, Slack threads, email chains) and extracts all decision points — not action items, not information, but actual decisions. For each decision, it captures six fields:

- What was decided
- Why it was decided (context and rationale)
- What alternatives were considered
- Who participated
- When it was decided
- What tasks or risks are related

The skill supports two modes: creating a new log from scratch, or appending new decisions to an existing log with automatic deduplication.

---

## How It Works

1. Paste your meeting notes or thread text
2. Optionally provide an existing decision log (for append mode)
3. Choose output format: table or cards
4. Get a clean, structured decision log ready to paste into Notion, Confluence, or any .md file

---

## Quick Start

Open a conversation with Claude and say:

- `"Extract decisions from this meeting: [paste notes]"`
- `"Log decisions from this Slack thread"`
- `"Update my decision log with decisions from today's call"`
- `"Decision log from these meeting notes"`

---

## Examples

**Input:**
> We decided to go with PostgreSQL instead of MongoDB due to the team's existing expertise. Alex and Maria were aligned. We considered Redis as a caching layer but agreed it's out of scope for now.

**Output (cards format):**
```
### Decision 1: Use PostgreSQL as the primary database

- **Decision:** Use PostgreSQL instead of MongoDB
- **Context:** Team has existing expertise with PostgreSQL
- **Alternatives:** MongoDB was considered but rejected; Redis considered for caching but out of scope
- **Participants:** Alex, Maria
- **Date:** —
- **Related:** —
```

---

## Requirements

- Claude account (any plan)
- Works with: Claude.ai Projects, Claude Cowork, Claude Code
- No external integrations required — text input only

---

## Output Formats

| Format | Best for |
|--------|----------|
| Table | Confluence, Notion databases, spreadsheets |
| Cards | Markdown docs, GitHub wikis, standalone .md files |

---

## Why a Separate Skill for Decisions?

Action items and decisions are different things. Action items track what someone will do. Decisions track what was agreed upon and why. Most AI meeting tools extract only action items. Six months later, no one remembers why a technical choice was made. decision-log captures that institutional memory automatically.

