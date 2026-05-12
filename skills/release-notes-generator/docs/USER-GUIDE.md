# User Guide: Release Notes Generator

## Quick Start

Here's the fastest way to get your release notes:

1. Write your sprint results or product updates in a `.md` or `.txt` file — plain language, no special structure needed
2. Place the file in your Cowork workspace
3. Say: "Generate release notes from [filename]"
4. Claude filters, formats, and hands you 4 ready-to-use versions

**Result:** Changelog entry, email, push notification, and social post — all ready to copy and send.

**Time:** ~3 minutes

---

## Your Input File — What to Write

There's no required format. Write the way you normally write sprint notes. A few examples of what works:

**Minimal (bullet list):**
```
Sprint 23 — v2.4.0 — May 2026

- Added 3 new filter options to the Reports section
- Improved CSV export speed by 40%
- Fixed login error affecting SSO users
- Refactored auth module (internal)
- Updated CI pipeline (internal)
```

**Verbose (prose + bullets):**
```
# Product Update — May 2026

This sprint we focused on the Reports section and fixed a long-standing SSO issue.

New features:
- Three new filter types: date range, tag, and status
- Bulk export to CSV now 40% faster

Bug fixes:
- Fixed: users with SSO login saw an error on the first login after password reset

Internal (not for release notes):
- Refactored auth module
- Migrated users table to new schema
```

Both inputs produce the same quality of output. Claude figures out what's user-facing and what's not.

---

## Scenarios

### Scenario 1: Regular sprint release — distributing across channels

**Situation:** Sprint 23 just wrapped. You have a bullet list of what shipped and need to share updates with customers via email, push notification, and LinkedIn — plus keep your CHANGELOG.md up to date.

**What to do:**
1. Drop your sprint notes file into the Cowork workspace (`sprint-23.md`)
2. Say: "Generate release notes from sprint-23.md"
3. Claude reads the file, filters out the internal items, and produces all 4 formats
4. Copy the changelog entry → paste into CHANGELOG.md
5. Copy the email → paste into your email tool, review once, send
6. Copy the push notification → paste into your in-app notification tool
7. Copy the social post → paste into LinkedIn/X, review, post

**Expected result:** Four formats ready in one run. The "Internal Changes" section at the bottom shows you what Claude excluded — verify it looks right.

---

### Scenario 2: Hotfix release — fast and reassuring

**Situation:** You pushed a hotfix to fix a login error affecting SSO users. You need to communicate this quickly and clearly — the message needs to start with "it's fixed" rather than "here's what's new."

**What to do:**
1. Write a short file: `hotfix-2026-05-12.md` with one or two lines:
   ```
   Hotfix — May 12, 2026
   Fixed: login error affecting users with SSO after password reset
   ```
2. Say: "Write release notes from hotfix-2026-05-12.md"
3. Claude detects the hotfix context and adjusts tone to reassurance-first in all 4 formats

**Expected result:**
- Email subject: "Fixed: login issue for SSO users"
- Email body opens with: "We've resolved the login error..."
- Push: "Fixed: login error for SSO users — all systems normal"
- Social: "Quick update: we patched a login issue affecting SSO users. Everything is back to normal."

---

### Scenario 3: Major release — lots of changes

**Situation:** Q2 just closed and you shipped 15 features. The sprint notes file is long.

**What to do:**
1. Prepare `q2-release.md` with all changes grouped loosely by area
2. Say: "Generate release notes from q2-release.md"
3. Claude generates all 4 formats, grouping highlights and summarising secondary changes
4. Claude will note: "This looks like a major release — a dedicated blog post might be worth the effort. Want me to draft an intro?" — say yes if you need one

**Expected result:** All 4 formats sized for the scope of the release; email covers top 3–4 highlights with a note "and more" for the rest; social post leads with the flagship feature.

---

## Tips

**Keep internal items in the file — Claude will filter them.** You don't need to pre-clean your sprint notes. Mark internal items with "(internal)" or just leave them as-is — Claude classifies each item and lists excluded ones separately so you can verify.

**Name your file with a version or sprint number.** Files like `sprint-23.md` or `v2.4.0-release.md` help Claude populate the changelog header automatically without asking.

**For hotfixes, include the word "hotfix" or "patch" in the filename.** This triggers the reassurance-first tone adjustment across all formats.

**The push notification is the hardest format to write.** Claude keeps it under 160 characters, but if you feel it's too generic, ask: "Make the push more specific about [feature name]." One-shot edits work well.

**The social post is ready to post — but review it.** Claude avoids emojis by default and keeps the tone professional. If your brand uses emojis, say "add relevant emojis to the social post" and Claude will revise.
