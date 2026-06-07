# Argument History — Thinking Machines

Events from completed chapters are appended here by the state-updater at the end of each chapter transition.

For nonfiction: "events" = claims established, analogies deployed, vocabulary introduced.

---

## Chapter 1 - Learning Without Instructions
- [Established: rules-vs-examples distinction, via spam-filter throughline — early rule-based filters collapsed because fixed lists can always be routed around; the alternative is showing a system labeled examples and letting it find the pattern itself]
- [Established: weights/parameters as adjustable settings — "a control panel with a million dials" analogy, doing double duty: makes the concept concrete AND dismantles the "weights are exotic/magical" misconception (novelty is scale, not kind)]
- [Established: the training loop — guess, measure (loss function), adjust (gradient descent), repeat — "a skier descending a mountain in fog" analogy, explicitly flagged in-text to resurface in later chapters]
- [Corrected: three misconceptions — (1) the system was shown, not told; (2) weights aren't magical, they're ordinary numbers at extraordinary scale; (3) gradient descent finds a good-enough locally-reachable answer, not the single theoretically-best one]
- [Planted: the transparency problem is structural, not a flaw or oversight — a system that finds its own patterns will necessarily hold patterns nobody can fully read back out; "powerful" and "hard to explain" reframed as one property seen from two angles — seed for Chapter 7]
- [Planted: "powerful but imperfect optimizer" thread (skier-in-fog) — explicitly marked in the chapter's own text as something that "will resurface, in different shapes, more than once before this book is done" — likely payoff in Chapter 6 (failure modes/hallucination) and possibly Chapter 8 (alignment)]
- [Bridged to: Chapter 2's question — nothing in the spam-filter story is specific to email or two categories; the same guess/measure/adjust loop, at far greater scale, underlies systems that converse, code, and explain. So: what, mechanically, is a system doing, moment to moment, when it produces the next word of a sentence?]
