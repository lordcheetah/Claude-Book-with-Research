# Claude Book Framework

A multi-agent framework for writing novels and nonfiction books with Claude Code. Supports multiple simultaneous projects, series bibles, English and non-English output, and research-assisted writing for any genre.

## Repository Structure

```
├── CLAUDE.md                 # Orchestrator — coordinates all agents
├── .claude/
│   ├── agents/               # 16 specialized sub-agents
│   └── skills/               # 6 reusable skills
├── projects/                 # YOUR book projects (one subdirectory per book)
├── series/                   # Series bibles (shared across related books)
│   └── _template/            # Templates for series bible files
├── examples/
│   ├── english-starter/      # Near-future thriller — complete English example
│   └── club-des-cinq/        # French children's adventure — 18 chapters written
├── bible/                    # Templates (copy to your project's bible/)
│   ├── style.md.example
│   ├── structure.md.example
│   ├── characters/_template.md
│   └── universe/_template.md
├── state/
│   └── template/             # Initial state file templates
└── scripts/
    ├── detection/            # AI-pattern detection (Python)
    └── style/                # Style compliance checker (Python)
```

## Quick Start

**1. Set up a new project:**
Tell Claude Code: `Set up a new project called [name]`

**2. Fill in your bible:**
- `bible/style.md` — your writing style, POV, tense, tone
- `bible/structure.md` — your story's structure and arc patterns
- `bible/characters/[name].md` — one file per character
- `bible/universe/[name].md` — one file per location

**3. Write your story:**
- `story/synopsis.md` — your story pitch
- `story/plan.md` — chapter-by-chapter outline
- Then: `Write chapter 1 of [project-name]`

Or copy the English starter example to see what a filled-in project looks like:
```powershell
cp -Recurse examples/english-starter projects/my-novel
```

---

## Agents

### Core Pipeline (run every chapter)

| Agent | Purpose | Model |
|-------|---------|-------|
| chapter-planner | Creates detailed chapter beats from synopsis | Opus |
| chapter-writer | Writes chapter drafts following style guide | Opus |
| style-linter | Validates compliance with bible/style.md | Sonnet |
| character-reviewer | Checks character consistency and voice | Sonnet |
| continuity-reviewer | Checks timeline and spatial logic | Sonnet |
| state-updater | Extracts and records state after each chapter | Sonnet |
| subplot-tracker | Updates open narrative thread registry | Sonnet |
| foreshadowing-tracker | Updates plants and payoffs registry | Sonnet |

### Optional / On-Demand

| Agent | Purpose | When to Use | Model |
|-------|---------|-------------|-------|
| revision-agent | Craft-level prose pass (filter words, passive, weak verbs) | Between writer and perplexity-improver | Opus |
| arc-reviewer | Narrative arc health: tension, character arcs, pacing | Every 3–5 chapters, at act transitions | Opus |
| nonfiction-reviewer | Argument structure and evidence sufficiency | For nonfiction — replaces character/continuity reviewers | Sonnet |
| world-rules-reviewer | Invented system consistency (magic, tech, physics) | Fantasy/sci-fi; when new rules are introduced | Sonnet |
| sensitivity-reader | Character portrayal and representation patterns | On demand; before sharing with external readers | Opus |
| bible-builder | Generate/fill out character and location files | When bible is sparse; when planner needs a new entry | Sonnet |
| research-assistant | Research for sci-fi plausibility, settings, nonfiction | When accuracy matters; uses web search + Wolfram Alpha | Sonnet |
| series-bible-updater | Extract series-canon facts after a book is complete | After completing a book in a series | Sonnet |

---

## Skills

| Skill | Trigger | Purpose |
|-------|---------|---------|
| book-analyzer | "Analyze [book]" | Extract style/characters/structure from source books |
| bible-merger | "Merge analysis" | Unify multiple book analyses into one bible |
| story-ideator | "Invent a story", "generate synopsis" | Create original storylines from your bible |
| perplexity-improver | After each chapter | Reduce AI-detectable writing patterns |
| synopsis-writer | End of manuscript | Query synopsis, back-cover blurb, logline, query letter |
| chapter-stats | On demand | Word count, pacing, dialogue ratio dashboard |

---

## Per-Chapter Workflow

```
plan → write → [revision pass] → perplexity-improver → style-linter
     → character-reviewer → continuity-reviewer → [world-rules-reviewer]
     → state-updater → subplot-tracker → foreshadowing-tracker → archive
```

Square brackets = optional. The orchestrator suggests arc-reviewer every 3–5 chapters.

---

## Persistent Registries

Two files grow throughout the project and are referenced when planning chapters:

- **`story/subplots.md`** — every open narrative thread, flagged when stalled
- **`story/foreshadowing.md`** — every plant and payoff, flagged when overdue

These are created automatically on the first chapter and updated after each chapter.

---

## Series Support

For books that share a world and characters across multiple volumes:

```
series/
└── my-series/
    ├── overview.md        ← What the series is
    ├── characters.md      ← Series-wide character tracker
    ├── world-rules.md     ← Permanent rules of the world
    ├── timeline.md        ← Series-wide chronological events
    └── books.md           ← Each book and what it permanently established
```

Tell the orchestrator: `Write [book-name] as part of the [series-name] series`

After completing each book, run **series-bible-updater** to record what the book permanently established.

---

## Research Assistant

Uses web search and Wolfram Alpha for four modes:
- **Sci-fi plausibility** — is this technology real/extrapolatable/handwave?
- **Setting & atmosphere** — how a place actually looks, sounds, operates
- **Historical/technical accuracy** — procedures, timelines, anachronism checks
- **Nonfiction research** — citable facts, named sources, contested claims flagged

Research briefs saved to `.work/[project]/research-[topic].md`.

---

## End-of-Project Tools

```
/synopsis-writer projects/my-novel
```
Produces: query synopsis, back-cover blurb, logline, query letter opening

```
/chapter-stats projects/my-novel
```
Produces: word count dashboard, pacing chart, dialogue ratio, outlier flags

---

## Examples

### `examples/english-starter/` — Near-Future Thriller
A complete English-language example: *The Manifest Anomaly*. Filled-in style guide, structure, character sheet, location file, synopsis, 18-chapter plan, and initial state files.

### `examples/club-des-cinq/` — French Children's Adventure
A complete 18-chapter French novel with the full pipeline: 4 analyzed source books, merged bible, 18 chapters, per-chapter state, and generated ebook.
