> [Версия на русском языке](README.ru.md)

# Campaign Retrospective Writer

Turn raw campaign metrics and notes into a structured marketing retrospective — in minutes, without any analytics tool.

---

## Overview

Campaign Retrospective Writer produces a structured post-campaign debrief from your pasted metrics and notes. It organises the results into six sections: goal vs. actual, channel breakdown, what worked and what didn't (with hypotheses), recommendations, and a one-line trend entry for tracking progress across campaigns. Use this skill when you need to wrap up a completed campaign, prepare a team debrief, share results with leadership, or build an archive of campaign learnings.

---

## Requirements

- Campaign metrics and/or qualitative notes (paste as plain text — no specific format required)
- Optional: campaign goal, channels used, and time period

**Works with:** email campaigns, paid ads, social media, events, content campaigns, or any marketing initiative.  
**No tools required:** no CSV upload, no dashboards, no integrations needed.

---

## How to Use

1. **Finish your campaign**
   - The skill is designed for *completed* campaigns; it will warn you if the campaign looks active

2. **Trigger the skill**
   - Say: `write campaign retrospective` or `campaign debrief`
   - In Russian: `напиши ретро по кампании` or `разбор кампании`

3. **Paste your data**
   - Drop in metrics, notes, or a summary of results — any format works
   - The skill will ask for missing context (goal, period, channels) if needed

4. **Review your retrospective**
   - Receive a six-section Markdown document ready to share or archive
   - All hypotheses are clearly labelled so facts and guesses stay separate

---

## Examples

### Example 1: Email Campaign Debrief

**Input:**
```
Q2 newsletter campaign, June 1–30.
Goal: CTR 2.0%, list size ~12,000.
Results: open rate 28% (was 24% last quarter), CTR 2.4%, unsubscribes 0.3%.
A/B test on subject lines — curiosity-style subject won by 18%.
No major complaints. Revenue attribution unclear.
```

**Output:**
```markdown
## Campaign Retrospective: Q2 Newsletter

**Type:** Email  
**Period:** 2026-06-01 — 2026-06-30  
**Channels:** Email

---

### 1. Goal vs. Result
| Metric       | Goal  | Actual | Δ%   |
|-------------|-------|--------|------|
| CTR         | 2.0%  | 2.4%   | +20% |
| Open Rate   | —     | 28%    | —    |
| Unsubscribes| —     | 0.3%   | —    |

### 2. Channel Breakdown
| Channel | Key Metric | Result | Verdict |
|---------|-----------|--------|---------|
| Email   | CTR       | 2.4%   | ✅      |

### 3. What Worked
- CTR exceeded goal by 20% — **(hypothesis): curiosity-style subject line drove higher open rates**

### 4. What Didn't Work
- Revenue attribution remains unclear — **(hypothesis): no UTM tracking on links**

### 5. Recommendations
**Repeat:** Curiosity-style subject lines; A/B testing cadence  
**Adjust:** Add UTM parameters to all links for attribution  
**Drop:** —

### 6. Trend Line
`Email Q2-2026: CTR 2.4%, +0.4pp vs. goal — A/B subject line test was the key driver`
```

---

### Example 2: Paid Social Campaign

**Input:**
```
Facebook + Instagram ads, May 15 – June 15.
Goal: 500 leads at CPL ≤ $20. Budget: $8,000.
Results: 380 leads, CPL $21.1. Top creative: video (60% of leads).
Static images underperformed — low CTR on all ad sets.
```

**Output:**
```markdown
## Campaign Retrospective: Paid Social — Lead Gen

**Type:** Paid  
**Period:** 2026-05-15 — 2026-06-15  
**Channels:** Facebook, Instagram

### 1. Goal vs. Result
| Metric | Goal    | Actual | Δ%    |
|--------|---------|--------|-------|
| Leads  | 500     | 380    | −24%  |
| CPL    | ≤$20.00 | $21.10 | +5.5% |

### 3. What Worked
- Video creatives drove 60% of leads — **(hypothesis): higher thumb-stop rate vs. static**

### 4. What Didn't Work
- Static images underperformed — **(hypothesis): banner blindness in the feed**

### 5. Recommendations
**Repeat:** Video-first creative strategy  
**Adjust:** Reallocate budget from static to video; test UGC-style video  
**Drop:** Static image ad sets

### 6. Trend Line
`Paid Social May–Jun 2026: 380 leads, CPL $21.1 (+5.5% over goal) — video dominates; drop statics next run`
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| write campaign retrospective | напиши ретро по кампании |
| campaign debrief | разбор кампании |
| analyze what worked in our campaign | что сработало в кампании |
| we just finished a campaign, help me review results | мы завершили кампанию, помоги разобрать результаты |

---

**Version:** 1.0.0  
**User Guide:** [docs/USER-GUIDE.md](docs/USER-GUIDE.md)
