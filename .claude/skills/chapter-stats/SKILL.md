---
name: chapter-stats
description: Generate a statistics dashboard for the manuscript — word counts, pacing metrics, dialogue ratios, sentence length, and structural shape. Use at any point to understand how the manuscript is shaped. Results help identify outlier chapters, pacing imbalances, and structural patterns.
---

# Chapter Stats

Generate a statistics dashboard across all written chapters.

## Quick Start

```
/chapter-stats projects/my-novel
```

## What It Measures

For each chapter:

| Metric | Method |
|--------|--------|
| Word count | Direct count |
| Paragraph count | Count double-newline blocks |
| Estimated read time | Word count ÷ 250 wpm |
| Dialogue ratio | Lines starting with `"` or `«` ÷ total lines |
| Average sentence length | Words ÷ sentence count |
| Longest sentence | Highest word count in a single sentence |
| Scene break count | Count `---` or `***` separators |

Across the full manuscript:

| Metric | Value |
|--------|-------|
| Total word count | — |
| Chapter count | — |
| Average chapter length | — |
| Shortest chapter | — |
| Longest chapter | — |
| Standard deviation | — |
| Total estimated read time | — |
| Overall dialogue ratio | — |

## Workflow

1. Load all chapter files from `{PROJECT_ROOT}/story/chapters/*.md`, sorted by filename
2. For each chapter, extract metrics via text analysis
3. Calculate cross-chapter statistics
4. Build the dashboard
5. Flag outliers

## Output

Save to `{PROJECT_ROOT}/story/manuscript-stats.md`:

```markdown
# Manuscript Statistics — [Project Name]
*Generated: [date] — [N chapters, N words total]*

---

## Summary

| | Value |
|--|-------|
| Total word count | N |
| Chapters written | N |
| Average chapter length | N words |
| Estimated total read time | N hours N minutes |
| Overall dialogue ratio | N% |

---

## Per-Chapter Statistics

| Chapter | Title | Words | Read Time | Dialogue % | Avg Sentence | Scenes |
|---------|-------|-------|-----------|------------|--------------|--------|
| 01 | ... | N | Nm | N% | N words | N |
...

---

## Shape Analysis

### Word Count Distribution
[ASCII bar chart showing relative chapter lengths]

Ch01 ████████████ 3,200
Ch02 ████████████████ 4,100
Ch03 ████████ 2,000  ← notably short
...

### Dialogue Ratio by Chapter
[ASCII bar chart]

### Outlier Flags
- **Longest**: Chapter [X] at [N] words ([X]% above average)
- **Shortest**: Chapter [X] at [N] words ([X]% below average)
- **Most dialogue-heavy**: Chapter [X] at [N]%
- **Least dialogue**: Chapter [X] at [N]%
- **Pacing note**: Chapters [X–Y] are all below average length — potential for thin coverage of [Act]

---

## Pacing Rhythm
[Visualization of chapter length pattern — does it vary? long-short-long? steady?]

Consistent rhythm: [assessment]
Variation: [standard deviation interpretation — tight/moderate/wide]
```

## Flags Worth Noting

The skill will surface:
- Any chapter more than 50% longer than average (may be overpacked)
- Any chapter less than 50% of average length (may be thin)
- 3+ consecutive chapters at below-average length (structural sag zone)
- Dialogue ratio below 10% (very dense prose — intentional?)
- Dialogue ratio above 70% (very dialogue-heavy — intentional?)
- Average sentence length above 30 words (potentially complex prose)

These are observations, not problems. Some outliers are intentional (a short punchy climax chapter; a dialogue-free action sequence). The writer decides what to act on.

## Optional: Wolfram Calculation

For reading level analysis (Flesch-Kincaid), the skill can invoke `wolfram-alpha-api-automation` with sample text to get a readability estimate. This requires sampling approximately 30 sentences from across the manuscript.
