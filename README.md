# Claude Book Framework

A multi-agent framework for writing novels with Claude Code. Supports multiple simultaneous book projects, English and non-English output, and research-assisted writing for any genre.

## Repository Structure

```
├── CLAUDE.md                 # Orchestrator — coordinates all agents
├── .claude/
│   ├── agents/               # Specialized sub-agents
│   └── skills/               # Reusable skills
├── projects/                 # YOUR book projects (one subdirectory per book)
│   └── my-novel/             # Example: your project lives here
│       ├── bible/            # Style guide, characters, locations
│       ├── story/            # Synopsis, chapter plan, chapters
│       ├── state/            # Per-chapter narrative state
│       ├── timeline/         # Event history
│       └── analysis/         # Optional: source book analyses
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
├── scripts/
│   ├── detection/            # AI-pattern detection (Python)
│   └── style/                # Style compliance checker (Python)
└── .work/                    # Temporary agent work files (gitignored)
```

## Quick Start

### Option A: Start from scratch

1. Tell Claude Code: **"Set up a new project called [name]"**
2. Fill in your `bible/style.md`, `bible/structure.md`, character and location files
3. Write `story/synopsis.md` and `story/plan.md`
4. Run: **"Write chapter 1 of [name]"**

### Option B: Copy the English starter

```powershell
cp -Recurse examples/english-starter projects/my-novel
```

Edit the files to match your story, then: **"Write chapter 1 of my-novel"**

### Option C: Analyze existing books for style matching

1. Place source books in `projects/[name]/analysis/src/` (txt or md format)
2. Run: **"Analyze projects/[name]/analysis/src/[book].txt"**
3. Review generated bible in `projects/[name]/analysis/output/[book]/`
4. For multiple books: **"Merge projects/[name]/analysis/output/* into projects/[name]/bible/"**

## Agents

| Agent | Purpose | Model |
|-------|---------|-------|
| chapter-planner | Creates detailed chapter beats from synopsis | Opus |
| chapter-writer | Writes chapter drafts following style guide | Opus |
| style-linter | Validates compliance with bible/style.md | Sonnet |
| character-reviewer | Checks character consistency and voice | Sonnet |
| continuity-reviewer | Checks timeline and spatial logic | Sonnet |
| state-updater | Extracts state changes after validation | Sonnet |
| **research-assistant** | **Researches topics for sci-fi/nonfiction** | **Sonnet** |
| **bible-builder** | **Generates/fills out characters and locations** | **Sonnet** |

## Skills

| Skill | Trigger | Purpose |
|-------|---------|---------|
| book-analyzer | "Analyze [book]" | Extract style/characters/structure from source books |
| bible-merger | "Merge analysis" | Unify multiple analyses into one bible |
| story-ideator | "Invent a story", "generate synopsis" | Create original storylines from your bible |
| perplexity-improver | After each chapter | Reduce AI-detectable writing patterns |

## Research Assistant

The research-assistant agent supports both fiction and nonfiction writing with four modes:

- **Sci-fi plausibility**: "Research cryosleep science for chapter 4" — evaluates fictional tech against current knowledge, flags where handwaving is required
- **Setting & atmosphere**: "Research what offshore platforms actually feel like" — sensory detail, jargon, realistic procedures
- **Historical/technical accuracy**: "Check my 1940s timeline for anachronisms"
- **Nonfiction research**: "Research sleep deprivation for my chapter on cognitive performance" — citable facts, named sources, contested claims flagged

Research briefs are saved to `.work/[project-name]/research-[topic].md`.

## Multi-Project Support

Each subdirectory of `projects/` is an independent book project. The orchestrator:
1. Detects which project you're referring to from context
2. Asks you to choose if multiple projects exist and none is named
3. Routes all agent calls to the correct project's files

**To work on a specific project**: "Write chapter 3 of my-sci-fi-novel"  
**With only one project**: "Write chapter 3" works without naming it

## Output Language

The orchestrator and all agents default to **English**. To write in another language, specify it in your project's `bible/style.md`. The writer and planner agents will match the language configured there.

Technical reports (style-linter, character-reviewer, continuity-reviewer) are always in English regardless of story language.

## Workflow (per chapter)

1. **Plan**: chapter-planner creates detailed beats
2. **Write**: chapter-writer drafts the chapter
3. **Improve**: perplexity-improver reduces AI-detectable patterns
4. **Lint**: style-linter validates against style guide
5. **Review**: character-reviewer and continuity-reviewer check consistency
6. **Loop**: writer revises if gates fail (max 3 iterations)
7. **Archive**: state-updater saves state; chapter moves to `story/chapters/`

## Ebook Export

For the Club des Cinq example, see `examples/club-des-cinq/ebook/`. Adapt the pipeline for your project:

```powershell
cd examples/club-des-cinq/ebook
.\build-ebook.ps1              # EPUB (default)
.\build-ebook.ps1 -Format all  # All formats
```

**Prerequisites**: Pandoc, powershell-yaml module, Calibre (for MOBI/AZW3)

## Perplexity Improver

Reduces AI-detectable patterns in chapters using a local language model.

**Prerequisites**: NVIDIA GPU (~16 GB VRAM), `uv` package manager

```
/perplexity-improver projects/my-novel/story/chapters/chapter-05.md
```

See `.claude/skills/perplexity-improver/SKILL.md` for full documentation.

## Examples

### `examples/english-starter/` — Near-Future Thriller
Complete English-language example: a data analyst on an isolated offshore station uncovers a corporate cover-up. Includes filled-in style guide, structure, character sheet, location file, synopsis, chapter plan, and initial state files. Use as a template or read to understand how the framework's files fit together.

### `examples/club-des-cinq/` — French Children's Adventure
A complete 18-chapter novel written using this framework, based on Enid Blyton's Famous Five style. Includes the full pipeline: 4 analyzed source books, merged bible, 18 completed chapters, per-chapter state files, and generated ebook. Demonstrates the full end-to-end workflow.
