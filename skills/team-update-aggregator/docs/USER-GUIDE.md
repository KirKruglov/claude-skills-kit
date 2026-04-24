# Team Update Aggregator — User Guide

## What This Skill Does

Reads weekly update files from your team and produces a `team-status-YYYY-MM-DD.md` report organized by person. Each team member gets a section with:
- What they accomplished this week
- What they plan to do next week
- What's blocking them
- Capacity / out-of-office notes
- Manager attention flags (⚠️)

---

## Preparing Your Input Files

### Option A: One file per person

Create one `.md` or `.txt` file per team member. The filename becomes the person's name in the report.

```
/updates/
├── anna-ivanova.md
├── john-smith.md
├── maria-petrova.md
└── alex-lee.md
```

Each file can be free-form — the skill extracts structured content automatically.

**Minimal file example (`anna-ivanova.md`):**
```
Completed: shipped search feature, fixed 3 bugs
Next week: start API refactor
Blockers: waiting for design review from Maria
```

### Option B: One file with all updates

Use H2 (`##`) or H3 (`###`) headers with team member names:

```markdown
## Anna Ivanova

Shipped the search feature this week. Waiting for design review before starting the API refactor.

## John Smith

Completed sprint planning and unblocked the data pipeline. Next week: focus on reporting dashboard.
```

### Option C: Mixed structure

Files with a `Name:` or `Who:` field at the top:

```
Name: Maria Petrova
---
This week I finished the onboarding flow. Feeling a bit overloaded — would help to discuss priorities.
```

---

## Trigger Phrases

Type one of these to start the skill:

**English:**
- `Aggregate team updates from /path/to/folder/`
- `Compile team status from these files: file1.md, file2.md`
- `Build team status report for this week`
- `Who's working on what — compile from updates/`

**Russian:**
- `Агрегируй обновления команды из /path/to/folder/`
- `Составь статус команды из этих файлов: file1.md, file2.md`
- `Скомпилируй people-отчёт по команде`

---

## Reading the Output

The output file `team-status-YYYY-MM-DD.md` has four sections:

### 1. Summary
2–4 sentences on overall team health, key wins, main blockers, and who needs your attention.

### 2. Team Members
One subsection per person. Manager flags (⚠️) appear when the skill detects stress signals, overload, unresolved blockers, or requests for help.

### 3. Cross-Team
- **Shared blockers** — the same blocker mentioned by 2+ people
- **Dependencies** — Person A waiting on Person B
- **Unowned action items** — actions without a named owner

### 4. Files Processed
What was included, skipped, or had unidentified owners.

---

## Tips

- **Name your files clearly.** `anna.md` works better than `update3.md`.
- **Encourage consistent format.** Even a 3-bullet update (done / next / blocked) is enough.
- **Run weekly.** Pair with `one-to-one-prep` before your 1-on-1s.
- **Large teams (10+).** The skill adds a "Large team" notice at the top — review the output for completeness.

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| "No files found" | Check the folder path; make sure files are `.md` or `.txt` |
| Person shows up as "Unknown" | Add their name as an H1 heading or `Name:` field in the file |
| Output file already exists | The skill will ask before overwriting — confirm or choose `-v2` |
| File has no content | Skill skips it and lists it under "Files with no updates" |
