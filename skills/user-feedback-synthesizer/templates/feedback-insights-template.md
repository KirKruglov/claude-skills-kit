# Feedback Insights — {date}

**Sources:** {file_count} files | **Signals extracted:** {signal_count} | **Themes identified:** {theme_count}
{notes}

---

## Executive Summary

{executive_summary_3_to_5_sentences}

---

## Themes

### 1. {theme_name} — {source_count} sources, {mention_count} mentions

- **Signal type:** {Pain | Desire | Compliment | Confusion | Split signal}
- **Description:** {what_users_say_about_this_theme}
- **Evidence:**
  - "{verbatim_quote}" — {source_file.md}
  - "{verbatim_quote}" — {source_file.md}

### 2. {theme_name} — {source_count} sources, {mention_count} mentions

- **Signal type:** {signal_type}
- **Description:** {description}
- **Evidence:**
  - "{verbatim_quote}" — {source_file.md}

<!-- Continue for each theme with source_count ≥ 2, ranked by source_count descending -->

---

## Prioritized Insights

| Priority | Insight | Theme | Sources |
|----------|---------|-------|---------|
| High | {insight_statement} | {theme_name} | {N} files |
| High | {insight_statement} | {theme_name} | {N} files |
| Medium | {insight_statement} | {theme_name} | {N} files |
| Low | {insight_statement} | {theme_name} | {N} files |

<!-- Priority: High = 3+ source files | Medium = 2 source files | Low = 1 source file (also listed in Open Questions) -->

---

## Open Questions

- {research_question_or_knowledge_gap}
- {single_source_signal_worth_investigating}
- {conflicting_signal_requiring_more_data}

---

## Files Processed

**Files included:** {list_of_processed_files}
**Files with no signals:** {list_or_None}
**Split signals flagged:** {list_or_omit_if_none}

---

<!-- 
FIELD RULES:
- Themes: ranked by source count (distinct files mentioning the theme), not total mentions
- Quotes: verbatim from source files — never paraphrase or summarize
- Insights: actionable statements — format: "[Signal type]: [context] [problem/need]"
- Priority: High ≥ 3 files | Medium = 2 files | Low = 1 file
- Executive Summary: describe top 2–3 themes and overall signal health (positive/mixed/critical)
- Notes in header (include if applicable):
    - "Pattern detection is limited with fewer than 3 sources"
    - "Large input: [N] files — review for completeness"
    - "Language mix: EN + RU signals processed"
    - "Focus area: [user-provided question]"
    - "No focus area specified — synthesizing all themes found"
-->
