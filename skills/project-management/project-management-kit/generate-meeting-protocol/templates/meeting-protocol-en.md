# Meeting Protocol: {{meeting_title}}

**Project:** {{project_name}}
**Meeting date:** {{meeting_date}}
**File:** `meeting-protocol-{{meeting_date}}.md`
**Document status:** `draft`
**Meeting type:** {{meeting_type}}
**Facilitator:** {{facilitator}}
**Scribe:** AI agent
**Source:** {{source_notes}}

---

## 1. Participants

| Name | Role | Attendance |
|------|------|------------|
| {{participant_name}} | {{role}} | yes / no |

---

## 2. Agenda

| # | Topic | Status |
|---|-------|--------|
| 1 | {{agenda_item}} | discussed / deferred / dropped |

---

## 3. Key Decisions

| ID | Decision | Initiator | Status |
|----|----------|-----------|--------|
| D001 | {{decision}} | {{initiator}} | accepted / deferred |

---

## 4. Action Items

| ID | Action | Owner | Deadline | Priority |
|----|--------|-------|----------|----------|
| A001 | {{action_item}} | {{owner}} | {{deadline}} | H/M/L |

---

## 5. Project Plan Changes

| What changed (ID: WP-xxx / Mx) | Was | Becomes | Basis (decision ID) |
|--------------------------------|-----|---------|---------------------|
| {{change_item}} | {{old_value}} | {{new_value}} | D00x |

---

## 6. Open Issues

- {{open_question}}

---

## 7. Next Meeting

**Date:** {{next_meeting_date}}
**Topic:** {{next_meeting_topic}}

---

## Changelog

| Date | Version | Change |
|------|---------|--------|
| {{meeting_date}} | 1.0 | Created by agent based on meeting notes |
| 2026-03-24 | 1.1 | Added fields "File", "Document status", "Source" based on template analysis |
| 2026-03-25 | 1.2 | Section 5: added ID format hint (WP-xxx / Mx) to "What changed" column header |
| 2026-03-26 | 1.3 | Removed conditional deletion instructions for sections 5/6/7 — moved to SKILL.md |
| 2026-03-28 | 1.4 | Translated to English |
