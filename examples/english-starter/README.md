# English Starter Example — "The Manifest Anomaly"

A near-future thriller showing how to use this framework for English-language fiction.

## What this example shows

- `bible/style.md` — Filled-in style guide for a third-person, past-tense thriller
- `bible/structure.md` — 18-chapter arc with act structure and scene patterns
- `bible/characters/maya-chen.md` — Complete character sheet for the protagonist
- `bible/universe/station-alpha.md` — Setting file with atmosphere and hidden elements
- `story/synopsis.md` — Full story pitch with logline, conflict, and themes
- `story/plan.md` — Chapter-by-chapter outline with beats and hooks
- `state/template/` — Pre-filled initial state files

## To use this as a starting point

```
cp -r examples/english-starter projects/my-novel
```

Then customize the bible, synopsis, and plan for your story — or start fresh using the
templates in `bible/` and `state/template/` as blank scaffolding.

## To write this story

```
Write chapter 1 of english-starter
```

The orchestrator will find the project, load the state, and invoke the chapter pipeline.
