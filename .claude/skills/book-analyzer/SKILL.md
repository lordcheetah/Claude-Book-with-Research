---
name: book-analyzer
description: Analyze source books to extract structured bible files (style, characters, structure, universe). Use when analyzing novels, stories, or any narrative text to create a reusable writing bible for style matching and story generation.
---

# Book Analyzer

Extract structured bible files from source books for the writing framework.

## Quick Start

```bash
# Analyze a single book (PROJECT_ROOT provided by orchestrator)
Analyze {PROJECT_ROOT}/analysis/src/[book].txt
```

Output structure in `{PROJECT_ROOT}/analysis/output/[book-slug]/`:
```
├── style.md
├── structure.md
├── characters/
│   └── [character].md
└── universe/
    └── [location].md
```

## Workflow

### 1. Read source completely
Load the full text, note overall structure and length.

### 2. Extract style
- Identify POV (first/third limited/omniscient)
- Identify tenses (primary, secondary)
- Sample 50 sentences for average length
- List 20-30 characteristic vocabulary items
- List dialogue tags used
- Estimate dialogue-to-prose ratio
- Note description techniques

### 3. Extract characters
For each significant character:
- Identity (name, age, role)
- Physical description
- 3-5 core personality traits with evidence
- 5-10 dialogue quotes showing voice
- Relationships mapped

### 4. Extract structure
- Map acts (setup/development/climax/resolution)
- Note chapter count and length range
- Analyze chapter openings and endings
- Identify recurring patterns
- Track mystery mechanics if applicable

### 5. Extract universe
For each significant location:
- Physical description with quotes
- Atmosphere and sensory details
- Story function

### 6. Generate files
Create all output files following templates in `bible/`.

## Evidence-Based Extraction

Every trait, pattern, or rule must be supported by:
- Direct quotes (with chapter reference)
- Quantitative data (averages, counts, percentages)

Bad: "Claude is stubborn"
Good: "Claude is stubborn (Ch.2: refuses to answer to 'Claudine'; Ch.5: insists on leading despite danger)"

## Output Format

Follow templates exactly:
- `bible/style.md` → `output/[book]/style.md`
- `bible/characters/_template.md` → `output/[book]/characters/[name].md`
- `bible/universe/_template.md` → `output/[book]/universe/[name].md`
- `bible/structure.md` → `output/[book]/structure.md`

For detailed extraction checklists, see [references/extraction-guide.md](references/extraction-guide.md).

## Output Language
Match the source book's language for extracted content and quotes.
Use English for metadata, structural annotations, and field labels.
