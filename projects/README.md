# Projects

Each subdirectory here is a separate book project.

## Starting a New Project

Create a folder for your project:

```
projects/
└── my-novel/
    ├── bible/
    │   ├── style.md          ← Copy from ../../bible/style.md.example and fill in
    │   ├── structure.md      ← Copy from ../../bible/structure.md.example and fill in
    │   ├── characters/
    │   │   └── hero.md       ← Copy from ../../bible/characters/_template.md per character
    │   └── universe/
    │       └── city.md       ← Copy from ../../bible/universe/_template.md per location
    ├── story/
    │   ├── synopsis.md       ← Your story pitch
    │   └── plan.md           ← Chapter-by-chapter outline
    ├── state/
    │   └── template/         ← Copy from ../../state/template/ and fill in
    │       ├── situation.md
    │       ├── characters.md
    │       ├── knowledge.md
    │       └── inventory.md
    ├── timeline/
    │   ├── history.md        ← Start empty
    │   └── current-chapter.md ← Start empty
    └── analysis/             ← Optional: source book analyses
        └── src/              ← Place source books here (txt/md)
```

## Quick Setup

Tell Claude Code: **"Set up a new project called [name]"** — it will create the scaffolding.

Or copy from the English starter example:

```
cp -r examples/english-starter projects/my-novel
```

## Working on a Project

Tell Claude Code which project to write: **"Write chapter 1 of [project-name]"** or just
**"Write chapter 1"** if only one project exists.

## See Also

- `examples/english-starter/` — English example with filled-in templates
- `examples/club-des-cinq/` — Complete French novel (18 chapters, full analysis pipeline)
- `bible/style.md.example` — Style guide template
- `bible/structure.md.example` — Structure template
