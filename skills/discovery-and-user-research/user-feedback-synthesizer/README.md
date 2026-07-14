> [Версия на русском языке](README.ru.md)

# user-feedback-synthesizer

Turn a folder of interview transcripts, support tickets, and survey files into a structured insight report — without spending two days tagging and clustering manually.

---

## What It Does

`user-feedback-synthesizer` reads your feedback files (`.md`, `.txt`, `.csv`) and produces a single report with:

- **Themes ranked by frequency** — how many sources mention each topic
- **Verbatim quotes** as evidence per theme
- **Prioritized insights** table (High / Medium / Low by source count)
- **Open questions** — gaps, conflicting signals, single-source findings worth investigating

The output file `feedback-insights-YYYY-MM-DD.md` is ready to share with your team or paste into a planning doc.

---

## Requirements

- One or more feedback files in `.md`, `.txt`, or `.csv` format
- Files should contain user interview transcripts, support ticket exports, survey responses, or any freeform feedback text
- `.csv` files need a header row; content column will be auto-detected

---

## How to Use

1. Trigger the skill with one of the phrases below
2. Provide a folder path or list of files
3. Optionally specify a focus area: "focus on onboarding pain points"
4. Claude processes all files and saves `feedback-insights-YYYY-MM-DD.md` to your working folder

---

## Examples

**Example 1 — Analyze a folder of interview transcripts**

> "Synthesize feedback from interviews/ folder"

Claude reads all `.md` and `.txt` files in `interviews/`, clusters themes, and outputs:
- 5 themes ranked by frequency
- Top quotes per theme
- Prioritized insights table
- Open questions based on gaps and conflicting signals

**Example 2 — Survey CSV with a research question**

> "User feedback report from q1-survey.csv — focus on checkout experience"

Claude reads `q1-survey.csv`, extracts signals related to checkout, surfaces themes from survey responses, and flags insights and open questions specific to that flow.

---

## Triggers

| English | Russian |
|---------|---------|
| `synthesize feedback` | `синтезируй фидбек` |
| `analyze user interviews` | `разбери транскрипты интервью` |
| `user feedback report` | `отчёт по пользовательскому фидбеку` |
| `I have interview transcripts and need insights` | `у меня есть транскрипты интервью, нужны инсайты` |

---

## Output

`feedback-insights-YYYY-MM-DD.md` with sections:

- **Executive Summary** — 3–5 sentence overview
- **Themes** — ranked list with signal type, description, and verbatim quotes
- **Prioritized Insights** — table with Priority / Insight / Theme / Sources
- **Open Questions** — knowledge gaps and single-source signals to investigate
- **Files Processed** — list of processed files and files with no signals
