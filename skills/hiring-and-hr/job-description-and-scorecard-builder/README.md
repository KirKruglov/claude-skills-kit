> [Версия на русском языке](README.ru.md)

# Job Description and Scorecard Builder

Write a job posting and a matched interview scorecard from your role notes — in one pass, no HR team required.

---

## Overview

Job Description and Scorecard Builder generates a structured job description and a matched interview scorecard from free-form role notes. It's the only tool in the ecosystem that creates both documents together from the hiring manager's perspective — every must-have requirement in the JD automatically becomes a scored criterion in the scorecard. Use this skill when you're opening a new position and need a ready-to-post JD and a ready-to-use evaluation form, when you want to ensure your scorecard is consistent with what you advertised, or when you run interviews without a dedicated recruiter or HR team.

---

## Requirements

- Role notes in free-form text: title, level, must-have requirements (minimum)
- Optional fields: nice-to-have requirements, compensation range, work format, team context, interview format preference
- No external tools, SaaS, or ATS integrations required

**Works best with:** a short paragraph or bullet list describing the role. Works for any level — Junior through C-suite.

---

## How to Use

1. **Gather your role notes**
   - Jot down the role title, level (Junior / Senior / Lead / etc.), must-have skills, and any other details you have (nice-to-haves, compensation range, work format)
   - Notes can be free-form, bullet points, or a mix

2. **Trigger the skill**
   - Say: "Write a job description for [role]" or "Job description and scorecard"
   - In Russian: "Напиши вакансию для [роли]" or "Вакансия и оценочный лист"

3. **Paste or type your role notes**
   - You can provide as little as a title and a few must-haves — the skill will flag what's missing at the top
   - Or provide a full brief for a complete, ready-to-use output

4. **Review your two documents**
   - **Job Description:** copy to your careers page, LinkedIn, or internal job board
   - **Interview Scorecard:** print or paste into your interview notes template; use it to rate every candidate consistently

---

## Examples

### Example 1: Hiring a Senior Product Manager

**Input:**
```
Role: Senior Product Manager
Level: Senior
Must have: 4+ years of PM experience, ability to write PRDs, experience with B2B SaaS, data-driven decision making
Nice to have: experience with enterprise sales cycles, SQL basics
Compensation: $130–160k
Work format: Hybrid (NYC)
Team: Product team of 6, reports to Head of Product
```

**Output (excerpt):**
```markdown
## Job Description — Senior Product Manager (Senior)

### About the Role
We're looking for a Senior Product Manager to drive product strategy and execution for our B2B SaaS platform. You'll work closely with engineering, design, and commercial teams, reporting to the Head of Product.

### Responsibilities
- Define and own the product roadmap for your area
- Write clear PRDs that align engineering and design around user problems
- Analyze usage data to prioritize features and validate decisions
- Partner with sales and customer success to understand enterprise needs
- Run discovery, define acceptance criteria, and ship iteratively

### Requirements

**Must Have:**
- 4+ years of product management experience
- Ability to write structured PRDs understood by engineering
- Experience with B2B SaaS products
- Data-driven approach to prioritization and decision making

**Nice to Have:**
- Familiarity with enterprise sales cycles
- SQL skills for self-serve data analysis

### Compensation & Work Format
- **Compensation:** $130,000–160,000
- **Work format:** Hybrid (New York City)

### About the Team
Product team of 6, reporting to Head of Product.

---

## Interview Scorecard — Senior Product Manager (Senior)

| Criterion | Weight | 1 — Not demonstrated | 2 — Below bar | 3 — Meets bar | 4 — Exceeds |
|-----------|--------|----------------------|---------------|---------------|-------------|
| 4+ years of product management experience | High | <2 years or unrelated | 2–3 years, gaps in ownership | 4+ years clear ownership | 5+ years, increasing scope |
| Ability to write structured PRDs | High | Cannot describe PRD process | Informal docs only | Writes structured PRDs used by engineering | PRDs cited as team standard |
| Experience with B2B SaaS products | High | Consumer only | Some B2B exposure | Full B2B SaaS product ownership | Led B2B product at scale |
| Data-driven decision making | High | No metrics usage | Uses data reactively | Proactively uses data to prioritize | Drove measurable outcomes with data |
| Familiarity with enterprise sales cycles | Medium | No exposure | Knows the concept | Has worked with enterprise sales | Deep alignment with sales cycles |

**Overall Recommendation:**
☐ Strong Hire  ☐ Hire  ☐ No Hire  ☐ Strong No Hire
```

---

### Example 2: Hiring a Junior Marketing Manager

**Input:**
```
Role: Marketing Manager
Level: Junior
Must have: 1+ year in digital marketing, copywriting, experience with social media content
Work format: Remote
```

**Output (excerpt):**
```markdown
## Job Description — Marketing Manager (Junior)

### About the Role
We're looking for a Junior Marketing Manager to support content creation and social media presence. You'll contribute to day-to-day digital marketing campaigns and help grow our online audience.

### Responsibilities
- Create and schedule social media content across key channels
- Write engaging copy for emails, posts, and landing pages
- Track content performance and suggest improvements
- Support campaign execution alongside the marketing team

### Requirements

**Must Have:**
- 1+ year of experience in digital marketing
- Strong copywriting skills for digital formats
- Hands-on experience creating and managing social media content

### Compensation & Work Format
- **Compensation:** not specified
- **Work format:** Remote

---

## Interview Scorecard — Marketing Manager (Junior)

| Criterion | Weight | 1 — Not demonstrated | 2 — Below bar | 3 — Meets bar | 4 — Exceeds |
|-----------|--------|----------------------|---------------|---------------|-------------|
| 1+ year in digital marketing | High | No experience | Internship only | 1+ year full-time | 2+ years with measurable results |
| Copywriting skills for digital formats | High | No samples | Drafts with heavy editing needed | Clean copy for digital formats | Compelling copy, minimal editing |
| Social media content experience | High | No social experience | Personal accounts only | Managed brand accounts | Grew audience or drove engagement metrics |
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Write a job description | Напиши вакансию |
| Job description and scorecard | Вакансия и оценочный лист |
| I need to open a position | Мне нужно открыть позицию |
| Create a JD for this role | Создай описание роли |
| Help me hire for [role] | Помоги нанять [роль] |

---

> See [User Guide](docs/USER-GUIDE.md) for step-by-step scenarios and tips.

**Version:** 1.0.0
