# Weekly AI Workflow Review

Turn your week of Claude interactions into actionable insights: patterns, wins, and prompt templates for next week.

---

## Overview

Weekly AI Workflow Review analyzes your notes about tasks delegated to Claude and produces a structured reflection report. It identifies recurring task types, successful prompts, and interactions that required rework — then generates reusable prompt templates based on what worked. Use this skill when you want to understand how you're using AI each week, improve your prompting habits over time, or build a personal library of effective prompt patterns without any technical tools.

---

## Requirements

- A weekly task log in markdown or plain text format
  - Can be structured (numbered list, markdown bullets) or unstructured (paragraphs, notes)
  - Minimum content: task descriptions and what you asked Claude to do
  - Optional but recommended: note the outcome for each task (used as-is / edited / discarded)
- No external tools, APIs, or plugins required — works with plain text in chat

**Recommended:** Log at least 5 tasks per week for meaningful pattern detection. Even rough notes work: "asked Claude to draft a product email, had to rewrite the tone."

---

## How to Use

1. **Gather your weekly Claude task log**
   - Keep a simple running list during the week: task, prompt (or summary), result
   - Or collect notes from memory at week's end — even rough descriptions work

2. **Trigger the skill**
   - Say: "Weekly AI workflow review" or "Review my Claude interactions this week"
   - In Russian: "Еженедельный обзор AI-задач" or "Проанализируй мои задачи Claude за неделю"

3. **Provide your task log**
   - Paste the text directly in chat or upload a markdown file
   - No special format required — the skill parses structured and unstructured input

4. **Review the report**
   - You'll receive a structured reflection with: patterns, wins, improvement areas, and prompt templates
   - Optionally ask to save the report as `weekly-ai-review-YYYY-MM-DD.md` for future reference

---

## Examples

### Example 1: Simple weekly log (no outcome notes)

**Input:**
```
Week of April 14:
- Asked Claude to write a product update email for the team
- Had Claude summarize 3 competitor blog posts
- Used Claude to draft 5 LinkedIn post ideas
- Asked Claude to create a project status update
- Claude helped rewrite a job description
```

**Action:** Skill classifies tasks by type, identifies content/writing as dominant, flags that no outcome data is available, and generates prompt templates for the two most recurring task types (content writing, summarization).

**Output:**
```markdown
## Weekly AI Workflow Review
**Period:** Week of April 14  **Tasks analyzed:** 5

### Patterns of the Week
- Dominant task type: Content / Writing (4 tasks, 80%)
- Recurring topics: email drafting, LinkedIn posts
- Outcome data: unavailable — log outcomes next week for richer analysis

### Recommended Prompt Templates
1. For email drafting: "Write a [type] email for [audience]. Tone: [formal/casual]. Length: [X sentences]. Key points to cover: [list]. Do not include [constraints]."
2. For summarization: "Summarize the following [content type] in [N] bullet points. Focus on [angle]. Audience: [who will read this]."

### Takeaway
Content writing dominates your Claude usage. Adding outcome notes next week will unlock pattern analysis and help identify which prompts to reuse.
```

---

### Example 2: Detailed log with outcomes

**Input:**
```
- Product changelog draft → used without edits. Prompt: "Write a changelog for v2.3 features: [list]. Audience: developers. Format: markdown bullets."
- Executive summary for Q1 → rewrote 70%. Prompt: "Summarize Q1 results." Too vague.
- 3 interview questions for UX role → used 2 of 3. Good enough.
- Cold outreach email → discarded. Prompt: "Write a cold email." No context given.
- Weekly digest from 4 Slack threads → used as-is. Prompt: "Summarize these Slack messages into a digest for the team: [paste]."
```

**Action:** Skill identifies 2 successful prompts (changelog, digest), 2 pain points (executive summary, cold email), and generates specific improvement recommendations.

**Output:**
```markdown
## Weekly AI Workflow Review
**Period:** Current week  **Tasks analyzed:** 5

### Patterns of the Week
- Dominant task type: Content / Writing (5 tasks)
- Successful interactions: 3 (60%)
- Tasks requiring rework: 2 (40%)

### What Worked Well
- **Content writing:** Changelog draft used without edits. Prompt pattern: specific format + explicit audience + content list provided.
- **Summarization:** Weekly digest accepted as-is. Pattern: clear output format + full context pasted inline.

### Areas for Improvement
- **Executive summary:** Rewrote 70%. Cause: vague request — no format, length, or audience specified. Recommendation: "Summarize Q1 results in [N] paragraphs. Audience: [exec/board]. Focus on: [revenue/growth/risks]. Format: prose, no bullets."
- **Cold email:** Discarded. Cause: missing context — no recipient role, company, or goal. Recommendation: "Write a cold outreach email to [role] at [company type]. Goal: [outcome]. Tone: [direct/warm]. Length: under 150 words."

### Recommended Prompt Templates
1. For reports/summaries: "Summarize [content] in [N paragraphs/bullets]. Audience: [who]. Focus on: [key angle]. Format: [prose/bullets/table]."
2. For outreach/emails: "Write a [type] email to [recipient role]. Goal: [outcome]. Tone: [style]. Length: [X words]. Context: [brief background]."

### Takeaway
Prompts with explicit format + audience + constraints succeed consistently. Next week: apply the template above to all summary requests.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Weekly AI workflow review | Еженедельный обзор AI-задач |
| Review my Claude interactions this week | Проанализируй мои задачи Claude за неделю |
| What patterns in my AI usage | Какие паттерны в работе с Claude |
| Help me reflect on how I used Claude this week | Помоги разобрать как я использовал AI на этой неделе |
| Analyze my weekly Claude log | Разбери мой еженедельный лог задач Claude |

---

**Version:** 1.0.0  
**Last updated:** 2026-04-22
