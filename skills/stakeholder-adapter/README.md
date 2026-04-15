# stakeholder-adapter — One Document, Every Audience

Stop rewriting the same document for every room you walk into. `stakeholder-adapter` takes your working document and generates ready-to-send versions for Leadership, Engineering, and your Client — each tuned to what that audience actually needs.

---

## What It Does

Most documents are written for one audience and then awkwardly forwarded to others. Executives skim past technical detail. Engineers miss the decision buried in business prose. Clients get confused by internal terminology.

`stakeholder-adapter` fixes this by applying audience-specific framing rules to your existing document:

- **Leadership / Executives** — business impact first, decision-focused, milestone-level timeline, no implementation noise
- **Engineering / Team** — full technical depth, structured by task and owner, concrete deadlines, blockers surfaced
- **Client / External partner** — outcome language, no jargon, clean prose, ends with clear next steps

The source content stays intact. The skill reframes it, not rewrites it.

---

## How It Works

1. Paste your document or provide a file path
2. Choose which audience versions you need (one, two, or all three)
3. Optionally specify document type and any key message that must appear in every version
4. Get all adapted versions in one response, clearly labeled and ready to use

---

## Quick Start

Open a conversation with Claude and say:

> "Adapt this document for leadership and the client: [paste your document]"

or

> "I need different versions of this status update for executives, the team, and the client"

Claude will guide you through the rest.

---

## Examples

**Before:**
> Status update pasted — written for the engineering team, includes sprint tasks, bug IDs, and internal blockers.

**After — Leadership version:**
> **For information.**
> Phase 2 backend is on track for April 22 delivery. One infrastructure dependency (CDN config) is resolved; no blockers remain. Budget impact: within plan. No action required.

**After — Client version:**
> We're on track for the April 22 delivery. Infrastructure setup is complete, and the team is in final testing. **Next steps:** we'll share a preview link by April 19 for your sign-off.

---

## Requirements

- Claude account (free or paid)
- Claude Cowork (recommended for file input)
- No external tools or APIs required
- Supported input formats: pasted text, `.md`, `.txt`

---

## Who It's For

- **Product managers** who write specs and updates that need to reach multiple stakeholders
- **Team leads** preparing status reports for both executives and engineers
- **Project managers** adapting proposals and plans for clients and internal teams
- **Business analysts** translating technical findings into executive or client language

---

## Installation

See [docs/INSTALL.md](docs/INSTALL.md) for step-by-step setup instructions.

---

## Related Skills

- [delegation-brief](../delegation-brief/) — structure a vague task before starting work
- [prd-review-challenger](../prd-review-challenger/) — stress-test a PRD before sharing it
- [one-to-one-prep](../one-to-one-prep/) — prepare for a 1-on-1 meeting with your report

---

[🇷🇺 Русская версия](README.ru.md)
