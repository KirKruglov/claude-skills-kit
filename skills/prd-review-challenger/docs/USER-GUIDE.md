# prd-review-challenger — User Guide

A devil's advocate for your product documents. Paste any PRD or feature spec — get a structured critique covering weak assumptions, open questions, implementation risks, and what's missing.

---

## How to Start

Open a conversation with Claude and use one of these phrases:

```
Review my PRD
Challenge my spec
Devil's advocate for my product doc
Find holes in my PRD
Critique my feature spec
Stress-test my PRD
What's missing in my spec
```

Then paste your document directly into the chat.

Claude will recognize the skill and begin the workflow.

---

## Step-by-Step Walkthrough

**Step 1 — Paste your document.** Copy your PRD, feature spec, or product decision text and send it in the conversation. Add context if relevant: target audience, project stage, or what angle you want focused on (UX risks, technical complexity, business assumptions).

**Step 2 — Claude assesses the document type.** If the document is too short for a full review, Claude will say so and give feedback on what's available. If it's a technical doc (not a PRD), Claude applies the same critical approach and notes the difference.

**Step 3 — Completeness checklist.** Claude checks whether the document covers: problem statement, target audience, user stories, acceptance criteria, edge cases, success metrics, out-of-scope items, technical dependencies, rollback plan, and cross-product impact.

**Step 4 — Four-axis critique.** Claude produces the structured review in four sections (see "What You Get" below).

**Step 5 — Top-3 priorities.** Claude closes with the three most critical gaps to close before development starts.

---

## Examples

### Example 1: Pre-review check before team presentation

**You say:**
> "Review my PRD. We're building a self-serve onboarding flow for new B2B users — launch in 6 weeks. [PRD text follows]"

**Claude responds:**
> "**Weak spots and hidden assumptions:** The document assumes all new users are technical decision-makers, but doesn't define what happens when an admin invites a non-technical colleague. This path is undocumented..."
> [continues with all five sections]

### Example 2: Validating an updated spec before dev kickoff

**You say:**
> "Devil's advocate for this spec — we've updated it after design review. [spec text]"

**Claude responds:**
> "The acceptance criteria in section 3 now conflict with the edge case described in section 5 — when the user has zero previous sessions, the fallback described in AC-3 doesn't match the behavior shown in EC-2..."
> [continues with full critique]

---

## What You Get

A structured review document with five sections:

**1. Weak spots and hidden assumptions** — specific statements in the doc that are treated as facts but haven't been validated or explained, with direct references to the relevant passages.

**2. Open questions** — questions the document doesn't answer but engineers and designers will ask (e.g., "What happens when [edge condition]?").

**3. Implementation and UX risks** — technical risks (complexity, dependencies, performance, security) and UX risks (confusing behavior, friction, edge cases in the interface) with the consequence of ignoring each.

**4. Alternative approaches** — 2–3 other ways to solve the same problem, with trade-offs stated explicitly.

**5. Completeness checklist** — a table showing which standard PRD components are present, missing, or partial, followed by a top-3 priority list of what to fix before development.

---

## Tips for Best Results

Give context upfront. The more Claude knows about your product's audience, constraints, and stage, the more targeted the critique. A one-liner like "B2B SaaS, SMB segment, 6-week runway" changes the quality of feedback significantly.

Specify your angle. If you only care about technical risks right now, say so: "Focus on implementation risks." The skill covers all four axes by default, but can zoom in.

Use it on early drafts. The earlier you run a critique, the cheaper it is to fix. Waiting until the doc is "ready" defeats the purpose.

Don't dismiss every critique. Some observations will seem obvious in hindsight — that's the point. The discomfort is the value.

---

## FAQ

**Q: Can I paste a PRD in English even if my other documents are in Russian?**
A: Yes. The skill responds in the language of the document you paste. If you want the critique in a different language, just say so explicitly.

**Q: The PRD is confidential — is it safe to paste it?**
A: The skill runs inside your Claude session. Anthropic's data handling policies apply. For highly sensitive internal documents, consult your company's policy on using AI tools. The skill itself doesn't store or transmit anything beyond the standard Claude session.

**Q: Can the skill also fix the PRD based on its own critique?**
A: No — the skill critiques, not rewrites. This is intentional: editing is the PM's job. If you want Claude to write or rewrite a PRD, use the product-management write-spec skill.

---

## Limitations

- Does not write, rewrite, or improve PRDs — critique only
- Does not have domain knowledge about your specific product without context you provide
- Does not replace review with engineers, designers, and actual stakeholders
- Very short documents (under 3 paragraphs) will receive partial feedback with a note on what's structurally missing
- Does not provide legal, financial, or security assessments without relevant specialist context

---

## Need Help?

If the skill isn't working as expected, check the [installation guide](INSTALL.md) to make sure everything is set up correctly.
