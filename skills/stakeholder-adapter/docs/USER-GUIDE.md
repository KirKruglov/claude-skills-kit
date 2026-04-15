# stakeholder-adapter — User Guide

Turn one document into ready-to-send versions for every audience — no manual rewriting required.

---

## How to Start

Open a conversation with Claude and use one of these phrases:

- "Adapt this document for leadership and the client: [paste document]"
- "I need different versions of this status update"
- "Create an executive version of this PRD"
- "Tailor this for our client"
- "stakeholder adapter"

Claude will recognize the skill and begin the workflow.

---

## Step-by-Step Walkthrough

**Step 1 — Provide your document**

Paste your document text directly into the message, or provide a path to a `.md` or `.txt` file. You can include the document in your trigger message or paste it when Claude asks.

**Step 2 — Claude asks clarifying questions (if needed)**

If you didn't already specify the target audiences, document type, or key message, Claude will ask them in a single step:

- Which audiences? (Leadership, Team, Client — choose one, two, or all three)
- What type of document?
- Is there a key message that must appear in every version?

**Step 3 — Claude generates adapted versions**

You get one clearly labeled section per selected audience. Each version is ready to copy and send.

**Step 4 — Save to files (optional)**

After presenting the versions, Claude offers to save them as separate `.md` files. Say "yes" and it writes them to your working directory.

---

## Examples

### Example 1: Status update for multiple stakeholders

**You say:**
> "Adapt this for leadership, the team, and the client:
> Sprint 12 complete. Implemented auth module, fixed 3 critical bugs (AUTH-42, API-17, UI-33). CDN config dependency resolved via DevOps on Apr 14. Remaining: final E2E tests, load testing (2 days). Known risk: load test may surface latency issues in the EU region. Delivery target: Apr 22."

**What you get:**

---
**Version for Leadership / Executives**

For information. Sprint 12 complete. All critical issues resolved; infrastructure dependency closed April 14. Final testing in progress — delivery remains on track for April 22. One low-level risk: potential latency in EU region under load. Monitoring in progress; no action required at this time.

---
**Version for Engineering / Team**

Sprint 12 done. Auth module shipped; bugs AUTH-42, API-17, UI-33 fixed. CDN config dependency: resolved (DevOps, Apr 14). Remaining tasks: E2E tests + load testing — 2 days estimated. Risk: EU region latency may surface during load test. Owner: [assign]. Target: Apr 22. No blockers.

---
**Version for Client / External partner**

Sprint 12 is complete. All planned features are implemented and critical issues resolved. We're in final testing and on track for the April 22 delivery. Next steps: we'll share a testing preview by April 20 for your review.

---

### Example 2: PRD adapted for leadership only

**You say:**
> "Create an executive version of this PRD: [paste PRD]"

Claude generates a single leadership version — concise, decision-focused, milestone-level timeline.

---

## What You Get

- One clearly labeled section per selected audience
- Leadership version: ~25–35% of the original, decision or impact at the top
- Team version: full technical depth, structured for action
- Client version: outcome language, no jargon, ends with "Next steps"

If your document contains potentially sensitive internal data, the client version will include a ⚠ flag — you decide whether to remove or rephrase before sending.

---

## Tips for Best Results

- Include the document **in your trigger message** to skip the prompting step
- Specify audiences upfront: "for leadership and the client" is enough for Claude to skip Q1
- Provide a key message if there's a commitment, date, or decision that must appear in all versions
- Review the client version for internal data before forwarding — Claude flags suspected sections but doesn't auto-remove them
- For very long documents (2000+ words), ask Claude for a condensed executive version (max 150 words)

---

## FAQ

**Q: Can I request just one audience version?**
A: Yes. Say "create an executive version" or select only "Leadership" — you'll get a single adapted section.

**Q: Can I ask Claude to adjust a version after it's generated?**
A: Yes. Say "make the leadership version shorter" or "add the delivery date to the client version" and Claude will update it.

**Q: Does the skill rewrite my document from scratch?**
A: No. It reframes and adapts your existing content. It does not add invented facts, dates, or commitments.

**Q: What if my document is in Russian?**
A: Claude detects the source language and adapts all versions in Russian. If you need a different language, specify it.

**Q: Will the skill save files automatically?**
A: No. Claude will ask after presenting versions. Say "yes" to save, or just copy from the chat.

---

## Limitations

- Adapts existing content only — does not generate new information
- Does not automatically remove sensitive data from client versions — flags it for your review
- Does not replace human review before sending to stakeholders
- Supported input formats: pasted text, `.md`, `.txt` (not `.docx`, `.pdf`, `.xlsx`)

---

## Need Help?

If the skill isn't working as expected, check the [installation guide](INSTALL.md) to make sure everything is set up correctly.
