# Current Situation

## Chapter
1 — Learning Without Instructions (complete)

## Story position
- Part: Machine learning fundamentals (Chapters 1–3)
- Chapter in arc: 1 of 3 (ML fundamentals block)
- Approximate word count written: ~2,650 (this chapter); ~2,650 cumulative

## Where we are
The book's argument has now landed its first claim: machine learning systems learn by adjusting internal settings (weights) in response to feedback on examples, not by following rules a person wrote down — and this single fact is the root of the transparency problem the book will keep returning to.

## Last chapter summary
Chapter 1 used a single throughline — the spam filter everyone has but nobody thinks about — to walk the reader from "surely someone wrote rules" through why rule-based filtering collapsed, to the alternative: showing a system labeled examples and letting it adjust itself. It built that idea up through three stacked analogies (teaching someone to recognize birds, a control panel with a million unlabeled dials, a skier descending a foggy mountain by feel) and landed on the chapter's real payload: a system trained this way ends up holding a *pattern* distributed across millions of numbers — not a rule a person could read back — and that this isn't a flaw or a corner cut, but the same fact, from the same cause, that makes these systems powerful in the first place. Powerful and hard-to-fully-explain are presented as one property seen from two angles, not two separate ones.

## Immediate problem (what the book now owes the reader)
The chapter ends by generalizing away from spam: nothing in the process described is specific to email, two categories, or short messages — the same guess/measure/adjust/repeat loop, at vastly greater scale, sits underneath systems that hold conversations, write code, and explain things. That generalization creates an open question the book must now answer directly: **what, mechanically, is a system doing, moment to moment, when it produces the next word of a sentence?** Chapter 2 exists to answer exactly that.

## Open hooks (threads later chapters must pay off)
- **The transparency problem (seeded here, due back in Chapter 7):** Chapter 1 establishes — gently, as an observation rather than an alarm — that a system which finds its own patterns will necessarily end up holding patterns nobody can fully read back out. This is framed as structural, not a bug, and not anyone's fault. Chapter 7 (interpretability limits) needs to pick this up as the same fact restated at far greater scale and stakes, not a new complaint.
- **"Powerful but imperfect optimizer" (the skier-in-fog idea):** gradient descent finds *a* good-enough answer reachable from where it started, not the single best answer that could theoretically exist anywhere on the "mountain." The chapter explicitly flags that this idea "will resurface, in different shapes, more than once before this book is done" — likely relevant to Chapter 6 (failure modes / hallucination) and possibly Chapter 8 (alignment).
- **The "novelty is scale, not kind" framing:** the million-dial analogy explicitly argues that a system with a million weights isn't doing something different in *kind* from a system with ten — only in *amount*. This sets up later chapters (4–5, especially "emergent capabilities from scale") to build directly on an idea the reader has already accepted, rather than needing to re-argue it.
- **The spam-filter throughline itself:** introduced as the concrete anchor for "pattern-finding from examples." If later chapters return to it (e.g., as a contrast case against next-token prediction in Ch.2, or as a callback when discussing simpler vs. more complex learned systems), it will land as a familiar friend rather than a new example.

## Orchestrator notes
Chapter 1 cleared style-linter (PASS) and nonfiction-reviewer (PASS, 0 blocking issues). Proceed to Chapter 2 planning. Load:
- bible/style.md
- bible/structure.md
- story/synopsis.md
- story/plan.md (Chapter 2 section)
- state/current/* (this state)

Chapter 2's opening should pick up directly from the bridge question Chapter 1 ends on — the reader has been told the loop (guess, measure, adjust, repeat) and the scale claim, and is now owed the mechanics of *what* is being predicted and *how* "next word" cashes out concretely (tokens, prediction-as-the-task).
