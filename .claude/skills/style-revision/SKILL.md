---
name: style-revision
description: Rewrite a passage in a named literary style or character voice while preserving its narrative beats. Use when asked to revise prose "in the style of" an author (Howard, Peake, Eddison) or "in the voice of" an archetype (Freeman, Paladin, Thorogood, Rogue), or to give a passage a particular tone/aesthetic. Style transformation only — never invents plot.
---

# Style Revision

Rewrite supplied prose into a named literary **style** or character **voice**
while preserving every core narrative beat. This is transformation, not
invention: do not add plot, characters, or events absent from the source.

The reference guides live in the shared craft library at the repo root:
`craft/styles/` (author styles) and `craft/voices/` (character voices). Read the
one guide that matches the request; do not batch-read them all.

## Workflow

1. Identify the requested style or voice from the user's input.
2. Load the single matching reference from `craft/styles/` or `craft/voices/`.
3. Extract the core beats from the source prose (outline them, don't rewrite yet).
4. Apply the guide's rules systematically (sentence shape, diction, imagery,
   tone, dialogue, anti-patterns).
5. Respect any length/character limit specified (default: no limit).
6. Check the result against the project's own `bible/style.md` — flag if the
   requested style would conflict with the book's established voice, so the
   author decides whether this is a one-off stylistic experiment or a shift.

## Available styles (`craft/styles/`)

| Style | Voice | Use case |
|---|---|---|
| **Howard** | Pulp heroic, elevated diction, accumulation-to-climax, physiology over interiority | Visceral action, dramatic adventure |
| **Peake** | Slow gothic camera; animates the inanimate | Dense atmospheric description, uncanny mood |
| **Eddison** | Archaic diction, inverted syntax | Elevated courtly prose, high-fantasy gravitas |

## Available voices (`craft/voices/`)

| Voice | Character | Use case |
|---|---|---|
| **Freeman** | Neurotic 1st-person stream of consciousness | Comedic, self-interested survival narration |
| **Paladin** | Devout questing knight, radiant-faith monologue | Earnest pilgrim narration, wondering diction |
| **Thorogood** | Bar-band storyteller, 2nd person, bluesy | Punchy, rhythmic retellings with attitude |
| **Rogue** | Grandiloquent confidence man, elevated diction | Formal rhetoric as weapon; every line a negotiation |

`craft/voices/voice_template.json` is a blank skeleton for defining a **new**
character voice (core personality + signature sentence patterns) when none of
the archetypes fit.

## Selection

- Style words ("gothic"/"Gormenghast" → Peake; "Conan"/"pulp"/"heroic" → Howard;
  "archaic"/"courtly"/"Mallory" → Eddison).
- Voice words ("stream of consciousness"/"neurotic" → Freeman; "questing knight"
  → Paladin; "bluesy"/"roadhouse" → Thorogood; "con man"/"grandiloquent" → Rogue).
- Ambiguous → ask the author which style/voice they mean.

## Output

- Preserve all core narrative beats from the source.
- Transformation only — no new plot elements.
- For a per-character voice the project wants to keep, hand the finished voice
  guide to **style-creator** to fold into the project's `bible/`.
