# feature-guide — User Guide

Structured feature cards for any Claude capability, on demand. Ask in plain language — get a clear answer with status, availability, and a verdict.

---

## How to Start

Open a conversation with Claude and use one of these phrases:

- "Does Claude have memory?"
- "What is the Projects feature?"
- "Can Claude create files?"
- "Does Claude support voice?"
- "I want Claude to remember context between sessions"
- "Scout: custom instructions"

Claude will recognize the skill and begin the workflow.

---

## Step-by-Step Walkthrough

**Step 1 — You ask about a feature**
Write the feature name or describe what you want to accomplish. No special format required.

**Step 2 — Claude identifies the feature**
If you used a feature name, Claude proceeds directly. If you described a need, Claude maps it to the closest feature and confirms with a single question if there's ambiguity.

**Step 3 — Live status lookup**
Claude searches Anthropic's official documentation for the current status, availability, and activation steps.

**Step 4 — Feature card is returned**
You receive a structured card with all key information. No follow-up needed.

**Step 5 — Optional: explore related features**
At the end of the card, Claude may suggest 1–2 related features to explore next.

---

## Examples

### Example 1: Feature name query

**You say:**
> "What is the Projects feature in Claude?"

**Claude responds:**
> ## Projects
>
> **What it is:** Projects is a workspace in Claude.ai that groups conversations and gives Claude persistent memory within that workspace. Useful for ongoing work that requires continuity.
>
> **Where available:** Claude.ai — Free and Pro plans
>
> **How to use:** Click "Projects" in the left sidebar on claude.ai, create a project, and have conversations inside it. Claude will remember context from previous sessions.
>
> **Limitations:**
> - Memory is scoped per project only
> - Does not work in standard conversations outside Projects
>
> **Status:** Available
>
> **Verdict:** Fits — if you want persistent context for an ongoing project, this is the right feature.
>
> Explore related features: Custom Instructions, Knowledge base?

### Example 2: Need-based query

**You say:**
> "I want Claude to remember things I've told it before"

**Claude responds:**
> That maps to the **Projects** feature (persistent memory per workspace) or **Custom Instructions** (fixed context injected into every conversation). Which matches your use case better — ongoing project memory, or always-on preferences?

---

## What You Get

A structured feature card for every query, containing:
- Feature name (official)
- Plain-language description
- Platform and plan availability
- Step-by-step activation instructions
- Known limitations
- Current status (available, beta, Pro-only, announced)
- A verdict on whether the feature fits your specific need

---

## Tips for Best Results

- Be specific: "Does Claude support voice in the mobile app?" gets a better card than "voice"
- Describe your goal if you don't know the feature name: "I want Claude to use my files as context"
- Ask one feature at a time — the skill generates one card per request
- If web search is unavailable, the card will be marked as based on training data — check the official docs for the latest status

---

## FAQ

**Q: What if the feature I'm asking about doesn't exist?**
A: The card will show Status: Not found, and Claude will suggest 1–2 related features that might fit your need.

**Q: Can I ask in Russian?**
A: Yes. The skill detects the language of your query and responds in the same language. Both English and Russian are fully supported.

**Q: Will the information be up to date?**
A: The skill runs a live web search against Anthropic's official docs. If web search is unavailable, the card is marked with "Training data — status may be outdated."

---

## Limitations

- Does not compare Claude to other AI products (ChatGPT, Gemini, etc.)
- Does not provide pricing details — only which plan a feature requires
- Does not configure or enable features on your behalf
- Generates one feature card per request
- Requires web search access for accurate, current status
