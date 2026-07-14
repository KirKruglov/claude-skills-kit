# Feature Announcement Writer — User Guide

Practical scenarios for turning a feature description into a ready-to-send announcement pack.

---

## Quick Start

Here's the fastest way to get your announcement:

1. Write or paste a 1–2 paragraph feature description
2. Say: "Write feature announcement" and paste the text
3. Receive 4 copy-ready formats: changelog, email, push, social post

**Result:** A complete announcement pack you can copy directly into each channel.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Solo PM launching a feature without a marketing team

**Situation:**
You've just shipped a new feature. There's no dedicated marketing support — you need to write the announcement yourself across changelog, email, Notion update, and LinkedIn. You have 20 minutes before the team standup.

**What to do:**
1. Open Claude with the Feature Announcement Writer skill active
2. Say: "Write feature announcement" and paste your feature brief (even a rough draft works)
3. If the skill asks for product name or audience, answer in one message
4. Copy the 4 output sections into your respective destinations:
   - Changelog entry → paste into CHANGELOG.md
   - Email → paste into your email client, review subject line, send
   - Push notification → paste into your in-app message tool
   - Social post → paste into LinkedIn or X, schedule or post

**Expected result:**
Four distinct, channel-appropriate texts generated in under a minute. Each respects the format constraints of its channel (160 chars for push, hook-first for social, benefit-first subject for email).

---

### Scenario 2: Announcing a beta feature to early users

**Situation:**
You're rolling out a new feature in beta to a limited group. You need messaging that's honest about the beta status, generates excitement, and doesn't overpromise. The audience is experienced users who opted into early access.

**What to do:**
1. Trigger: "Generate announcement for my feature"
2. Provide your description and add: "This is a beta launch, early users only"
3. The skill will detect the beta context and:
   - Add `[Beta]` prefix in changelog
   - Adjust email tone to "you're in the beta" framing
   - Keep push tight and excitement-forward
   - Write social post as a "who wants in?" invitation

**Expected result:**
Beta-appropriate copy across all 4 formats — consistent messaging that won't confuse users about availability or maturity.

---

### Scenario 3: Adapting an engineering description for non-technical users

**Situation:**
Your developer wrote a technically accurate description of a new feature. It's full of API terms and implementation details. You need user-facing copy, not a tech spec.

**What to do:**
1. Paste the developer's description as-is
2. If the skill flags it as technical: respond "user-facing" to confirm the switch
3. The skill will extract the underlying user benefit and generate plain-language copy

**Expected result:**
User-facing copy that translates technical implementation into concrete benefits. What the code does → what the user can now accomplish.

---

## Tips

**1. The more specific the input, the better the output.**
"Added export" produces generic copy. "Users can now export any dashboard as PDF in one click, directly from the header menu" gives the skill enough to write specific, benefit-first copy.

**2. Use defaults for speed, override only when it matters.**
Audience defaults to `users`, launch type defaults to `GA`. If you're writing for enterprise customers or a beta group, say so — the framing changes significantly.

**3. Ask for the blog intro only if you need it.**
The skill offers a blog intro at the end of every output. It won't generate it automatically. This keeps the default output focused and fast.
