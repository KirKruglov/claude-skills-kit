# User Guide: Competitive Feature Matrix Builder

---

## Quick Start

1. Save your competitor notes as separate `.md` or `.txt` files in one folder (one file per competitor)
2. Optionally add `your-product.md` with your own feature list for gap comparison
3. Say: **"Build a competitive feature matrix from [folder path]"**
4. Get a Feature Matrix table, Gap Analysis, and Recommendations

---

## Scenario 1: Pre-Roadmap Competitive Review

**Situation:** You're preparing for a quarterly roadmap planning session. You have notes on 4 competitors collected over the past few weeks, sitting in a folder as separate markdown files. You need a single table that shows which features each competitor has, and where your product lags behind.

**What to do:**

1. Open your notes folder (e.g., `/research/q2-competitive/`). Make sure you have one file per competitor.
2. Add a `your-product.md` file listing your own product's features in the same folder.
3. Trigger the skill:
   > "Build a competitive feature matrix from my /research/q2-competitive/ folder"
4. Review the Feature Matrix table — check the ✓/✗/? symbols for accuracy; adjust your notes if something was misread.
5. Share the Gap Analysis section with your team as the basis for roadmap discussion.

**Expected result:** A ready-to-paste markdown document with the full matrix and a prioritized gap table (High / Medium / Low). The Recommendations section provides 2–4 specific action bullets based on what you're missing.

**Tip:** The more structured your notes (bullet lists of features, clear headings), the more accurate the extraction. Even messy notes work — the skill flags lower-confidence extractions so you can review them.

---

## Scenario 2: Feature Positioning Before a Sales Meeting

**Situation:** Your sales team has a meeting with a prospect who is also evaluating two competitors. You need a quick comparison to understand your differentiators and the gaps you should address in the conversation.

**What to do:**

1. Gather your existing competitor notes (even rough notes from LinkedIn, product pages, or internal docs) into a folder.
2. Trigger the skill:
   > "Competitive feature matrix from /sales-intel/prospect-eval/"
3. In the output, look at the **Your Differentiators** section — these are features unique to your product.
4. Look at the **High priority gaps** — these are features competitors have that you don't; be ready to address them in the conversation.
5. Copy the matrix into your sales prep doc.

**Expected result:** A clear view of where you win (differentiators) and where competitors have an edge (gaps), grounded in your own research notes — not generic market data.

---

## Scenario 3: Single-Competitor Deep Dive

**Situation:** You only have notes on one competitor right now, and you want a structured feature list before adding more competitors later.

**What to do:**

1. Put the competitor notes in a folder (e.g., `/research/notion/`).
2. Trigger the skill:
   > "Build a feature matrix from /research/notion/"
3. The skill will generate a single-column feature list and note that gap analysis requires 2+ competitors.
4. Use the extracted feature list as a starting template — add more competitor files to the folder and re-run when ready.

**Expected result:** A normalized feature list for the one competitor, ready to extend. The skill notes what's missing (self-comparison, gap analysis) so you know exactly what to add next.

---

## Tips

- **Name your files clearly:** The skill extracts competitor names from filenames (e.g., `hubspot-notes.md` → "Hubspot") or from the first `# Heading` in the file. Clear names = clean column headers in the matrix.
- **Use `your-product.md` for real gap analysis:** Without it, the skill builds a competitor-only comparison. Add your own feature list to unlock the Gap Analysis and Recommendations sections.
- **Unstructured prose still works:** If your notes are paragraphs rather than bullet lists, the skill uses sentence-level extraction. It flags these extractions as lower-confidence so you can review before sharing.
- **Re-run after updating notes:** The skill reads files fresh each time. Update your notes, re-trigger, and get an updated matrix in seconds.
