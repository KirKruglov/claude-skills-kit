---
name: prompt-builder
description: Interactive structured prompt generator for Claude based on the user's task description. Activate this skill when the user wants to create a prompt for Cowork or Claude.ai.
triggers:
  - "create a prompt"
  - "write a prompt"
  - "prompt builder"
language: en
interactive: true
version: 1.0
---

# Prompt Builder Skill

## Purpose
An interactive generator that builds structured prompts for Claude based on the user's task description. The skill asks questions, interprets loose answers, clarifies details, and assembles a ready-to-use prompt from a universal template.

## Instructions for Claude

### Step 1: Interactive interview

Ask questions in the order below. Wait for the user's answer after each question.

**Rules:**
- User answers may be unstructured or vague — interpret the intent
- If an answer is unclear or incomplete, ask a clarifying question
- Do not move to the next item until you have enough information
- Collect answers into variables for final generation

#### Question 1: Claude's role
```
What role should Claude take on in this task?
(E.g.: analyst, writer, tester, coder, etc.)
Describe what it will do in general terms.
```

**Action:** Interpret the answer, extract the role and core function. If the answer is too broad, ask: "If I understood correctly, Claude should act as [your interpretation]? Confirm or clarify?"

**Variable:** `ROLE`

---

#### Question 2: Context
```
What context does Claude need to understand the task?
(Background: why this matters, conditions, prerequisites?)
```

**Action:** Interpret as background and prerequisites. If the user says "it's clear from the task", ask: "Are there specific conditions, constraints, or history that affect the task?"

**Variable:** `CONTEXT`

---

#### Question 3: Main task
```
Specifically, what should Claude produce?
(Describe the exact result you need)
```

**Action:** Interpret as the primary goal. If the answer is vague, reframe: "So you need [your interpretation]?"

**Variable:** `TASK`

---

#### Question 4: Input data
```
What data or information will be passed to Claude?
(Text, table, list, description, nothing?)
```

**Action:** Interpret the format and type of input. If "it depends", ask: "Give an example of a typical input."

**Variable:** `INPUT`

---

#### Question 5: Output requirements
```
What should the result look like?
(Format: text, list, table, code, structured JSON, etc.)
(Length: brief, detailed, specific number of items?)
(Style: technical, plain language, with examples?)
```

**Action:** Interpret all three aspects. If only one is answered, ask about the others: "And the format? Length? Style?"

**Variable:** `OUTPUT`

---

#### Question 6: Constraints and tone
```
Are there any constraints or special requirements?
(What to avoid, tone, taboos, formatting restrictions?)
```

**Action:** Interpret as constraints and stylistic requirements. If "no constraints", ask: "Can Claude be creative? Is there a preferred style (formal/informal)?"

**Variable:** `CONSTRAINTS`

---

#### Question 7: Examples
```
Do you need input/output examples for clarity?
(If yes, provide one: what goes in, what's expected out)
```

**Action:** If "yes" — ask for an example. If "no" — skip, proceed to generation.

**Variable:** `EXAMPLES` (optional)

---

### Step 2: Generate the prompt

After collecting all answers, assemble the final prompt using this template:
```
## Role
[ROLE]

## Context
[CONTEXT]

## Task
[TASK]

## Input data
[INPUT]

## Output requirements
[OUTPUT]

## Constraints
[CONSTRAINTS]

[IF EXAMPLES COLLECTED:]
## Examples
[EXAMPLES]
```

---

### Step 3: Output and save

1. **Display the final prompt in chat** clearly and structured
2. **After the prompt, ask:**
```
   The prompt is ready. Do you want to save it as a .md file?
```
3. **If "yes":**
   - Suggest a filename (e.g.: `prompt-[short-description].md`)
   - Save the file via `present_files`
4. **If "no":**
   - Ask: "Do you need any edits to the prompt?"
   - If edits — return to the relevant step, update the variable, regenerate

---

## Key interpretation rules

- **Vague answers** → ask a clarifying question by rephrasing ("If I understood correctly...")
- **Unfilled fields** → apply default logic (e.g., if context is not important, write "Minimal context" or skip)
- **Special characters and formatting** → interpret the answer, apply correct formatting in the final prompt
- **Contradictions** → ask for clarification instead of assuming

---

## Usage examples

### Example 1: Prompt for code review
**User:** "I need a prompt to review code. Check for bugs, style, optimization."

**Claude interprets:**
- ROLE: Code reviewer
- TASK: Analyze code for bugs, style issues, and optimization opportunities
- etc.

### Example 2: Prompt for content writing
**User:** "I want a prompt for writing articles about cars. For a blog. Should be engaging."

**Claude interprets:**
- ROLE: Content writer for an automotive blog
- TASK: Write engaging articles about cars
- OUTPUT: Full-length article, conversational style
- etc.

---

## Cowork integration

Files are saved to `/home/claude/` and can be copied by the user into the project structure:
- For a project: `projects/[project-name]/resources/prompts/[prompt-name].md`
- For global use: `global/prompts/[prompt-name].md`
