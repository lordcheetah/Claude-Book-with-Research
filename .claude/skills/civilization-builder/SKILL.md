---
name: civilization-builder
description: >-
  Build a civilization from first principles using the derivation chain —
  planet → biology → cognition → culture → technology → language → science →
  history — with each layer derived from the one below it and an author
  checkpoint between layers. Works for any species: human civilizations in
  novel environments derive different structures too. Use when worldbuilding a
  culture/species/society in depth for a project's bible/universe. Triggers on
  "build a civilization", "design this culture/species from scratch",
  "derive this society", "worldbuild this people in depth".
---

# Civilization Builder — Derivation-Chain Pipeline

A deep-worldbuilding pipeline for designing a civilization (alien or human-in-a-
novel-environment) where every feature traces back to a physical cause. This is
the in-depth companion to **bible-builder** (which fills gaps/stubs) and
**world-rules-reviewer** (which checks consistency). Follow the chain exactly —
do not skip layers or reorder. Every layer derives from the one below it.

Human civilizations on different worlds derive different institutions — the Nile
floodplain produced different structures than the Mongol steppe, and both are
human. A novel environment produces a novel civilization even with familiar
biology.

## The derivation chain

```
Planet → Biology → Cognition → Culture → Technology → Language → Science → History
```

Each step must be complete and **author-approved** before the next. No forward
references. The orchestrator runs this; bible canon is only written by
**bible-builder** after the author approves a layer.

## Step 0: Prerequisites

1. Read `{PROJECT_ROOT}/CLAUDE.md`-injected context, `{PROJECT_ROOT}/bible/style.md`,
   and any existing `{PROJECT_ROOT}/bible/universe/*` for established canon to obey
   and to differentiate against.
2. If the project has world rules (magic/physics/tech laws), the civilization's
   biology and technology must obey them.
3. Decide species type: known biology (e.g. human) or a novel species.
4. Write the build plan to `.work/{project-name}/civilization-build-[name].md`.

## Step 1: Planet

Build the physical environment first — the planet determines everything.
Consult `craft/references/designing-worlds.md` for the biome/planetary-mechanics
method. Derive: star/orbit/rotation, tidal-lock status, atmosphere, geology and
hydrology, energy sources, biome architecture, and any world-rule field/force
saturation. **Checkpoint 1:** author approves the planet before biology.

## Step 2: Biology

For a **novel species**, derive biology from planetary conditions (what survives
here, not what's cool). For a **known species**, document how this planet's
gravity, atmosphere, radiation, food, and day/night cycle reshape physiology.
Derive energy metabolism, sensory emphasis, locomotion, reproduction pressures,
lifespan/development. **The test:** can every feature trace back to a planetary
condition? If not, it's an assumption. Use `craft/references/interrogating-design.md`
to pressure-test risky choices. **Checkpoint 2.**

## Step 3: Cognition

Derive cognition from biology. What sensory data dominates experience here? What
cognitive capabilities does the environment reward? What biases does it produce?
What concepts are easy/hard to form? For novel species, additionally: native
information-processing architecture, which human cognitive assumptions this
species does NOT share, what consciousness is like for this biology.
**Checkpoint 3.**

## Step 4: Culture

Use the **deriving-social-systems** skill to derive coordination structures from
cognition + biology + environment. Do NOT start from a checklist of institutions
— inventory constraints, derive structures, name them functionally, and run the
**negative derivation** (what familiar structures do NOT emerge, and why).
Familiar institutions may emerge for human civilizations, but only from the
derivation, not from assumption.

**Then run the world-assumptions-reviewer agent on the culture material before
proceeding** — it flags anthropomorphism and cultural parochialism imported
uncritically into a novel context (applies to human civilizations too).
**Checkpoint 4.**

## Step 4.5: Cultural Layer

Derive the felt, interior culture from the same constraint chain (Step 4 derives
coordination structures; 4.5 derives what they feel like from the inside). Do
NOT import human cultural categories and fill them — ask what each constraint
produces. Six required categories:

1. **Aesthetic tradition** — what is beauty for this species, derived from its
   primary sensory modality and local environment?
2. **Performance / communal experience** — what shared experiences does the
   biology and communication modality enable (not assumed music/theater)?
3. **Meaning-making and mystery** — what epistemological gaps exist, and what
   practices form around them? Religion only if its preconditions are met;
   otherwise what fills the same functional space?
4. **Memory and the dead** — what persists after biological death (substrate
   residue, chemical trace, nothing), and what practices form around it?
5. **Pre-sapient / pre-bonding childhood** — what is existence like before full
   cognition, and what practices form around that period?
6. **Novel cultural forms** — did the derivation produce practices with NO
   familiar analogue? These are the highest-value output. Give them full treatment.

**Checkpoint 4.5.**

## Step 5: Technology

Derive technology from culture + biology + environment. What does this species
need that biology doesn't provide? What materials does the planet offer? What
manipulative capability does biology give? What does cognition make easy to
engineer — and what would they never think to build? (A planet without iron
produces no steel; abundant geothermal energy skips combustion.) **Checkpoint 5.**

## Step 6: Language

Derive language from communication biology + cognition + culture. Physical
medium and (for humans) environment-shaped phonology; grammar's deep structure;
which concepts are lexicalized vs. circumlocuted; what is untranslatable to/from
other languages in the world. **Checkpoint 6.**

## Step 7: Science

Derive the species' scientific understanding from cognition + technology +
accumulated observation. What does their sensory apparatus and technology reveal?
What do they understand well, and what are they blind to? Where does their
science converge with or diverge from others'? For real-world grounding, the
**research-assistant** can source the actual science. **Checkpoint 7.**

## Step 8: History

Derive history from everything above — what actually happened to this species in
this environment. Key biology/environment-driven transitions, how coordination
structures evolved, internal conflicts arising from tensions in the derived
social systems, contact events, current state and trajectory. **Final checkpoint.**

## Step 9: Audit

1. Run the **world-assumptions-reviewer** agent on all civilization material.
2. Run **world-rules-reviewer** for internal-system consistency.
3. Run **continuity-reviewer** for cross-reference / naming consistency against
   existing bible canon.

## Rules

- **Never skip a checkpoint.** Each layer builds on the one below.
- **Derive, don't assume.** Even familiar-looking institutions must emerge from
  the chain, not a template.
- **Flag the gaps.** If a derivation needs a decision the author hasn't made,
  stop and ask — do not fill gaps with assumptions.
- **Cross-civilization differences are features, not bugs.** Two civilizations
  can have incompatible social structures; that means the derivation is working.
- **Novel structures are expected** — name them functionally and describe the
  mechanism.

## After completion

Hand the approved layers to **bible-builder** to write into
`{PROJECT_ROOT}/bible/universe/` (one entity per file). Significant historical
events go into `{PROJECT_ROOT}/timeline/history.md`. Do not write bible canon
directly from this skill — surface it and let bible-builder fold it in.
