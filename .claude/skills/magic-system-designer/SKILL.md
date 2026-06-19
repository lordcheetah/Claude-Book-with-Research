---
name: magic-system-designer
description: >-
  Design a fantasy magic system with clear rules, costs, and limits using
  Sanderson's Three Laws and the hard/soft framework. Use when building or
  auditing the magic for a fantasy project. Triggers on "design a magic system",
  "how should the magic work", "make the magic consistent", "hard/soft magic",
  "what are the rules/costs of this magic". Produces the design; bible-builder
  writes it into the bible.
---

# Magic System Designer

Design (or stress-test) a fantasy magic system so it creates drama instead of
solving problems for free. Read `craft/references/magic-systems.md` first — it
holds Sanderson's Three Laws, the hard/soft framework, the design template, and
the pitfalls this skill applies.

## Workflow

1. **Decide the system's job.** Will the magic *solve plot problems* (then it
   needs to be **hard** — explicit rules the reader understands, per Sanderson's
   First Law) or *create wonder/atmosphere* (then it can stay **soft**)? Most
   strong systems are hard where the protagonist wins with it and soft where it
   sets mood and scale. State this split explicitly.

2. **For the hard portion, specify all four + the boundary:**
   - **Energy source** — where it comes from; finite or infinite; exhaustible?
   - **Rules of use** — who can use it, how it's acquired, conditions required,
     constraints.
   - **Cost / consequence** — cost per use, overuse effects, long-term effects.
   - **Possible vs. impossible** — what it can do, what it explicitly cannot,
     and where the boundary sits.

3. **Apply Sanderson's Second Law** — make the *limitations* carry the interest.
   For each power, name the constraint that turns it into a source of conflict
   and strategy. A power with no cost is a flag to fix.

4. **Apply the Third Law** — before adding a new power, ask whether deepening or
   recombining an existing one would be stronger. Prefer interconnected rules
   over a pile of separate abilities.

5. **Run the pitfall pass** (from the reference): is anything plot-convenient or
   inconsistent? Is an exception foreshadowed? Does the magic let characters
   solve problems *creatively within the limits* rather than by escalation?

6. **Tie magic to the world.** How does this magic reshape the society's
   geography, economy, politics, and class structure? (Magic that exists changes
   how a civilization develops — don't bolt it onto a default setting.) For deep
   society derivation, hand off to the `civilization-builder` skill /
   `deriving-social-systems`.

## Consistency check (for an existing system)

Given a draft or existing bible, verify: rules established early; no
plot-convenient bending; costs always paid; the four elements all specified;
the boundary of the possible is clear and respected across chapters. Report
violations with chapter/line. (This complements **world-rules-reviewer**, which
checks system consistency across the whole manuscript.)

## Output

Write the design to `.work/{project-name}/magic-system-[name].md` (project-name
derived from PROJECT_ROOT). When the author approves it as canon, hand it to
**bible-builder** to fold into `{PROJECT_ROOT}/bible/universe/` — do not write
bible canon directly.
