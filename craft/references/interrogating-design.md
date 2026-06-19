# Interrogating Design — Single-Decision Pressure Test

A method for stress-testing one worldbuilding decision, rule, or premise until
its implications, contradictions, and dependencies are resolved. Use when
validating a proposed rule or premise, or when the author says "stress test
this", "what are the implications", "does this break anything", or "red team
this". Interrogation only — produces no canon (hand approved results to
**bible-builder**).

## Method

Interview the author one question at a time, walking down each branch of the
decision tree and resolving dependencies in order. For every question, offer
your recommended answer. If a question can be answered from existing files,
explore them instead of asking.

**OODA loop (Boyd):**
- **Observe** — read the relevant files; grep for related terms.
- **Orient** — synthesize against the established rules; *destroy outdated mental
  models* when new data contradicts them (don't defend the old reading — update).
- **Decide** — formulate a specific hypothesis about the implication or conflict.
- **Act** — test it against the manuscript/bible, don't just assert it.

**Dependency-order walkthrough** — check implications layer by layer (customize
per project): core premise/definitions → physical/world rules → biology/economy/
established systems → existing canon and narrative.

**Red-team escalation** — 1) contradicts an explicit rule? 2) contradicts an
implicit downstream constraint? 3) survives application across every case it
should govern? 4) would a hostile reader find it inconsistent? 5) strip the
narrative beauty — is the bare mechanism still valid?

**Russell Conjugation check** — restate the proposal in the most boring, clinical
language possible. If it only works in emotive framing, it's aesthetic, not
sound. (Full rigor toolkit: `worldbuilding-rigor.md`.)

## After validation

Self-review for placeholders, contradictions, and ambiguity; present the result
in digestible sections; save the decision record to
`.work/{project-name}/design-decision-[topic].md`; hand approved canon to
**bible-builder**.
