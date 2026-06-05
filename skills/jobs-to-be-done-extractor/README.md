# Jobs-to-be-Done Extractor

Extract structured JTBD statements from a folder of custdev transcripts and interview notes. The skill reads multiple md/txt files, synthesizes cross-file patterns, and produces an evidence-backed JTBD map ranked by frequency — ready for roadmap sessions and prioritization work.

## Who benefits

Product managers and UX researchers who have accumulated 3–15 interview files and need to turn raw notes into structured user motivation statements without manual synthesis.

## Requirements

- A folder containing custdev transcripts or interview notes (.md or .txt format)
- Minimum 1 file; optimal 3–15 for meaningful frequency analysis
- Files should contain qualitative text (quotes, notes, open-ended responses) — not just numeric ratings

## How to Use

1. Trigger the skill (see triggers below)
2. Point Claude to the folder containing your custdev files
3. Receive a JTBD map with: ranked statements, evidence quotes, source references, confidence labels, and a Patterns & Gaps section

## Examples

**Example 1 — After a sprint of user interviews:**
> "Extract jobs to be done from my interviews folder"

Claude reads all files in the folder, clusters motivation signals, and returns a ranked JTBD table with evidence quotes and a Patterns & Gaps section highlighting recurring themes.

**Example 2 — Preparing for a roadmap session:**
> "JTBD from interviews — I have 8 transcript files in /research/q2-custdev/"

Claude processes all 8 files, assigns High/Medium/Low confidence based on cross-file frequency, and delivers a map you can paste directly into your roadmap planning doc.

## Triggers

| English | Russian |
|---------|---------|
| `extract jobs to be done` | `извлеки JTBD из интервью` |
| `JTBD from interviews` | `синтез custdev заметок` |
| `synthesize custdev notes` | `что хотят пользователи из транскриптов` |
| `what are my users trying to do` | `сформируй jobs to be done` |

## User Guide

See [docs/USER-GUIDE.md](docs/USER-GUIDE.md) (EN) · [docs/USER-GUIDE.ru.md](docs/USER-GUIDE.ru.md) (RU)
