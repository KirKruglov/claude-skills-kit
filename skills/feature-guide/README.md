# Feature Guide — Instant Claude Feature Cards for Any User

Stop searching docs. Get a structured answer about any Claude feature in seconds.

---

## What It Does

Claude Feature Scout turns questions like "does Claude have memory?" or "how do I use Projects?" into a clean, structured feature card — no documentation digging required.

Each card includes:
- What the feature does (plain language, no jargon)
- Where it's available (Claude.ai, Projects, Claude Code, mobile, etc.)
- Which plan you need (Free, Pro, Team, Enterprise)
- How to activate or use it
- Current limitations
- Up-to-date status (available, beta, Pro-only, announced)
- A verdict: does this feature fit your specific need?

The skill runs a live web search to pull the latest status directly from Anthropic's documentation — so you're never working from outdated information.

---

## How It Works

1. You describe a feature by name or describe what you want to do
2. The skill searches Anthropic's official docs for the current status
3. A structured feature card is returned — ready to act on
4. Optionally explore related features in the same session

---

## Quick Start

Open a conversation with Claude (with this skill installed) and try:

- "Does Claude have memory?"
- "What is the Projects feature?"
- "I want Claude to remember things between sessions"
- "Does Claude support voice?"
- "Can Claude create and save files?"

---

## Examples

**Input:** "Does Claude have memory?"

**Output:**
```
## Memory (Projects)

What it is: Claude can retain information across conversations when you use Projects.
  Each project has its own memory that persists between sessions.

Where available: Claude.ai — Free and Pro plans

How to use: Create a Project on claude.ai, then have conversations inside it.
  Claude will remember context from previous sessions within that project.

Limitations:
- Memory is scoped per project, not across all conversations
- Does not work in standard (non-project) conversations

Status: Available

Verdict: Fits — if you want Claude to remember context, Projects is the right feature.

Explore related features: Custom Instructions, Knowledge base?
```

---

## Requirements

- A Claude account (free or paid)
- Web search must be enabled in your Claude session for up-to-date status

No technical setup required. Works in Claude.ai, Claude Projects, Claude Cowork, and Claude Code.

---

## When to Use It

- Before spending 10 minutes in Anthropic's documentation
- When you're not sure if Claude can do something specific
- When a feature's status may have changed (beta → available, etc.)
- When onboarding someone new to Claude

---

## Installation

See [INSTALL.md](docs/INSTALL.md) for step-by-step setup instructions.
