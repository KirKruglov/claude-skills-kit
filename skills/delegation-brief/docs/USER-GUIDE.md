# delegation-brief — User Guide

Generate a structured 5-section task brief for Cowork in under 2 minutes — no technical knowledge required.

---

## How to Start

Open a conversation with Claude and use one of these phrases:

- "Create a delegation brief"
- "Help me delegate a task"
- "Structure my task for Cowork"
- "Write a brief"
- "I want to delegate"

Claude will recognize the skill and begin the workflow.

---

## Step-by-Step Walkthrough

**Step 1 — Claude asks 4 questions at once**

You'll see four questions covering: type of task, expected output, files involved, and restrictions. Select the closest option or type your own answer.

**Step 2 — Claude asks one final question**

What does success look like? Choose an option or describe it in your own words.

**Step 3 — Claude generates the brief**

You get a 5-section brief, ready to copy. Paste it at the start of a new Cowork session as your task instruction.

---

## Examples

### Example 1: Editing a document

**You say:**
> "Help me delegate a task"

**Claude responds:**
> (asks 4 questions — you select: "Modify an existing file", "Changes in the existing file", "Specific file", "Style and formatting")
> (asks final question — you select: "Changes made without errors")

**Brief generated:**
```
## Task Brief

**Task:** Make changes to an existing document preserving its style and formatting.

**Expected result:** Modified file with the requested changes applied.

**Files involved:** Specific file — to be named before starting.

**Off-limits:** Style and formatting.

**Success criteria:** Changes made without errors.
```

### Example 2: Creating something from scratch

**You say:**
> "Create a brief for a new task"

**Claude responds:**
> (asks 4 questions — you type: "Write a summary of last week's meeting", "A short text in chat", "No files", "Nothing critical")
> (asks final question — you type: "The summary captures all decisions and action items")

**Brief generated:**
```
## Task Brief

**Task:** Write a summary of last week's meeting.

**Expected result:** A short text in chat.

**Files involved:** Not specified.

**Off-limits:** No restrictions.

**Success criteria:** The summary captures all decisions and action items.
```

---

## What You Get

A plain-text brief with five sections that tell Claude exactly what to do, what format to use, what files to touch, what to avoid, and how to know the job is done. The brief is designed to be pasted directly into a new Cowork session.

---

## Tips for Best Results

- If you're not sure about a field, pick the closest option — you can always refine later
- The "Off-limits" section is the most important one: if you leave it blank, Claude may change things you didn't expect
- For complex tasks, run the skill twice — once for the overall brief, once for a specific sub-task
- After generating the brief, read it back before using it — if something doesn't match, ask Claude to adjust a specific section

---

## FAQ

**Q: Do I need to answer all 5 questions?**
A: Yes. If you skip a question or pick "I don't know", Claude will mark that section as "Not specified" in the brief — which is fine, but may lead to less precise results.

**Q: Can I edit the brief after it's generated?**
A: Yes. The brief is plain text in the chat. Copy it, open a text editor or just paste it into a new Cowork session and adjust the wording before hitting send.

**Q: Does this skill actually do the task?**
A: No. The skill only generates the brief — the actual task happens in a separate Cowork session where you paste the brief as your instruction.

---

## Limitations

- The skill does not access your files or file system
- It asks exactly 5 questions — no more, no fewer
- It does not estimate time, priority, or effort
- It does not save the brief to a file unless you explicitly ask
- The brief is a starting point — always review before using in a high-stakes session

---

## Need Help?

If the skill isn't working as expected, check the [installation guide](projects/claude-skills-kit/skills/delegation-brief/docs/INSTALL.md) to make sure everything is set up correctly.
