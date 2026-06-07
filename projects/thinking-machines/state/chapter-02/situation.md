# Current Situation

## Chapter
2 — Reading as Prediction (complete)

## Story position
- Part: Machine learning fundamentals (Chapters 1–3)
- Chapter in arc: 2 of 3 (ML fundamentals block)
- Approximate word count written: ~3,389 (this chapter); ~6,038 cumulative

## Where we are
The book has now landed its second major claim, in direct answer to the question Chapter 1 closed on: a language model, mechanically, is doing the same basic thing as phone autocomplete — guessing the next piece based on what came before — except that the "pieces" are tokens (not words), and the task has been scaled across almost everything humans have ever written down. The chapter then made the harder turn: showing why a system trained on nothing but "guess the next piece" produces output that *looks* like understanding, naming the field's most contested live debate fairly (without resolving it), and identifying the structural gap between "sounds true" and "is true" as a necessary consequence — not a flaw — of the training objective.

## Last chapter summary
Chapter 2 opened on phone autocomplete (an experience every reader has had) and answered Chapter 1's literal bridge question within the first few hundred words: a system produces the next word the same way a keyboard does, just at a vastly larger scale (the crayon-drawing-vs-satellite-photo analogy). It then complicated that answer immediately — the system predicts *tokens*, not words — using a LEGO-kit analogy to explain tokenization, and rode that analogy directly into correcting the "strawberry" letter-counting misconception that circulates online. It named next-token prediction as the entire training objective with full, unhedged confidence (correctly identified by the research brief as settled ground), scaled the picture up ("training on almost everything," recalling the million-dial control panel from Ch.1), then walked through the "Paris is the capital of France" example slowly and concretely to dismantle the "the system looks things up" misconception — replacing it with the actual mechanism (statistical pattern density, not retrieval). From there it asked the chapter's center-of-gravity question — why does pure prediction produce something that looks like knowing? — and named the "stochastic parrots" debate fairly, by name (Bender/Mitchell vs. an unnamed but seriously-argued opposing position), explicitly refusing to resolve it: "the result *looks like* knowing... nobody currently knows." It closed by identifying the structural sounds-true/is-true gap (the seed for Chapter 6's hallucination discussion) and bridged cleanly to Chapter 3: if prediction is the *task*, what is the system actually *holding*, internally, that makes its predictions this good?

## Immediate problem (what the book now owes the reader)
The chapter ends by deliberately naming what it has NOT explained: a pile of correctly-predicted tokens isn't, by itself, meaning. Producing "Paris" in the right place isn't the same as the concept of Paris meaning anything to anything. That creates the open question Chapter 3 exists to answer: **not what the system is doing (now fully known, mechanically) — but what it must be *holding* internally in order to do it.** This is the chapter's explicit, named handoff — Chapter 3 should open by picking it up directly, the same way Chapter 2 opened by picking up Chapter 1's question directly.

## Open hooks (threads later chapters must pay off)
- **The sounds-true/is-true structural gap (seeded here, due back in Chapter 6):** established as a *necessary, structural* consequence of training a system to do nothing but predict plausible continuations — not a bug, not a sign of half-finished engineering. Chapter 6 (hallucination) needs to pick this up as the same fact restated at higher stakes, in the same even register Chapter 1 used for the transparency problem (which this explicitly parallels and cross-references).
- **The stochastic-parrots vs. emergent-understanding debate (named fairly, deliberately left open):** two serious camps were named — the "stochastic parrots" position (Bender, Mitchell, et al., 2021) and an unnamed-but-substantive opposing position arguing the framing increasingly strains against what these systems visibly do. The book has explicitly committed to NOT resolving this. Later chapters (especially 5 and 8) must not silently tip the scales toward either side — any return to this question should preserve the "live, unresolved, both serious" framing established here.
- **Phone autocomplete "scaled roughly a billion-fold" (the chapter's anchor analogy):** does the same anchoring job for Ch.2 that the spam filter did for Ch.1. Available for light callback in later chapters discussing scale.
- **The LEGO/building-blocks-kit analogy (tokens):** foundational for any later discussion of how raw text becomes something the system can operate on — Chapter 3 (representations/embeddings) will likely need to build on or extend this picture rather than introduce a competing one.
- **The "Paris" mechanism (statistical pattern density, not lookup):** this worked example is now the book's go-to concrete illustration of "fluency without retrieval." Expect it to be referenced again whenever later chapters need to ground an abstract claim about how the system produces correct-sounding output.

## Orchestrator notes
Chapter 2 cleared all gates:
- **Perplexity/AI-detection**: initial WARNING (46.4% suspect, 21 multi-flagged) → after a 19-edit rhythm-and-density rewrite pass (user-confirmed before applying) → PASS (3.8% suspect, 0 multi-flagged — better than Chapter 1's own clean pass)
- **Style-linter**: initial FAIL (1 blocking — unhedged anthropomorphic verb "experiences" applied to the system, plus a section-count warning of 8 vs. the stated 3–6 range) → corrected with a single surgical word-choice fix (and a companion "reads"→"gets" tightening) → PASS. The section-count warning was reviewed and accepted as-is per user decision (names read as natural phrases, pacing works; collapsing sections risked worse pacing than the numeric overage cost)
- **Nonfiction-reviewer**: PASS on first pass, 0 blocking issues, 3 polish-level warnings (naming asymmetry in the debate section reflecting a gap in the source research brief; one slightly-overconfident aside about why true statements cluster densely; a missing beat about who fixes the tokenizer's vocabulary) — none threaten the chapter's argument

Proceed to Chapter 3 planning. Load:
- bible/style.md
- bible/structure.md
- story/synopsis.md
- story/plan.md (Chapter 3 section)
- state/current/* (this state)
- research-full-book-brief.md, Section 3 (Representations/Embeddings) when planning Chapter 3

Chapter 3's opening should pick up directly from the open question Chapter 2 ends on — the reader has been told *what* the system does (predict tokens) and is now owed *what it's holding* internally that makes those predictions work (representations, geometry, "what the model knows" as a spatial/structural fact rather than a stored-fact one).
