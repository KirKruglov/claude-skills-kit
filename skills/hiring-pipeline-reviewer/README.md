# Hiring Pipeline Reviewer

Turn scattered interview notes into a structured weekly candidate status report — with flags, scores, and clear next steps.

---

## Overview

Hiring Pipeline Reviewer generates a structured status report for all candidates in your hiring pipeline from interview notes and evaluation sheets. It consolidates scores, identifies stuck candidates, and recommends concrete next steps for each person — all in one scan. Use this skill when preparing for your weekly recruiter sync, deciding which candidates to advance or decline, or reviewing your pipeline after a round of interviews.

---

## Requirements

- Interview notes or evaluation sheets (plain text, .md, or .txt)
  - Can be pasted directly in chat or provided as a file
  - One block of notes covering all candidates, or separate notes per candidate
  - Notes can be unstructured — the skill will attempt to parse candidate boundaries
- Optional: position title, hiring criteria, custom "stuck" threshold (default: 5 days)

**Works best with:** Notes covering 3–15 candidates. Very large pipelines (20+ candidates) may produce verbose output.

---

## How to Use

1. **Gather your interview notes**
   - Collect notes from your latest round of interviews and evaluation sheets
   - Notes can be rough — no formatting required

2. **Trigger the skill by saying:**
   - "Review hiring pipeline"
   - "Hiring pipeline status"
   - In Russian: "Статус по кандидатам" or "Ревью пайплайна найма"

3. **Paste or upload your notes**
   - Paste the notes directly in chat, or provide a file path
   - Optionally mention the position title and key hiring criteria

4. **Review the report**
   - Scan the Candidate Table for stage, score, and next steps
   - Check the Flags section for stuck or incomplete candidates
   - Use the Recommendations section to drive decisions
   - Optionally request a recruiter update narrative

---

## Examples

### Example 1: Single-position weekly review

**Input:**
```
Alex Chen — Phone Screen 2026-04-09
Strong communication, relevant background. Score 4/5. Schedule interview 1.

Jordan Lee — Interview 1 2026-04-07
Technical gaps in system design. Score 2/5. Likely decline.

Sam Rivera — Interview 2 2026-04-05
No update since last week. Team split 2/2. Need to discuss.

Casey Park — Applied 2026-04-12
Haven't reviewed resume yet.
```

**Output:**
```markdown
## Hiring Pipeline Status — Engineering Manager — 2026-04-16

### Candidate Table

| Candidate    | Stage        | Last Action | Score | Next Step            | Flag         |
|--------------|--------------|-------------|-------|----------------------|--------------|
| Alex Chen    | Phone Screen | 2026-04-09  | 4/5   | Schedule Interview 1 | —            |
| Jordan Lee   | Interview 1  | 2026-04-07  | 2/5   | Decline              | —            |
| Sam Rivera   | Interview 2  | 2026-04-05  | —     | Team sync needed     | ⚠ stuck      |
| Casey Park   | Applied      | 2026-04-12  | —     | Review application   | ❓ incomplete |

### Flags
- ⚠ Sam Rivera — stuck since 2026-04-05, no next step defined
- ❓ Casey Park — no evaluation data yet

### Recommendations
- Advance: Alex Chen — strong score, clear next step
- Decline: Jordan Lee — significant technical gaps
- Decision needed: Sam Rivera — team split; requires sync before proceeding
```

---

### Example 2: Multi-stage pipeline with mixed notes quality

**Input:**
```
Maria T. — offered on 04/10, waiting for response. Strong all-around 5/5.

Ben K. — second interview done 04/08, minor culture concerns, 3.5/5. 
Next: reference check or decline.

Dev S. — ghosted since initial screen 04/01, no reply to follow-up.
```

**Output:**
```markdown
## Hiring Pipeline Status — 2026-04-16

### Candidate Table

| Candidate | Stage          | Last Action | Score | Next Step              | Flag    |
|-----------|----------------|-------------|-------|------------------------|---------|
| Maria T.  | Offer extended | 2026-04-10  | 5/5   | Await response         | —       |
| Ben K.    | Interview 2    | 2026-04-08  | 3.5/5 | Reference check        | —       |
| Dev S.    | Phone Screen   | 2026-04-01  | —     | Close or mark inactive | ⚠ stuck |

### Flags
- ⚠ Dev S. — no response since 2026-04-01 (15 days)

### Recommendations
- Advance: Maria T. — offer pending; monitor for response
- Decision needed: Ben K. — minor concerns; confirm with team before reference check
- Decline: Dev S. — non-responsive; recommend closing
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Review hiring pipeline | Ревью пайплайна найма |
| Hiring pipeline status | Статус по кандидатам |
| Summarize candidates | Сводка по кандидатам |
| Weekly candidate update | Еженедельный отчёт по найму |
| What's the status on my candidates? | Что у нас по кандидатам? |

---

**Version:** 1.0.0  
**Last updated:** 2026-04-16
