> [Версия на русском языке](README.ru.md)

# claude-skills-kit

![GitHub stars](https://img.shields.io/github/stars/KirKruglov/claude-skills-kit?style=flat-square)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
![Skills](https://img.shields.io/badge/skills-77-informational?style=flat-square)
![Last commit](https://img.shields.io/github/last-commit/KirKruglov/claude-skills-kit?style=flat-square)

77 curated agent skills for Claude — designed for non-technical users across PM, operations, finance, HR, and industry-specific teams.

> 70 standalone skills + 7 nested skills in `project-management-kit`

---

## Quick Start

**Step 1.** Find a skill in the catalog below.

**Step 2.** Copy the skill folder to your workspace:

- **Cowork** — copy the skill folder into your Cowork workspace directory. Claude detects it automatically.
- **Claude.ai / Projects** — open the skill's `SKILL.md`, copy its content, and paste it into Project Instructions.

**Step 3.** Use Claude as usual. The skill activates based on your message — no commands needed.

> See [INSTALL.md](INSTALL.md) / [INSTALL.ru.md](INSTALL.ru.md) for step-by-step setup.

---

## Why Claude Skills Kit?

Most skill repositories contain only a `SKILL.md` file.
Claude Skills Kit ships a **complete package** per skill:

| What's included                | Why it matters                                           |
| ------------------------------ | -------------------------------------------------------- |
| `SKILL.md` — core instructions | Claude activates the skill                               |
| `README.md` (EN + RU)          | You know what the skill does before installing           |
| `docs/USER-GUIDE.md`           | How to use the skill with examples (where applicable)    |
| `INSTALL.md` (EN + RU)         | Common setup guide in the repo root                      |

**Designed for non-technical users.** No code, no CLI, no configuration.
**Bilingual EN/RU.** Claude detects the language of your request automatically.

---

## What is a skill?

A skill is a folder containing a `SKILL.md` file with structured instructions for Claude. Add it to Claude.ai or Cowork — and Claude gains a new, reproducible capability without writing code.

Skills are:
- **Interface-agnostic** — work in Claude.ai, Projects, API, and Cowork
- **Self-contained** — each skill folder includes everything needed
- **Composable** — multiple skills can be combined in a single setup

---

## Find by role

A skill can appear under several roles. Full descriptions are in the [catalog below](#skills).

**📆 PM / Product** — [project-management-kit](skills/project-management/project-management-kit/) · [project-onboarding](skills/project-management/project-onboarding/) · [context-builder-cowork](skills/project-management/context-builder-cowork/) · [sprint-review-summarizer](skills/project-management/sprint-review-summarizer/) · [backlog-grooming-assistant](skills/project-management/backlog-grooming-assistant/) · [retro-pattern-analyzer](skills/project-management/retro-pattern-analyzer/) · [decision-log](skills/project-management/decision-log/) · [weekly-digest-synthesizer](skills/status-reports-and-stakeholder-updates/weekly-digest-synthesizer/) · [okr-progress-narrator](skills/status-reports-and-stakeholder-updates/okr-progress-narrator/) · [stakeholder-adapter](skills/status-reports-and-stakeholder-updates/stakeholder-adapter/) · [meeting-prep-briefer](skills/team-leadership/meeting-prep-briefer/) · [user-feedback-synthesizer](skills/discovery-and-user-research/user-feedback-synthesizer/) · [user-persona-synthesizer](skills/discovery-and-user-research/user-persona-synthesizer/) · [jobs-to-be-done-extractor](skills/discovery-and-user-research/jobs-to-be-done-extractor/) · [prd-review-challenger](skills/launch-and-releases/prd-review-challenger/) · [release-notes-generator](skills/launch-and-releases/release-notes-generator/) · [feature-announcement-writer](skills/launch-and-releases/feature-announcement-writer/) · [changelog-narrator](skills/launch-and-releases/changelog-narrator/) · [survey-results-analyzer](skills/launch-and-releases/survey-results-analyzer/) · [retention-cohort-interpreter](skills/data-analysis/retention-cohort-interpreter/) · [experiment-results-interpreter](skills/data-analysis/experiment-results-interpreter/) · [north-star-metric-auditor](skills/metrics-and-exec-narratives/north-star-metric-auditor/) · [competitive-feature-matrix-builder](skills/market-and-competitive-intelligence/competitive-feature-matrix-builder/) · [weekly-competitor-tracker](skills/market-and-competitive-intelligence/weekly-competitor-tracker/) · [industry-trend-brief](skills/market-and-competitive-intelligence/industry-trend-brief/) · [research-folder-synthesizer](skills/personal-productivity/research-folder-synthesizer/) · [reading-list-prioritizer](skills/personal-productivity/reading-list-prioritizer/)

**🚀 Founder / CEO** — [exec-metrics-storyteller](skills/metrics-and-exec-narratives/exec-metrics-storyteller/) · [weekly-metrics-story-writer](skills/metrics-and-exec-narratives/weekly-metrics-story-writer/) · [north-star-metric-auditor](skills/metrics-and-exec-narratives/north-star-metric-auditor/) · [fundraise-pipeline-tracker](skills/business-ops/fundraise-pipeline-tracker/) · [data-room-prep-checklist](skills/business-ops/data-room-prep-checklist/) · [proposal-and-quote-drafter](skills/business-ops/proposal-and-quote-drafter/) · [win-loss-debrief-writer](skills/business-ops/win-loss-debrief-writer/) · [company-policy-drafter](skills/business-ops/company-policy-drafter/) · [job-description-and-scorecard-builder](skills/hiring-and-hr/job-description-and-scorecard-builder/) · [onboarding-plan-30-60-90](skills/hiring-and-hr/onboarding-plan-30-60-90/) · [invoice-and-payment-tracker-summary](skills/finance-and-billing/invoice-and-payment-tracker-summary/) · [accounts-receivable-followup-writer](skills/finance-and-billing/accounts-receivable-followup-writer/) · [monthly-close-checklist-and-reconciliation-prep](skills/finance-and-billing/monthly-close-checklist-and-reconciliation-prep/) · [competitive-feature-matrix-builder](skills/market-and-competitive-intelligence/competitive-feature-matrix-builder/) · [industry-trend-brief](skills/market-and-competitive-intelligence/industry-trend-brief/) · [daily-admin-brief](skills/personal-productivity/daily-admin-brief/)

**👥 Team Lead / Manager** — [one-to-one-prep](skills/team-leadership/one-to-one-prep/) · [delegation-brief](skills/team-leadership/delegation-brief/) · [meeting-prep-briefer](skills/team-leadership/meeting-prep-briefer/) · [team-update-aggregator](skills/status-reports-and-stakeholder-updates/team-update-aggregator/) · [morning-standup-brief-generator](skills/status-reports-and-stakeholder-updates/morning-standup-brief-generator/) · [weekly-status-report-generator](skills/status-reports-and-stakeholder-updates/weekly-status-report-generator/) · [weekly-digest-synthesizer](skills/status-reports-and-stakeholder-updates/weekly-digest-synthesizer/) · [okr-progress-narrator](skills/status-reports-and-stakeholder-updates/okr-progress-narrator/) · [decision-log](skills/project-management/decision-log/) · [hiring-pipeline-reviewer](skills/hiring-and-hr/hiring-pipeline-reviewer/) · [onboarding-plan-30-60-90](skills/hiring-and-hr/onboarding-plan-30-60-90/) · [interview-debrief-synthesizer](skills/hiring-and-hr/interview-debrief-synthesizer/) · [workspace-health-monitor](skills/personal-productivity/workspace-health-monitor/) · [daily-admin-brief](skills/personal-productivity/daily-admin-brief/)

**🧑‍💼 HR / Recruiter** — [hiring-pipeline-reviewer](skills/hiring-and-hr/hiring-pipeline-reviewer/) · [job-description-and-scorecard-builder](skills/hiring-and-hr/job-description-and-scorecard-builder/) · [onboarding-plan-30-60-90](skills/hiring-and-hr/onboarding-plan-30-60-90/) · [interview-debrief-synthesizer](skills/hiring-and-hr/interview-debrief-synthesizer/) · [company-policy-drafter](skills/business-ops/company-policy-drafter/)

**💰 Finance / Ops** — [invoice-and-payment-tracker-summary](skills/finance-and-billing/invoice-and-payment-tracker-summary/) · [accounts-receivable-followup-writer](skills/finance-and-billing/accounts-receivable-followup-writer/) · [monthly-close-checklist-and-reconciliation-prep](skills/finance-and-billing/monthly-close-checklist-and-reconciliation-prep/) · [legal-matter-tracker](skills/business-ops/legal-matter-tracker/)

**📣 Marketer** — [campaign-retrospective-writer](skills/marketing-and-content/campaign-retrospective-writer/) · [content-performance-reporter](skills/marketing-and-content/content-performance-reporter/) · [research-to-content-brief](skills/marketing-and-content/research-to-content-brief/) · [feature-announcement-writer](skills/launch-and-releases/feature-announcement-writer/) · [release-notes-generator](skills/launch-and-releases/release-notes-generator/) · [newsletter-digest-builder](skills/personal-productivity/newsletter-digest-builder/) · [reading-list-prioritizer](skills/personal-productivity/reading-list-prioritizer/) · [industry-trend-brief](skills/market-and-competitive-intelligence/industry-trend-brief/) · [weekly-competitor-tracker](skills/market-and-competitive-intelligence/weekly-competitor-tracker/) · [competitive-feature-matrix-builder](skills/market-and-competitive-intelligence/competitive-feature-matrix-builder/)

**📊 Analyst** — [csv-data-analyzer](skills/data-analysis/csv-data-analyzer/) · [report-analyzer](skills/data-analysis/report-analyzer/) · [retention-cohort-interpreter](skills/data-analysis/retention-cohort-interpreter/) · [experiment-results-interpreter](skills/data-analysis/experiment-results-interpreter/) · [metrics-anomaly-investigator](skills/data-analysis/metrics-anomaly-investigator/) · [kpi-digest-builder](skills/metrics-and-exec-narratives/kpi-digest-builder/) · [exec-metrics-storyteller](skills/metrics-and-exec-narratives/exec-metrics-storyteller/) · [weekly-metrics-story-writer](skills/metrics-and-exec-narratives/weekly-metrics-story-writer/) · [north-star-metric-auditor](skills/metrics-and-exec-narratives/north-star-metric-auditor/) · [survey-results-analyzer](skills/launch-and-releases/survey-results-analyzer/) · [content-performance-reporter](skills/marketing-and-content/content-performance-reporter/) · [research-folder-synthesizer](skills/personal-productivity/research-folder-synthesizer/)

**🤖 Claude power user** — [prompt-builder](skills/prompts-and-memory/prompt-builder/) · [prompt-library-curator](skills/prompts-and-memory/prompt-library-curator/) · [memory-auditor-chat](skills/prompts-and-memory/memory-auditor-chat/) · [memory-auditor-cowork](skills/prompts-and-memory/memory-auditor-cowork/) · [session-handoff-composer](skills/sessions-and-context/session-handoff-composer/) · [context-window-health-check](skills/sessions-and-context/context-window-health-check/) · [cowork-session-planner](skills/sessions-and-context/cowork-session-planner/) · [feature-guide](skills/setup-and-audit/feature-guide/) · [cowork-plugin-audit](skills/setup-and-audit/cowork-plugin-audit/) · [skill-usage-log-reviewer](skills/setup-and-audit/skill-usage-log-reviewer/) · [routines-setup-assistant](skills/setup-and-audit/routines-setup-assistant/) · [weekly-ai-workflow-review](skills/setup-and-audit/weekly-ai-workflow-review/) · [setup-wizard](skills/setup-and-audit/setup-wizard/)

---

## Skills

The **Input** column says what you must provide to run the skill.

| Domain | Groups |
| ------ | ------ |
| [I. Delivery](#i-delivery) | [Project Management](#project-management) · [Status Reports & Stakeholder Updates](#status-reports--stakeholder-updates) |
| [II. People](#ii-people) | [Team Leadership](#team-leadership) · [Hiring & HR](#hiring--hr) |
| [III. Product](#iii-product) | [Discovery & User Research](#discovery--user-research) · [Launch & Releases](#launch--releases) |
| [IV. Data](#iv-data) | [Data Analysis](#data-analysis) · [Metrics & Exec Narratives](#metrics--exec-narratives) |
| [V. Business](#v-business) | [Market & Competitive Intelligence](#market--competitive-intelligence) · [Marketing & Content](#marketing--content) · [Business Ops](#business-ops) · [Finance & Billing](#finance--billing) |
| [VI. Personal & Claude](#vi-personal--claude) | [Personal Productivity](#personal-productivity) · [Prompts & Memory](#prompts--memory) · [Sessions & Context](#sessions--context) · [Setup & Audit](#setup--audit) |

---

### I. Delivery

#### Project Management

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| project-management-kit | Project brief → 7 nested skills | [→](skills/project-management/project-management-kit/) | AI Project Manager agent — 7 skills for project documentation (charter, risk register, project plan, communication plan, meeting protocol, plan-vs-actual report, closure report). PMBoK 8 + Agile. Bilingual EN/RU |
| project-onboarding | Interview answers and project folder | [→](skills/project-management/project-onboarding/) | Full project onboarding for Cowork: generates context.md, folder rules, file map, and starter prompts in one session. Bilingual EN/RU |
| context-builder-cowork | Interview answers | [→](skills/project-management/context-builder-cowork/) | Generates a structured `project-context.md` file via interactive interview |
| sprint-review-summarizer | Pasted sprint notes or .md | [→](skills/project-management/sprint-review-summarizer/) | Transforms plain-language sprint notes into a structured stakeholder doc — delivered, deferred, risks, and next sprint focus. No Jira required. Bilingual EN/RU |
| backlog-grooming-assistant | Backlog CSV or Markdown table | [→](skills/project-management/backlog-grooming-assistant/) | Reads a local backlog export (CSV or Markdown), flags problematic items (no owner, no estimate, stale, blocked), and generates a structured grooming session agenda with a scorecard. No Jira API required. Bilingual EN/RU |
| retro-pattern-analyzer | Two or more retro .md/.txt | [→](skills/project-management/retro-pattern-analyzer/) | Analyzes sprint retrospective files to surface recurring pain points, unresolved action items, and positive patterns across sprints. Bilingual EN/RU |
| decision-log | Pasted meeting or thread text | [→](skills/project-management/decision-log/) | Extracts structured decisions from meeting notes, Slack threads, or email chains — builds a clean log separate from action items. Two modes: new log and append with deduplication. Bilingual EN/RU |

##### Project Management Kit — 7 nested skills

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| generate-charter | Project brief or free-form notes | [→](skills/project-management/project-management-kit/generate-charter/) | Generates a project charter — the foundational document of the Initiation phase. Bilingual EN/RU |
| generate-risk-register | Approved project-charter.md file | [→](skills/project-management/project-management-kit/generate-risk-register/) | Generates or updates a risk register with probability/impact scoring and response strategies. Bilingual EN/RU |
| generate-project-plan | Approved project-charter.md file | [→](skills/project-management/project-management-kit/generate-project-plan/) | Generates a project plan with WBS, milestones, dependencies, and resource map. Bilingual EN/RU |
| generate-comm-plan | project-charter.md and project-plan.md | [→](skills/project-management/project-management-kit/generate-comm-plan/) | Generates a communication plan with stakeholder matrix, communication schedule, and escalation rules. Bilingual EN/RU |
| generate-meeting-protocol | Free-form meeting notes | [→](skills/project-management/project-management-kit/generate-meeting-protocol/) | Generates a structured meeting protocol from free-form notes. Bilingual EN/RU |
| generate-plan-fact-report | project-plan.md plus actual data | [→](skills/project-management/project-management-kit/generate-plan-fact-report/) | Generates a plan-vs-actual variance report comparing planned and actual project data. Bilingual EN/RU |
| generate-closure-report | Charter, plan-fact report, lessons | [→](skills/project-management/project-management-kit/generate-closure-report/) | Generates a project closure report — the final artifact of the project lifecycle. Bilingual EN/RU |

#### Status Reports & Stakeholder Updates

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| weekly-digest-synthesizer | Folder of .md/.txt status files | [→](skills/status-reports-and-stakeholder-updates/weekly-digest-synthesizer/) | Compiles status updates from multiple .md/.txt files into a structured weekly digest — by project, with action items and blockers. Bilingual EN/RU |
| weekly-status-report-generator | Pasted raw weekly notes | [→](skills/status-reports-and-stakeholder-updates/weekly-status-report-generator/) | Transforms raw weekly notes into two ready-to-send status reports in one pass: a detailed Manager Report and a 3-point Skip-Level Brief. Bilingual EN/RU |
| team-update-aggregator | Folder of .md/.txt member updates | [→](skills/status-reports-and-stakeholder-updates/team-update-aggregator/) | Aggregates weekly updates from team members into a people-centric status report — organized by person, not by project. Progress, plans, blockers, capacity, and manager attention flags per team member. Bilingual EN/RU |
| morning-standup-brief-generator | Working folder with .md/.txt notes | [→](skills/status-reports-and-stakeholder-updates/morning-standup-brief-generator/) | Compiles local notes, tasks, and project files into a structured daily standup brief — Yesterday / Today / Blockers / Questions. No connectors required. Bilingual EN/RU |
| okr-progress-narrator | OKR file (.md/.txt/.csv) or text | [→](skills/status-reports-and-stakeholder-updates/okr-progress-narrator/) | Transforms raw OKR data (tables, lists, CSV, or pasted text) into a narrative stakeholder update: executive summary, per-objective narrative, KR status table, risks, and next steps. Bilingual EN/RU |
| stakeholder-adapter | Source document (.md/.txt or pasted) | [→](skills/status-reports-and-stakeholder-updates/stakeholder-adapter/) | Adapts any document into audience-specific versions: Leadership (business impact, decision-focused), Engineering/Team (technical depth, actionable), Client (outcome language, no jargon). Bilingual EN/RU |

---

### II. People

#### Team Leadership

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| one-to-one-prep | Previous 1-on-1 notes and tasks | [→](skills/team-leadership/one-to-one-prep/) | Generates a structured prep document for monthly 1-on-1 meetings: action item tracking, prioritized discussion topics, and wellbeing questions. Bilingual EN/RU |
| delegation-brief | Interview answers | [→](skills/team-leadership/delegation-brief/) | Generates a structured task brief via 5-question interview — ready to paste into a new Cowork session. Bilingual EN/RU |
| meeting-prep-briefer | Daily schedule plus workspace files | [→](skills/team-leadership/meeting-prep-briefer/) | Generates a structured per-meeting brief for every call in your day — participants, context from local files, open questions, and suggested agenda. Paste your schedule or point to a file. No integrations required. Bilingual EN/RU |

#### Hiring & HR

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| hiring-pipeline-reviewer | Pasted interview notes/evaluations | [→](skills/hiring-and-hr/hiring-pipeline-reviewer/) | Generates a structured weekly status report for all candidates in your hiring pipeline from interview notes and evaluation sheets. Flags stuck candidates, consolidates scores, and recommends next steps. Bilingual EN/RU |
| job-description-and-scorecard-builder | Pasted role notes | [→](skills/hiring-and-hr/job-description-and-scorecard-builder/) | Generates a job description and a matched interview scorecard from role notes — paired hiring documents for managers who run interviews without an HR team. No recruiting SaaS required. Bilingual EN/RU |
| onboarding-plan-30-60-90 | Role title and priorities | [→](skills/hiring-and-hr/onboarding-plan-30-60-90/) | Generates a targeted 30-60-90 day onboarding plan for a new hire from the manager's perspective — goals, key contacts, learning milestones, and success metrics per phase. No HR tools required. Bilingual EN/RU |
| interview-debrief-synthesizer | Pasted notes from several interviewers | [→](skills/hiring-and-hr/interview-debrief-synthesizer/) | Consolidates mismatched notes from several interviewers into one comparable debrief — evidence separated from impressions with attribution, where interviewers disagree, and competencies nobody probed. No ATS required. Bilingual EN/RU |

---

### III. Product

#### Discovery & User Research

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| user-feedback-synthesizer | Folder of .md/.txt/.csv feedback | [→](skills/discovery-and-user-research/user-feedback-synthesizer/) | Synthesizes user interview transcripts and feedback files (.md, .txt, .csv) into a prioritized insight report with themes, quotes, and open questions. Bilingual EN/RU |
| user-persona-synthesizer | Pasted or .md interview transcripts | [→](skills/discovery-and-user-research/user-persona-synthesizer/) | Extracts recurring user profiles from real CustDev transcripts and generates structured persona cards with verbatim quotes and respondent counts. No integrations required. Bilingual EN/RU |
| jobs-to-be-done-extractor | Folder of .md/.txt custdev notes | [→](skills/discovery-and-user-research/jobs-to-be-done-extractor/) | Extracts Jobs-to-be-Done statements from a folder of custdev transcripts and interview notes — ranked JTBD map with evidence quotes, frequency counts, and patterns. Bilingual EN/RU |

#### Launch & Releases

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| prd-review-challenger | PRD text or file | [→](skills/launch-and-releases/prd-review-challenger/) | Devil's advocate for PRDs, feature specs, and product decisions — surfaces weak assumptions, open questions, implementation risks, and logical gaps before the document goes to the team. Bilingual EN/RU |
| release-notes-generator | Sprint summary .md/.txt file | [→](skills/launch-and-releases/release-notes-generator/) | Turns a plain-language sprint summary into 4 user-facing release notes formats: changelog entry, email announcement, in-app push notification, and social post. No git required. Bilingual EN/RU |
| feature-announcement-writer | One feature description, text/.md | [→](skills/launch-and-releases/feature-announcement-writer/) | Generates a multi-format feature announcement pack (changelog, email, push notification, social post) from a single product description — no copywriting needed. Bilingual EN/RU |
| changelog-narrator | Two .md/.txt document versions | [→](skills/launch-and-releases/changelog-narrator/) | Compares two versions of a business document and generates a human-readable changelog — no git, no Track Changes. Works on PRDs, SOPs, contracts, and strategy docs. Bilingual EN/RU |
| survey-results-analyzer | Survey CSV export | [→](skills/launch-and-releases/survey-results-analyzer/) | Analyzes survey CSV exports — quantitative frequencies, open-ended themes, and Top-3 insights without code or Python. Bilingual EN/RU |

---

### IV. Data

#### Data Analysis

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| csv-data-analyzer | CSV file in workspace | [→](skills/data-analysis/csv-data-analyzer/) | Analyzes CSV files with business data through a dialogue-based question flow — no code, no Python, no integrations required. Bilingual EN/RU |
| report-analyzer | PDF or PPTX report file | [→](skills/data-analysis/report-analyzer/) | Analyzes large PDF/PPTX reports and produces a structured summary with key data and insights |
| retention-cohort-interpreter | Pasted cohort retention table | [→](skills/data-analysis/retention-cohort-interpreter/) | Interprets cohort retention tables into plain-language diagnosis: curve health, drop-off windows, benchmark comparison, hypotheses, and next steps. No analytics tools required. Bilingual EN/RU |
| experiment-results-interpreter | Pasted A/B test results | [→](skills/data-analysis/experiment-results-interpreter/) | Turns A/B test results into a go/no-go decision — plain-language significance assessment, ship/rollback/extend recommendation with rationale, and a copy-paste stakeholder summary. No stats background required. Bilingual EN/RU |
| metrics-anomaly-investigator | Description of the anomaly | [→](skills/data-analysis/metrics-anomaly-investigator/) | Turns a metric anomaly description into a ranked hypothesis framework and stakeholder narrative — no database or code required. Bilingual EN/RU |

#### Metrics & Exec Narratives

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| kpi-digest-builder | Local .md/.txt/.csv KPI files | [→](skills/metrics-and-exec-narratives/kpi-digest-builder/) | Aggregates numeric KPIs from local files (.md, .txt, .csv) into a weekly snapshot with delta vs. previous week — no code, no integrations required. Bilingual EN/RU |
| exec-metrics-storyteller | Metrics snapshot plus business context | [→](skills/metrics-and-exec-narratives/exec-metrics-storyteller/) | Turns a metrics snapshot into a board-ready executive narrative with revenue and LTV framing. Bilingual EN/RU |
| weekly-metrics-story-writer | Pasted weekly metrics plus context | [→](skills/metrics-and-exec-narratives/weekly-metrics-story-writer/) | Turns dashboard numbers into a polished weekly narrative for stakeholders — email or Slack, copy-paste ready in minutes. Bilingual EN/RU |
| north-star-metric-auditor | Current NSM plus business model | [→](skills/metrics-and-exec-narratives/north-star-metric-auditor/) | Audits a North Star Metric against 4 standard criteria and proposes 2–3 business-model-fit alternatives for PMs and founders. Bilingual EN/RU |

---

### V. Business

#### Market & Competitive Intelligence

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| competitive-feature-matrix-builder | Folder of competitor notes (md/txt) | [→](skills/market-and-competitive-intelligence/competitive-feature-matrix-builder/) | Builds a comparative feature matrix and gap analysis from a folder of competitor notes (md/txt) — fully offline, no web access required. Bilingual EN/RU |
| weekly-competitor-tracker | competitors/ folder of .md files | [→](skills/market-and-competitive-intelligence/weekly-competitor-tracker/) | Tracks weekly competitor changes from your markdown notes — compares current vs. last-week snapshot and generates a delta-report with significance flags. No APIs required. Bilingual EN/RU |
| industry-trend-brief | Folder of articles (md/txt) | [→](skills/market-and-competitive-intelligence/industry-trend-brief/) | Synthesizes a folder of articles and clippings into a weekly trend signals brief for product teams — ranked themes, source-linked signals, and takeaways. Fully offline. Bilingual EN/RU |

#### Marketing & Content

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| campaign-retrospective-writer | Pasted campaign metrics and notes | [→](skills/marketing-and-content/campaign-retrospective-writer/) | Builds a structured marketing retrospective from pasted campaign data: goal vs. result, channel breakdown, what worked/didn't, recommendations, and trend line. Bilingual EN/RU |
| content-performance-reporter | Analytics CSV exports | [→](skills/marketing-and-content/content-performance-reporter/) | Compiles weekly analytics CSV exports from content platforms (YouTube, GA4, LinkedIn) into a narrative report: what worked, what didn't, the week's pattern, and recommendations. Bilingual EN/RU |
| research-to-content-brief | Folder of research notes (md/txt) | [→](skills/marketing-and-content/research-to-content-brief/) | Turns research notes (audience, competitor signals, trends) into a structured content brief with six sections. No interview needed. Bilingual EN/RU |

#### Business Ops

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| proposal-and-quote-drafter | Pasted discovery call notes | [→](skills/business-ops/proposal-and-quote-drafter/) | Turns discovery call notes into a client proposal: scope, pricing packages, cover letter, and review checklist. Bilingual EN/RU |
| win-loss-debrief-writer | Pasted closed deal notes | [→](skills/business-ops/win-loss-debrief-writer/) | Generates a structured win/loss debrief from closed deal notes — decision drivers, objections, competitive context, repeat/fix recommendations, and a trend row for your deal log. No CRM required. Bilingual EN/RU |
| fundraise-pipeline-tracker | Pasted investor notes | [→](skills/business-ops/fundraise-pipeline-tracker/) | Assembles a structured investor pipeline from pasted meeting notes: Tier 1/2/3 tiering, per-investor status and follow-up priorities — no CRM required. Bilingual EN/RU |
| data-room-prep-checklist | Round stage and business model | [→](skills/business-ops/data-room-prep-checklist/) | Generates a stage-specific due-diligence checklist, folder structure, and investor gap list for founders entering seed or Series A due diligence — from pasted round context, no integrations required. Bilingual EN/RU |
| legal-matter-tracker | Client or case name | [→](skills/business-ops/legal-matter-tracker/) | Scans workspace files by client or case name and assembles a chronological timeline of events with key facts — no integrations required. Bilingual EN/RU |
| company-policy-drafter | Policy type and parameters | [→](skills/business-ops/company-policy-drafter/) | Drafts or updates a single company policy (PTO, remote work, expenses, AI-usage) in handbook-ready format for SMB teams without in-house HR or legal staff. Legal review flag included. Bilingual EN/RU |

#### Finance & Billing

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| invoice-and-payment-tracker-summary | Pasted invoice list | [→](skills/finance-and-billing/invoice-and-payment-tracker-summary/) | Turns a pasted invoice list into an aging summary, per-client reconciliation, and needs-action list — no accounting SaaS required. Bilingual EN/RU |
| accounts-receivable-followup-writer | Invoice details and relationship context | [→](skills/finance-and-billing/accounts-receivable-followup-writer/) | Drafts an escalating 4-message invoice reminder sequence from overdue invoice details and client relationship context — gentle to final notice, relationship-preserving throughout. No accounting SaaS required. Bilingual EN/RU |
| monthly-close-checklist-and-reconciliation-prep | Pasted transaction list (CSV/table) | [→](skills/finance-and-billing/monthly-close-checklist-and-reconciliation-prep/) | Turns a pasted bank export or transaction list into a monthly-close checklist, categorization draft with disputed-transaction flags, and an accountant/investor summary — no SaaS required. Bilingual EN/RU |

---

### VI. Personal & Claude

#### Personal Productivity

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| reading-list-prioritizer | .md file with reading list | [→](skills/personal-productivity/reading-list-prioritizer/) | Prioritizes and groups a local markdown reading list by topic and relevance to your role — outputs a focused weekly reading plan with a shortlist. Bilingual EN/RU |
| newsletter-digest-builder | Folder of .txt/.md articles | [→](skills/personal-productivity/newsletter-digest-builder/) | Transforms a folder of saved newsletters and articles into a role-prioritized weekly digest — topic-grouped with a 'Read This Week' shortlist. No integrations. Bilingual EN/RU |
| research-folder-synthesizer | Folder of .md/.txt files | [→](skills/personal-productivity/research-folder-synthesizer/) | Synthesizes a folder of mixed local files into a structured thematic report with themes, key findings, and gaps. Bilingual EN/RU |
| workspace-health-monitor | Workspace files or pasted text | [→](skills/personal-productivity/workspace-health-monitor/) | Audits a manager's workspace files to find orphaned files, forgotten action items, duplicates, and plan-to-reality drift. Bilingual EN/RU |
| daily-admin-brief | Pasted calendar, inbox, todos | [→](skills/personal-productivity/daily-admin-brief/) | Turns a pasted calendar dump, inbox shortlist, and open todos into a one-page daily brief — top actions, schedule conflicts, draft reply stubs, dates to capture. No connectors. Bilingual EN/RU |

#### Prompts & Memory

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| prompt-builder | Interview answers | [→](skills/prompts-and-memory/prompt-builder/) | Builds a structured prompt for any task via interactive Q&A |
| prompt-library-curator | Pasted prompts or .md/.txt | [→](skills/prompts-and-memory/prompt-library-curator/) | Organises and tags your personal prompt collection into a structured, navigable markdown catalog with index table and duplicate detection. Bilingual EN/RU |
| memory-auditor-chat | Current session memory layers | [→](skills/prompts-and-memory/memory-auditor-chat/) | Audits and cleans Claude.ai native memory: finds contradictions, outdated entries, duplicates, and noise in Memory Edits and Memory Summary. Bilingual EN/RU |
| memory-auditor-cowork | Cowork workspace memory files | [→](skills/prompts-and-memory/memory-auditor-cowork/) | Audits and cleans file-based memory in Cowork: auto-memory, CLAUDE.md, User Preferences, and Project Instructions. Bilingual EN/RU |

#### Sessions & Context

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| session-handoff-composer | Current session | [→](skills/sessions-and-context/session-handoff-composer/) | Composes a structured handoff block from the current session when context fills up — decisions, tasks, open questions, and next steps ready to paste into a new session. Bilingual EN/RU |
| context-window-health-check | Current session | [→](skills/sessions-and-context/context-window-health-check/) | Assesses current Claude session health and gives a plain-language status (🟢/🟡/🔴) with one concrete recommendation: keep working, create a handoff, or start fresh. No technical metrics. Bilingual EN/RU |
| cowork-session-planner | Current workspace folder | [→](skills/sessions-and-context/cowork-session-planner/) | Generates a pre-session brief for Cowork by scanning project files — current status, session goal, and prioritised work plan before your first message. Bilingual EN/RU |

#### Setup & Audit

| Skill | Input | Link | Description |
| ----- | ----- | ---- | ----------- |
| feature-guide | Feature name or goal description | [→](skills/setup-and-audit/feature-guide/) | Instantly explains any Claude feature or capability: what it is, where it's available, required plan, how to activate, limitations, and an applicability verdict. Bilingual EN/RU |
| cowork-plugin-audit | Plugin list plus workflow description | [→](skills/setup-and-audit/cowork-plugin-audit/) | Audits installed Cowork plugins against your workflow and produces a keep/disable/disable-until-needed table with token-savings estimate. No integrations required. Bilingual EN/RU |
| skill-usage-log-reviewer | Pasted list of installed skills | [→](skills/setup-and-audit/skill-usage-log-reviewer/) | Audits your installed Claude skill collection — flags unused skills, spots duplicates, and generates a deactivation checklist to reduce context noise. Bilingual EN/RU |
| routines-setup-assistant | Interview answers | [→](skills/setup-and-audit/routines-setup-assistant/) | Sets up Claude Cowork Scheduled Tasks via interview — generates ready-to-paste automation prompts for recurring tasks. No integrations required. Bilingual EN/RU |
| weekly-ai-workflow-review | .md file or pasted task log | [→](skills/setup-and-audit/weekly-ai-workflow-review/) | Analyzes weekly notes about Claude-delegated tasks to surface delegation patterns, effective prompts, and optimization areas — with reusable prompt templates. Bilingual EN/RU |
| setup-wizard | Service link plus your setup goal | [→](skills/setup-and-audit/setup-wizard/) | Walks you through setting up an external service or IT tool one step at a time — builds the route from official documentation and closes each step only on evidence you send. Never runs commands for you. Bilingual EN/RU |

---

## How to install a skill

### Option 1 — Git clone (full kit)

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

The skill folder will be at `skills/<group>/<skill-name>/`.

See [INSTALL.md](INSTALL.md) for sparse-checkout, single-skill download, and more options.

---

## How to add a skill to Claude.ai

> Requires a Pro, Max, Team, or Enterprise plan with Code Execution enabled.

1. Go to **Settings → Capabilities** and make sure **Code Execution and File Creation** is enabled
2. Take the skill folder (e.g., `context-builder-cowork/`) and compress it into a ZIP file
   - The ZIP must contain the folder itself as the root, not the files directly
3. Go to **Customize → Skills**
4. Click **"+"** → **"Upload a skill"**
5. Select the ZIP file
6. The skill will appear in the list — enable the toggle

Claude will automatically activate the skill when a request matches its purpose.

---

## How to add a skill to Claude Cowork

1. Open Claude Cowork (desktop app)
2. Go to **Settings → Skills**
3. Click **"+"** → **"Upload a skill"**
4. Select a ZIP file prepared as described above
5. Enable the toggle

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to suggest a skill, report a bug, or improve documentation.

---

## Community

| File | Purpose |
| ---- | ------- |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to suggest skills, report bugs, improve docs |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | Community standards |
| [SECURITY.md](SECURITY.md) | How to report security issues |
| [GitHub Discussions](https://github.com/KirKruglov/claude-skills-kit/discussions) | Questions, ideas, general discussion |

Issue templates and PR template are active automatically via `.github/`.

---

## License

MIT
