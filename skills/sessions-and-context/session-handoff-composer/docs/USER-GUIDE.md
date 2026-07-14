# Session Handoff Composer User Guide

Learn how to carry your work context seamlessly into a new session.

---

## Quick Start

Here's the fastest way to create a handoff:

1. When your session is getting long, say: "Compose handoff"
2. Answer one clarifying question if the skill asks
3. Copy the markdown block you receive
4. Start a new session and paste the block as your first message

**Result:** A structured summary of your session that brings Claude up to speed instantly.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Session filling up mid-task

**Situation:**
You are a product manager drafting a feature spec in Cowork. The session started with research, moved into outlining, and now you're halfway through the draft. The session has grown long, Claude's context is filling up, and responses are starting to feel less focused. You need to continue the draft in a fresh session without losing any decisions or context.

**What to do:**

1. Notice the session slowdown and say: "Compose handoff"
   - No preparation needed — the skill reads the conversation automatically

2. The skill may ask one question
   - For example: "The acceptance criteria section was mentioned but I couldn't find a decision — did you finalize these?"
   - Answer briefly in one message

3. Copy the handoff block you receive
   - The block contains: what's done, what's in progress, open questions, files, and next steps
   - A ready-to-use opener line is included below the block

4. Start a new Cowork session
   - Paste the opener line first: *"Continue from: feature spec. Context below."*
   - Paste the handoff block immediately after
   - Claude will read it and continue exactly where you left off

**Expected result:**

You receive a block like:
```
### Done
- Problem statement written and approved
- User stories drafted (3 of 5)

### In Progress
- User story #4: edge case handling not resolved

### Next Steps
1. Finish user story #4 (handle the "no data" edge case)
2. Write acceptance criteria
3. Add metrics section
```

The new session starts with full context and zero repetition. You don't need to re-explain the task or re-read previous decisions.

**Why this works:** Instead of re-pasting old messages or re-explaining context, you get a compact, structured briefing that Claude can absorb in one message.

---

### Scenario 2: Pausing research to continue later

**Situation:**
You are a team lead doing competitive research on project management tools. You've been working for 90 minutes, covered 3 tools in depth, and need to stop for a meeting. You want to continue tomorrow in a new session and pick up exactly where you left off — including the tools you've already covered and the comparison table you still need to build.

**What to do:**

1. Before closing the session, say: "Session handoff — I need to continue tomorrow"

2. Review the generated handoff block
   - Check that all completed research is listed under "Done"
   - Check that the remaining tools appear under "Next Steps"
   - If anything is missing, mention it: "Also add: we decided to exclude Monday.com from scope"

3. Save the block to a scratch file or clipboard
   - You can paste it into a notes app to keep it safe overnight

4. Next day: open a new session, paste the opener line and the block, and continue

**Expected result:**

The handoff shows exactly which tools are done, which is next, and the open scope question. When you return, Claude reads the block and immediately continues the research on the next tool without any re-introduction.

**Why this works:** Even if you close the app, lose the session, or return days later, the handoff is a self-contained briefing. No session history required.

---

### Scenario 3: Switching focus within a long working session

**Situation:**
You are a content writer. You started a Cowork session working on a blog post draft, then mid-session you switched to editing a different article. The session now contains two separate workstreams, and context is getting mixed. You want to cleanly hand off the blog post work to a new session so you can focus on it without the editing thread polluting the context.

**What to do:**

1. Say: "Compose handoff for the blog post work only"
   - Specify which topic you want to extract

2. The skill will separate the blog post thread from the editing work
   - Multiple topics get separate sections in the handoff

3. Copy the relevant section of the handoff
   - Take only the blog post portion to start your new focused session

**Expected result:**

A handoff that separates the two workstreams, letting you start a clean session for the blog post with only the relevant context.

**Why this works:** Long sessions often drift across topics. The handoff makes the separation explicit, so your next session starts clean.

---

## Tips

### Tip 1: Trigger early, not at the last moment

Don't wait until Claude is clearly struggling to keep up. Trigger the handoff when you notice responses getting less precise or when the session has been running for 30+ minutes on a complex task. An early handoff is cleaner than a late one — the skill has more room to read and organize the context.

**Pro tip:** You can trigger it preemptively as a "checkpoint" even if you plan to keep the current session going. Just save the block and use it if needed.

### Tip 2: Add missing context before copying

After you see the handoff block, read it quickly. If something critical is missing (a decision you made verbally, a constraint you mentioned early), add it in the same message: "Also add to Open Questions: we haven't decided on the publishing date." The skill will update the block before you copy it.

### Tip 3: Keep the opener line and the block together

Always paste the opener line first, then the handoff block. The opener line signals to Claude that this is a continuation session — it sets the right mode immediately. Without the opener, Claude will read the block as raw data rather than as a continuation briefing.

---

**Version:** 1.0.0
**Last updated:** 2026-04-19
