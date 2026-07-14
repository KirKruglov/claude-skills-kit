# User Guide: Context Window Health Check

## What This Skill Does

This skill tells you whether your current Claude session is still running smoothly or whether it's time to wrap up. You get a simple status — green, yellow, or red — plus one clear action. Nothing technical required.

---

## Quick Start

Type any of these in chat:
- `check my context`
- `context health check`
- `is my context running out?`
- `should I start a new session?`

You can also just describe what you're experiencing:
- *"Claude, you seem to be forgetting our earlier decisions."*
- *"This session has been going on for a long time — should I start fresh?"*

---

## Scenarios

### Scenario 1: You've been working for a long time and want a quick check

**Situation:** You've been working with Claude for 30+ messages across several topics. Things seem fine, but you want to be proactive.

**What to do:**
1. Type: `context health check`
2. Read the status and explanation
3. If 🟢 → keep working
4. If 🟡 → type `session-handoff-composer` before your next major task

**Expected result:**
```
## Context Health

**Status:** 🟡 Caution

This session is running long and covers several different topics. Claude may start losing track of details from early in the conversation.

**Recommendation:** Create a handoff summary before starting the next major task.

→ Next step: Use session-handoff-composer to document key context before switching sessions.
```

---

### Scenario 2: Claude seems to have forgotten something

**Situation:** You noticed Claude gave an answer that contradicts something you discussed earlier, or it asked you to repeat information you already provided.

**What to do:**
1. Type: `you seem to be forgetting our earlier decisions — should I start a new session?`
2. The skill recognises this as a symptom and runs a full assessment
3. Follow the recommendation

**Expected result:**
```
## Context Health

**Status:** 🔴 Critical

You've reported that Claude is losing track of earlier context — this is a clear sign the session has exceeded reliable working memory.

**Recommendation:** Start a new session. Preserve your context first.

→ Next step: Use session-handoff-composer to capture key decisions and open items before switching.
```

---

### Scenario 3: You just started and want to know if you're safe

**Situation:** Early in a session, you just want to confirm things are fine before diving into a complex task.

**What to do:**
1. Type: `check my context`
2. Read the result

**Expected result:**
```
## Context Health

**Status:** 🟢 Healthy

Your session is fresh — only a few messages in. No context concerns at this point.

**Recommendation:** Your session is in good shape — keep working.
```

---

## Tips

1. **Use it proactively.** Don't wait for problems. Check after a long working session before starting a new major task.
2. **Pair with session-handoff-composer.** If you get 🟡 or 🔴, run `session-handoff-composer` next to preserve your work before starting fresh.
3. **Symptoms count.** You don't need to use the exact trigger phrase. If you describe what Claude is doing wrong (forgetting, repeating, contradicting), the skill picks that up automatically.
4. **Focus matters.** A long single-topic session is less risky than a short multi-topic one. The skill accounts for this.

---

## Frequently Asked Questions

**Can I see how many tokens I've used?**
No — exact token counts are not visible in the chat interface. The skill gives you a signal-based assessment instead, which is accurate enough for practical decisions.

**What's the difference between this skill and session-handoff-composer?**
This skill *diagnoses* whether your session needs a handoff. `session-handoff-composer` *creates* the handoff document. Use this one first, then handoff-composer if needed.

**Will this skill always be right?**
It reads visible signals — message count, topic diversity, symptoms you describe. It can be conservative (err toward caution). If you feel fine and get 🟡, use your judgement; the skill just flags the risk.
