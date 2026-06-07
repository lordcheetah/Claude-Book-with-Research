# Reader State — Thinking Machines

## Chapter
1 — Learning Without Instructions (complete)

---

## Nonfiction reader state (replaces character states)

This file tracks the implied reader's knowledge and expectations across the book.
Update via state-updater after each chapter.

---

## What the reader knows
(after Chapter 1, cumulative)
- Why the book exists and what it will explain (from the Introduction)
- The central argument: understanding is available (from the Introduction)
- **The rules-vs-examples distinction**: early rule-based systems (e.g., spam filters) collapsed because a fixed list of rules can always be routed around; the alternative is showing a system labeled examples and letting it find the pattern itself — "teaching by example, not by explanation"
- **Weights/parameters as adjustable settings**: a trained system is, underneath, an enormous number of small adjustable numbers ("a million dials"), and no single one of them "means" anything on its own — the system's "opinion" lives in the pattern across all of them together
- **The training loop, by name and mechanism**: guess → measure (via a *loss function*, a number that captures how wrong the guess was) → adjust (via *gradient descent*, a blind, local, mechanical correction — "a skier in fog feeling for downhill") → repeat, at a scale that dwarfs intuition. The reader knows this is what "training" *means*
- **Three corrected misconceptions**, explicitly: (1) the system was *shown*, not *told*; (2) weights aren't exotic or magical — they're ordinary numbers, and the novelty is scale, not kind; (3) gradient descent finds *a* good-enough answer reachable from its starting point, not the single theoretically-best answer
- **The transparency-problem implication**: a system that finds its own patterns will necessarily end up holding patterns nobody — including its builders — can fully read back out in plain language. The reader has been shown *why* this is structural rather than a flaw, and why "I can't really explain how it knows" is often the most accurate sentence available, not an admission of ignorance
- **The "powerful AND hard to explain" reframe**: these aren't two separate properties that happen to co-occur — they're the same property, observed from two angles. The reader has been walked through *why* this is true, not just told that it is

## What the reader does NOT yet know
- Anything about language, tokens, or prediction as a task — that's Chapter 2's territory entirely
- How "examples" scale from two labeled piles of email to something closer to "almost everything ever written down"
- Embeddings, vector space, attention, context windows (Chapters 3–4)
- Why/how capabilities seem to "emerge" at scale (Chapter 5)
- Anything about failure modes, hallucination, or alignment (Chapters 6, 8)

## Reader's likely questions going into next chapter
- "If 'examples' aren't two piles of labeled email anymore, what *are* they — and what's the task, if it isn't sorting into categories?"
- "What, mechanically, is the system doing when it produces the next word of a sentence?" (This is the literal bridge question Chapter 1 ends on — the reader has been handed it explicitly and is owed an answer.)
- Likely latent question, not yet asked aloud by the text but primed by the dial/scale framing: "If novelty is just scale, how much scale are we actually talking about — and does that change things, or just make them bigger?" (Chapter 5 territory, but the seed is already planted.)

---

## Tone calibration
- Skepticism level assumed: **shifted from "moderate, hasn't trusted hype" (Introduction) to oriented and engaged** — Chapter 1 gave the reader a working mental model and explicitly validated a feeling many of them already had ("I can't explain how it knows" reframed as accurate, not inadequate). The tone has moved from "convince me this is worth my attention" to "I'm following — show me the next layer."
- Technical tolerance: confirmed willing to follow multi-step analogies (bird-watching → dial panel → skier in fog) when each one does specific, non-redundant work. The chapter has earned some credit here — later chapters can build on these without re-explaining, and can introduce comparably layered analogies without losing the reader.
- Emotional register: **moved from curious-but-untrusting toward grounded and ready** — the chapter deliberately defused what could have been an alarming idea (systems that can't be fully explained) by reframing it as a structural fact rather than a hidden flaw. The reader should now feel oriented rather than anxious going into Chapter 2.

---

## Notes
- Track the implied reader's knowledge state so later chapters don't re-explain or skip steps
- Flag if a chapter introduces a concept that builds on something not yet established
- Chapter 2 can safely assume fluency with: weight/parameter, training, loss function, gradient descent, and the general shape "guess → measure → adjust → repeat." It should NOT assume any familiarity with language-specific mechanics (tokens, prediction, embeddings) — those still need full introduction.
