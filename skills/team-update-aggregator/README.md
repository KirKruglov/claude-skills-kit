> [Версия на русском языке](README.ru.md)

# Team Update Aggregator

A Claude skill that compiles weekly updates from your team members into a structured **people-centric** status report — organized by person, not by project. Each team member gets a dedicated section with progress, next-week plans, blockers, capacity notes, and manager attention flags.

## Overview

Most weekly digest tools organize information by project or topic. This skill organizes it by **person** — so you see the full picture for each team member at a glance: what they accomplished, what's blocking them, how loaded they are, and whether anything needs your attention.

Built for managers preparing for 1-on-1s, weekly team reviews, or people tracking.

## Requirements

Local `.md` or `.txt` files with team member updates. One file per person, or one file containing multiple sections (one per person).

## How to Use

1. Tell Claude the folder path or list of files containing your team's updates
2. The skill identifies each person from the filename or file header
3. It extracts progress, plans, blockers, capacity, and any manager flags
4. Output: `team-status-YYYY-MM-DD.md` saved to your working directory

## Examples

**Example 1 — Folder of individual files**
> "Aggregate team updates from /updates/week-17/"

Each file (e.g., `anna.md`, `ivan.md`) becomes one section in the report.

**Example 2 — Single file with multiple sections**
> "Build the team status report from team-updates.md"

The skill splits by H2/H3 name headers and creates one entry per person.

**Example 3 — Pre-1-on-1 prep**
> "Compile team status — I have 1-on-1s tomorrow"

Result: report with flags highlighting who needs attention.

## Triggers

| English | Russian |
|---------|---------|
| `aggregate team updates` | `агрегируй обновления команды` |
| `compile team status` | `статус команды` |
| `team weekly report` | `составь отчёт по команде` |
| `build team status report` | `обновления от команды` |
| `who's working on what` | `что делает команда` |
| `team update summary` | `people-отчёт` |

## Output Structure

```
team-status-YYYY-MM-DD.md
├── Summary (team health, key achievements, flags)
├── Team Members (one section per person)
│   ├── Progress
│   ├── Next week plans
│   ├── Blockers
│   ├── Capacity
│   └── Manager flags ⚠️
└── Cross-Team (shared blockers, dependencies, unowned actions)
```

## Key Difference from weekly-digest-synthesizer

| weekly-digest-synthesizer | team-update-aggregator |
|--------------------------|----------------------|
| Organized by **project / topic** | Organized by **person** |
| "What's happening on Project Alpha?" | "How is Anna doing this week?" |
| Good for project status meetings | Good for 1-on-1s and people management |

## Related Skills

- **weekly-digest-synthesizer** — project-centric weekly digest from multiple files
- **one-to-one-prep** — structured prep document for individual 1-on-1 meetings
- **hiring-pipeline-reviewer** — weekly candidate status from interview notes
