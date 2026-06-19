---
name: writing-artifacts
description: >
  Where writing artifacts live in this project: bible/ (read-only canon), state/, story/, and timeline/ under PROJECT_ROOT, plus .work/ for scratch. Use when deciding where to read from or write to.
---

# Writing Artifacts

This project is a multi-project novel orchestrator. All story paths are relative
to **PROJECT_ROOT** (`projects/[name]` or `examples/[name]`), set by the
orchestrator. Read the root `CLAUDE.md` for the full workflow; read
`{PROJECT_ROOT}/bible/style.md` for this story's voice.

## Read-only canon (never write here during drafting)

```text
{PROJECT_ROOT}/bible/
  style.md               # voice, tense, POV, register — the style reference
  structure.md           # chapter/act structure
  tropes.md              # genre-native tropes, clichés to avoid, in-use tracker
  characters/*.md        # character profiles
  universe/*.md          # locations, factions, world details
```

A series project also has a read-only `{SERIES_ROOT}/` constraint layer.

## Story working files

```text
{PROJECT_ROOT}/story/
  synopsis.md            # query synopsis
  plan.md                # chapter plan
  subplots.md            # subplot registry (subplot-tracker)
  foreshadowing.md       # plant/payoff registry (foreshadowing-tracker)
  chapters/*             # final chapters (destination)
```

## Current + archived state

```text
{PROJECT_ROOT}/state/current/*        # current chapter state (situation, characters)
{PROJECT_ROOT}/state/chapter-NN/*     # archived per-chapter state
{PROJECT_ROOT}/timeline/history.md    # all past chapters (append-only)
{PROJECT_ROOT}/timeline/current-chapter.md
```

## Scratch

Draft iterations, critique reports, and brainstorm captures that are not yet
final live under `.work/` at the repo root. Promote *knowledge* (not raw
artifacts) into `state/`, `story/`, or a bible entry when a drafting effort
completes. Bible entries are filled only by **bible-builder** — never invent
canon directly.

## Shared, durable craft references

Cross-project craft knowledge lives in `craft/` at the repo root
(prose-smells, style guides, named author styles, structure/scene/dialogue
references). Read from it; do not rewrite it per chapter.

## Shared Workspace

The working tree is shared between the author and all agents. Any file may have
been edited by someone else since you last saw it. Read the current state
before acting on it; treat what's on disk as the authority, not your memory of
what was there. When your edits would conflict with changes someone else made,
surface the conflict rather than silently overwriting. The author's direct
edits are always authoritative.
