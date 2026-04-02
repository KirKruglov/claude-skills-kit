# generate-meeting-protocol

Generates a structured meeting protocol from free-form notes.

## Overview

Transforms unstructured meeting notes into a formal protocol with decisions, action items, and proposed changes to project documents. Can be used in any project phase.

**Phase:** any (independent skill)
**Output:** `meeting-protocol-{date}.md`

## Triggers

| Language | Commands |
|----------|----------|
| English | "generate meeting protocol", "meeting notes", "meeting minutes" |
| Russian | «оформи протокол», «протокол встречи», «обработай заметки со встречи» |

## Required Inputs

| Data | Required | Notes |
|------|:--------:|-------|
| Meeting notes | yes | Any format: bullet points, free text, chat copy, voice dictation transcript |
| Project plan | no | If available — changes are linked to work packages (WP-xxx) |
| Previous protocols | no | For tracking action item completion |

## Output Structure

The protocol contains: meeting metadata (date, attendees, agenda), key discussion points, decisions made, action items (who, what, by when), and proposed changes to project plan or other documents.

## Dependencies

**Requires:** meeting notes from the user (no prior skills needed).

**Unlocks:** no downstream dependencies. This is a standalone utility skill.

## Example

> Here are the notes from today's sprint demo. Attendees: PM, 2 devs, designer, customer. We discussed the prototype, customer requested 2 changes, and we decided to push the launch by 1 week.

Agent produces a structured protocol with decisions, action items with owners and deadlines, and a proposed update to the project plan.
