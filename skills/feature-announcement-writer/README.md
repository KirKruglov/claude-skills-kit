# Feature Announcement Writer

Turn a single feature description into a ready-to-send announcement pack — in 4 formats, no copywriting required.

---

## Overview

Feature Announcement Writer generates a multi-format communication pack from a plain-language product feature description. It produces four ready-to-use formats — changelog entry, email announcement, in-app push notification, and social post — tailored to the feature's audience and launch type. Use this skill when launching a new feature and need copy for multiple channels at once, preparing a beta announcement without a marketing team, or adapting a feature description written for engineers into user-facing communication.

---

## Requirements

- A feature description (plain text, pasted inline or as a `.md` file — minimum 1 paragraph)
- Optional: product name, feature name, target audience, launch type

No additional tools or skills required. Works entirely from the description you provide.

---

## How to Use

1. **Describe your feature**
   - Write or paste a 1–2 paragraph plain-language description of what the feature does and who benefits

2. **Trigger the skill by saying:**
   - "Write feature announcement"
   - "Generate announcement for my feature"
   - In Russian: "Напиши анонс фичи" or "Создай пакет анонса"

3. **Provide optional context** (or let defaults apply)
   - Product name, feature name, audience type (users / customers / internal / developers), launch type (GA / beta / soft launch)
   - Defaults: audience = users, launch type = GA

4. **Receive your announcement pack**
   - 4 copy-ready sections: changelog entry, email, push notification, social post
   - Copy each section directly to its destination channel

---

## Examples

### Example 1: New Export Feature Launch

**Input:**
> We just shipped PDF export for reports. Users can now export any report to a clean, formatted PDF in one click — no more screenshots or manual reformatting. Works for all report types. Available to all users starting today.

**Output:**

📋 **Changelog:** `- PDF Export: Export any report to a clean PDF in one click — no screenshots required.`

📧 **Email Subject:** `New: Export reports as PDF — available today`

📱 **Push:** `Export any report to PDF in one click. No more screenshots or reformatting. Try it now.` _(88 chars)_

🔗 **Social:** `Tired of screenshotting reports to share them? We fixed that. PDF export is now live — pick any report, hit export, done. Try it and let us know what you think.`

---

### Example 2: Beta Feature Announcement

**Input:**
> We're rolling out AI-powered meeting summaries to beta users. After each meeting, Claude automatically generates a structured summary with key decisions, action items, and next steps — directly in your workspace. No manual note-taking required. Beta access starts this week for early users.

**Output:**

📋 **Changelog:** `- [Beta] AI Meeting Summaries: Automatic post-meeting summaries with decisions, action items, and next steps — no manual notes needed.`

📧 **Email Subject:** `[Beta] AI meeting summaries are live — you're in`

📱 **Push:** `AI meeting summaries are here. Get decisions, action items, and next steps automatically after every meeting. _(107 chars)_`

🔗 **Social:** `What if every meeting ended with a perfect summary — automatically? We're testing AI-powered meeting summaries with early users this week. Structured output, no manual notes. Who wants in?`

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Write feature announcement | Напиши анонс фичи |
| Feature announcement writer | Генератор анонса фичи |
| Generate announcement for my feature | Создай пакет анонса |
| I need to announce a new feature | Мне нужно анонсировать новую функцию |

---

**Version:** 1.0.0  
**Last updated:** 2026-05-14
