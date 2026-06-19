# Craft Reference Library

Shared, cross-project craft knowledge. These files are **read-only reference**
for the writer, critic, revision-agent, persona critics, and the style-revision
skill. They are not per-project — they apply to every book under `projects/`.

The orchestrator (`CLAUDE.md`) injects the relevant files into an agent's
context when they're useful for the task at hand. Agents may also read them
directly.

## Layout

```
craft/
├── references/        Genre-agnostic craft references (consult, don't rewrite)
├── style-guides/      Copy-edit standards: Chicago (US) vs New Oxford (UK)
├── styles/            Named author prose styles for stylistic revision
├── voices/            Character voice archetypes + a blank voice template
└── data/              Reusable abstracted templates and craft-axis vocab
```

## references/

| File | What it gives you |
|---|---|
| `prose-smells.md` | **Highest-value.** Catalogue of structural LLM prose tics (paradoxical pairing, exhaustive triad, negative definition, default atmosphere words…) with numeric frequency thresholds and concrete fixes. Pair with the `perplexity-improver` skill and the `critic`. |
| `audiobook-considerations.md` | Writing for the ear: similar-name pairs, homophones, pronoun ambiguity, read-aloud numbers, pronounceable invented names. |
| `anti-patterns.md` | Problem/Why/Fix tables across openings, character, plot, dialogue, prose, POV, pacing. |
| `prose-style.md` | Show/tell spectrum, sentence rhythm, verb hierarchy, POV integrity, multi-POV management. |
| `dialogue.md` | Subtext and evasion patterns, said-rule, action beats. |
| `scene-structure.md` | Scene/Sequel, Motivation-Reaction Units with reaction ordering. |
| `story-structure.md` | Side-by-side Three-Act / Save the Cat / Seven-Point / Fichtean / Snowflake, with a "which to choose" table. |
| `character.md` | Want/Need/Lie/Ghost/Flaw, arc types, deep-POV checklist, voice-differentiation test. |
| `pacing.md`, `openings.md`, `endings.md`, `revision-editing.md`, `genre-conventions.md`, `length-forms.md`, `craft-wisdom.md` | Standard craft checklists and process wisdom. |

### references/ (worldbuilding)

| File | What it gives you |
|---|---|
| `worldbuilding-rigor.md` | **Dual-use rigor toolkit** for keeping invented systems consistent (hard SF/fantasy) *and* nonfiction arguments honestly grounded: operating principles (mechanism-over-association, Pearl's ladder, predictive power), six metascience triage filters, and adversarial protocols (red-team ladder, Russell Conjugation strip, CADS quadrants). Wired into `world-rules-reviewer` and `nonfiction-reviewer`. |
| `magic-systems.md` | Fantasy magic design: Sanderson's Three Laws, hard/soft framework, the source/rules/cost/limits template, genre pitfalls, reveal timing, checklist. Used by the `magic-system-designer` skill. |
| `designing-worlds.md` | Physical-substrate method: biomes, planetary mechanics, weather-as-narrative, one productive contradiction per biome. Used by `civilization-builder` Step 1. |
| `designing-lore.md` | Deep-memory layer: myth, legendary figures, historical eras, relics — macro scale (complements the single-object `folklore-generator`). |
| `interrogating-design.md` | Single-decision pressure test: OODA loop, red-team escalation, Russell Conjugation check. Used by `civilization-builder` and `magic-system-designer`. |

## style-guides/

`decision-matrix.md` is the practical one: a side-by-side of where Chicago
(American) and New Oxford (British) diverge — punctuation, spelling, dates,
capitalization. Pick one per project and keep it consistent. `shared-rules.md`
is the CMOS∩NOSM intersection.

## styles/

Named prose-style guides for the `style-revision` skill — rewrite a passage in
a public-domain author's register while preserving the beats:
- `howard-style.md` — pulp, accumulation-to-climax, physiology over interiority
- `peake-style.md` — slow gothic camera, animating the inanimate
- `eddison-style.md` — archaic, inverted syntax

## voices/

Character-voice archetypes for the `style-revision` skill (voice mode), plus
`voice_template.json` (a blank voice-guide skeleton):
- `freeman-voice.md` — neurotic first-person stream of consciousness
- `paladin-voice.md` — devout questing knight
- `thorogood-voice.md` — second-person bluesy bar-band
- `rogue-voice.md` — grandiloquent con-man

## data/

- `paragraph-templates.json` — abstracted paragraph blueprints (word-count,
  tension-arc, structure, rhetorical-dna, respecification-seed). Genre-agnostic.
- `character-actions.json` — abstracted generic character-action sentences.
- `craft-axes-vocabulary.json` — the craft-axis taxonomy used by scene framing:
  senses, rhythms, POV distances, scene shapes, registers, sentence-length caps,
  signature constructions, plus **ban lists** (simile / cadence / syntactic /
  imagery / register). The single most reusable craft data file.
- `genre-dark-fantasy/` — optional Robert-E-Howard-flavored name / scene-tag /
  vocabulary banks. Genre flavor only; use for dark-fantasy projects or ignore.

## Attribution

- `references/` and `style-guides/` adapted from **howells/fiction** (Daniel
  Howells, MIT).
- `styles/`, `voices/`, and `data/` adapted from **Claude-Fiction-Kit**
  (sandervw). The dark-fantasy banks read as Howard/Conan pastiche, not from any
  specific project's canon.
- `worldbuilding-rigor.md`, `designing-worlds.md`, `designing-lore.md`,
  `interrogating-design.md` adapted from **worldcodex** (alainator, MIT) — its
  epistemological framework, design skills, and `/civilization-build` pipeline.
  The `civilization-builder` and `deriving-social-systems` skills and the
  `world-assumptions-reviewer` agent also derive from it.
- `magic-systems.md` adapted and translated from a Chinese-language
  fantasy-world-building skill (wordflowlab, via microck/ordinary-claude-skills).
