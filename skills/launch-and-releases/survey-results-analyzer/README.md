> [Версия на русском языке](README.ru.md)

# Survey Results Analyzer

Turn raw survey CSV exports into structured insights — frequencies, themes, and Top-3 findings — without any code or data tools.

---

## Overview

Survey Results Analyzer reads a CSV file with survey responses and produces a structured markdown report covering quantitative analysis (frequency breakdowns, Likert means) and qualitative analysis (theme grouping from open-ended responses), plus a synthesized Top-3 insights summary. It auto-detects question types — close-ended vs. open-ended — so you don't need to configure anything. Use this skill when reviewing Google Forms, Typeform, or SurveyMonkey exports before stakeholder reporting, sprint reviews, or product decisions.

---

## Requirements

- A CSV file with survey data exported from any survey tool (Google Forms, Typeform, SurveyMonkey, etc.)
  - First row must be column headers (question text)
  - One row per respondent
  - At least 2 columns required
- File provided as an attachment or via workspace folder path
- No Python, no code, no additional tools required

**Works best with:** 10–200 respondents. Surveys with fewer than 5 respondents will be analyzed but flagged with a small-sample warning.

---

## How to Use

1. **Export your survey data as CSV**
   - In Google Forms: Responses → Download as CSV
   - In Typeform: Results → Export → CSV
   - In SurveyMonkey: Analyze → Export → All responses data

2. **Trigger the skill by saying:**
   - "Analyze survey results" and attach the CSV
   - Or: "I have a survey CSV to analyze"
   - In Russian: "Проанализируй результаты опроса"

3. **Provide the file**
   - Attach the CSV file directly, or share the path in your workspace folder
   - The skill will auto-detect column types and run both quantitative and qualitative analysis

4. **Review the report**
   - Receive `survey-analysis-{filename}.md` in your workspace folder
   - Report includes: summary table, per-question analysis, and Top-3 insights
   - Use insights directly in stakeholder presentations or product decisions

---

## Examples

### Example 1: NPS + Open-Ended Feedback Survey

**Input:** CSV with 3 columns — "Would you recommend us? (1–10)", "What do you like most?", "What should we improve?"

**Action:** Skill detects a Likert 1–10 column and two open-ended columns. Computes NPS-style mean, groups qualitative themes, synthesizes cross-column Top-3 insights.

**Output (excerpt):**
```markdown
## Quantitative Analysis

### Would you recommend us? (1–10)
**Mean:** 7.8 / 10

| Score | Count | % |
|-------|-------|---|
| 9–10  | 14    | 47% |
| 7–8   | 9     | 30% |
| 5–6   | 5     | 17% |
| 1–4   | 2     | 6% |

**Key finding:** 77% scored 7 or higher — solid satisfaction with room for improvement in the detractor segment.

## Top-3 Insights

### 1. Onboarding friction is the top improvement request
**Finding:** 42% of open-ended "improve" responses mention setup complexity or slow start.
**Implication:** This suggests prioritizing onboarding UX will have the highest impact on NPS lift.
```

---

### Example 2: Post-Sprint Team Satisfaction Survey

**Input:** CSV with 4 columns — "Sprint Rating (1–5)", "Process quality (1–5)", "Biggest blocker (open)", "Would you change anything? (open)"

**Action:** Skill detects two Likert columns and two open-ended columns. Computes means, distribution tables, theme clusters, and flags cross-column pattern between low process scores and communication-related themes.

**Output (excerpt):**
```markdown
## Qualitative Analysis

### Biggest blocker (open)
| Theme | Frequency | % | Example quote |
|-------|-----------|---|---------------|
| Communication gaps | 8 | 44% | "unclear who owns the decision" |
| Scope creep | 6 | 33% | "new tasks added mid-sprint again" |
| Tooling / CI issues | 4 | 22% | "deploys took 40 min, blocked testing" |

## Top-3 Insights
### 2. Process quality rating correlates with communication themes
**Finding:** Respondents rating process ≤ 3 were 3× more likely to cite "communication gaps" in open-ended answers.
**Implication:** This suggests a communication protocol improvement (e.g., clear DRI per task) would directly raise process satisfaction scores.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Analyze survey results | Проанализируй результаты опроса |
| Survey results analyzer | Анализ опроса |
| I have a survey CSV to analyze | У меня CSV с результатами опроса |
| What are the key insights from this survey | Какие главные выводы из этого опроса |
| Analyze this survey data | Проанализируй эти данные опроса |

---

**Version:** 1.0.0  
**Last updated:** 2026-05-19
