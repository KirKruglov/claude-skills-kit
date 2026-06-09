> [Версия на русском языке](README.ru.md)

# Content Performance Reporter

Turn your weekly analytics CSV exports into a readable narrative report: what worked, what didn't, and what to do next week. No code, no dashboards, no API connections required.

Designed for marketers, SMM managers, and content creators who export data and need editorial insight — not more raw numbers.

---

## Requirements

- One or more CSV files from your analytics platform in the Cowork workspace (uploaded or in the selected folder)
- No additional setup, API keys, or tools needed

---

## How to Use

1. Export your weekly analytics as CSV from your platform(s)
2. Upload the file(s) to your Cowork workspace (or confirm they're in the selected folder)
3. Trigger the skill with one of the phrases below
4. Claude detects the platform, extracts metrics, and generates the report
5. Review the narrative and recommendations — no follow-up questions needed

---

## Examples

**Example 1: weekly report**

> "Content performance report" + <name>.csv`

Claude detects  from column headers, identifies the primary metric (Reach), finds the top 3 and bottom 3 posts, calculates total reach and average ER, and outputs: What Worked ("Video Reels averaged 2× more reach than carousels"), What Didn't Work ("Text-only posts had the lowest ER: 1.1%"), Pattern of the Week ("Short-form video dominated top performers"), and a concrete recommendation.

**Example 2: Multi-platform weekly review**

> "Analyze my content performance" + uploads `ga4-weekly.csv` + `linkedin-may.csv`

Claude generates a separate section for Google Analytics (Sessions, Top pages) and LinkedIn (Impressions, Top posts), then a combined Summary: which platform drove the most traffic, where engagement was highest, and what to prioritize next week.

---

## Triggers

| Language | Trigger Phrase |
|----------|---------------|
| EN | `content performance report` |
| EN | `analyze my content performance` |
| EN | `what worked this week` |
| EN | `weekly content report` |
| EN | `compile my analytics` |
| EN | `content analytics report` |
| RU | `отчёт по контенту` |
| RU | `что сработало на этой неделе` |
| RU | `анализ контент-аналитики` |
| RU | `еженедельный отчёт по контенту` |
| RU | `скомпилируй аналитику` |
| RU | `отчёт по перформансу контента` |

---

## What This Skill Does and Doesn't Do

**Does:**
- Detect the platform automatically from CSV column headers
- Identify Top 3 and Bottom 3 content items by primary metric
- Calculate aggregate metrics: total reach/views, average engagement rate
- Compare to previous week if data is available (no invented deltas)
- Write a narrative analysis in plain business language
- Handle multiple platforms in a single run

**Doesn't:**
- Generate charts or visual dashboards (paste the table into Sheets to visualize)
- Connect to platform APIs directly
- Compare against industry benchmarks (no external data)
- Export to .docx or .pptx formats (markdown output only)
- Modify or overwrite your original CSV files
