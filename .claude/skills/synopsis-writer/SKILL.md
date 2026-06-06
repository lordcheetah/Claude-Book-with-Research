---
name: synopsis-writer
description: Generate submission and marketing materials from a completed manuscript — agent query synopsis, back-cover blurb, logline, and query letter opening. Use after the manuscript is complete or substantially complete. Reads the full manuscript and bible, then produces each document type on request.
---

# Synopsis Writer

Generate professional submission and marketing materials from your manuscript. Each document type has different requirements — this skill produces the right format for each.

## Quick Start

```
/synopsis-writer projects/my-novel
```

Produces all four document types and saves them to `projects/my-novel/submissions/`.

Or request specific types:
```
/synopsis-writer projects/my-novel --type synopsis
/synopsis-writer projects/my-novel --type blurb
/synopsis-writer projects/my-novel --type logline
/synopsis-writer projects/my-novel --type query-opening
```

## Inputs Required

Before generating, load:
- All completed chapters: `{PROJECT_ROOT}/story/chapters/*.md`
- `{PROJECT_ROOT}/story/synopsis.md` — the original pitch (for comparison)
- `{PROJECT_ROOT}/bible/characters/*.md` — character identities and arcs
- `{PROJECT_ROOT}/bible/style.md` — genre, tone, audience

## Document Types

### 1. Logline (1–2 sentences)
The elevator pitch. Structure: **[protagonist] must [goal] before [stakes], but [obstacle].**

Rules:
- Name the protagonist and their defining attribute
- State the central conflict in active terms
- State what's at stake if they fail
- Include the genre feel in the word choice
- No more than 35 words

### 2. Back-Cover Blurb (150–200 words)
What readers see before buying. Structure: hook → situation → conflict → stakes → tease.

Rules:
- Open with the most compelling sentence in the book (not the first sentence — the best one for marketing)
- Establish protagonist and world in 2–3 sentences
- State the core conflict without spoiling the resolution
- End on a question or unresolved tension that makes the reader want to open the book
- Match the genre's blurb conventions (thriller blurbs are different from literary fiction)
- Do not reveal the ending

### 3. Query Synopsis (1–2 pages / 500–800 words)
What agents read to evaluate the full story. Rules for this format:
- **Does include the ending** — agents need to know the full arc
- Third person, present tense regardless of the novel's tense
- Follow the story in order (no non-linear structure)
- Cover every major plot point; skip subplots unless they're essential to understanding the main arc
- Include emotional beats, not just plot events
- Name all significant characters on first mention
- One paragraph per major act/movement

Format:
```
[Title], [Genre], approximately [word count] words.

[Plot summary paragraphs]

[Ending paragraph — how it resolves]
```

### 4. Query Letter Opening (2–3 paragraphs)
The hook section of a query letter (not the full letter — just the manuscript pitch section).

Paragraph 1: Hook the agent — logline or the most compelling statement about the book.
Paragraph 2: Expanded pitch — protagonist, world, conflict, stakes (2–5 sentences each).
Paragraph 3: Comp titles and positioning — "For fans of [Title] and [Title]" with brief explanation of how this book compares.

Rules:
- Address the specific agent's interests if known (skip if not)
- Comp titles should be recent (last 5 years) and successful but not #1 bestsellers
- Paragraph 2 should not summarize the whole plot — just enough to create desire to read more

## Output

Save all generated materials to `{PROJECT_ROOT}/submissions/`:
- `logline.md`
- `back-cover-blurb.md`
- `query-synopsis.md`
- `query-letter-opening.md`
- `submissions-README.md` — brief notes on how each was generated and what to customize

## Interaction Style

After generating each document:
- Ask if the emphasis is right (is this the right protagonist to lead with? The right conflict to foreground?)
- Offer to adjust for specific agents or markets if the writer specifies
- Note any places where the manuscript's actual content diverged significantly from the synopsis (this sometimes reveals that the written story has a different center than the planned story — worth the writer knowing)

The goal is professional, submission-ready materials — not a rough draft the writer has to heavily rewrite.
