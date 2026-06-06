# Series Bibles

Each subdirectory here is a series — a collection of related books that share characters, world, and accumulated history.

## When to Use a Series Bible

If you're writing a standalone book, you don't need this. Use a series bible when:
- Multiple books share the same characters and world
- Facts established in Book 1 constrain what can happen in Book 2
- Characters age, change, or develop across volumes
- The world has a history that accumulates

## Structure

```
series/
└── [series-name]/
    ├── overview.md          ← What the series is, its tone and scope
    ├── characters.md        ← Series-wide character tracker (what's established across all books)
    ├── world-rules.md       ← Rules of the world that never change
    ├── timeline.md          ← Series-wide chronological events
    └── books.md             ← Each completed book and what it permanently established
```

## How It Relates to Per-Book Projects

Each book project in `projects/[book-name]/` has its own `bible/` for book-specific details.
The series bible holds what's **permanent across all books** — facts that can't be contradicted.

When writing a new book in the series, tell the orchestrator:
**"Write [book-name] as part of the [series-name] series"**

The orchestrator will load both the project bible and the series bible, treating the series bible as a read-only constraint layer.

## Creating a New Series

Tell Claude Code: **"Set up a new series called [name]"** — it will create the scaffolding.
Or copy the template:

```
series/
└── [series-name]/
    ├── overview.md
    ├── characters.md
    ├── world-rules.md
    ├── timeline.md
    └── books.md
```

## Updating the Series Bible

After completing a book, run **series-bible-updater** to extract what the new book permanently established and add it to the series record. The series bible grows after every book; it is never rewritten.
