# Reader State — Thinking Machines

## Chapter
4 — Attention (complete)

---

## Nonfiction reader state (replaces character states)

This file tracks the implied reader's knowledge and expectations across the book.
Update via state-updater after each chapter.

---

## What the reader knows
(after Chapter 4, cumulative)

**Carried forward from Chapters 1–3**: the rules-vs-examples distinction; weights/parameters as adjustable settings; the training loop; tokens and tokenization; next-token prediction as the entire training objective; the "Paris" mechanism (pattern density, not retrieval); the stochastic-parrots debate, named fairly and left open; the structural sounds-true/is-true gap; representation as position (embeddings, the map-with-addresses picture, caveat included); distributed representation; the live-corrected king/queen demo and its reusable "present → check → bound the correction" rhetorical template; the reopened "knowing" question; and the specific, urgent, named puzzle this chapter was owed: why does "bank" relocate on the map depending on context?

**New in Chapter 4**:
- **Attention, named and explained — and the puzzle resolved**: the reader now holds the direct mechanical answer to the question Chapter 3 closed on. Attention is the computation that, for every word, recalculates how relevant every other word is to interpreting it — fresh, every time — and the reader has watched this resolve "bank" specifically, word for word, in the same two sentences that posed the puzzle. This is not an abstract description; the reader has seen the mechanism work on the exact case they were promised an answer to
- **The trophy/suitcase puzzle**: a second, sharper illustration of the same underlying problem (pronoun resolution), used to demonstrate that flipping a single word flips the correct interpretation entirely — proof that whatever resolves this has to weigh the *whole* sentence at once
- **A pre-empted misconception**: the reader has been told, plainly and memorably, that "attention" is not the model "paying attention" in any humanlike sense — it's closer to a spreadsheet of relevance scores, recalculated from nothing every time, than to a spotlight of conscious focus. This correction arrived *before* the word could quietly start doing anthropomorphic work in the reader's head, which the chapter named directly as its reason for delivering it as its own beat
- **Multi-head attention**: the reader knows the system runs many of these relevance-computations in parallel, each potentially specializing in a different kind of relationship (grammar, meaning, proximity) — "not one lens on the sentence, but dozens, overlapping"
- **A fresh, light callback to the transparency problem**: immediately after the multi-head explanation, the reader was reminded — in one calm sentence, no elaboration — that the book can describe with precision *what* these parallel computations do while still not being able to fully read out what any one of them specifically learned to track, "the same shape... as the transparency problem this book named back at the very beginning." The six-chapter-old thread is warm again, without becoming a digression
- **The context window**: the reader now has a name and a concrete image (“the stage”) for the bounded span of text the system can hold and weigh at once — and has seen, for the first time, the architecture's literal *boundary* come into view
- **Quadratic cost**: the reader knows, with concrete numbers attached (roughly a quarter-million comparisons at 500 words, pushing toward a million at 1,000), that doubling the input roughly quadruples the computational cost — and has been told plainly that this is a structural property of the mechanism, not a temporary engineering snag awaiting a fix
- **"Lost in the middle"**: the reader has been handed a name for something they have very likely already experienced — information from earlier in a long conversation getting less reliable use, even though it's technically still "in the window." Critically, the reader has also been handed the correct frame for this (a property of how the comparison gets made, via the conference-call analogy) and has watched the book explicitly name and reject "the model forgets" as the wrong way to think about it
- **Power and limit as one structural fact**: the reader has been shown, without the book naming its own favorite retired phrase ("novelty is scale, not kind"), that the very thing that makes attention powerful — its ability to weigh everything against everything — is the same thing that defines its hard limits. The shape of the idea is present; the worn label is not

## What the reader does NOT yet know
- What actually changes, mechanically, when this architecture is simply built larger — more parameters, more data, more compute (Chapter 5's entire territory)
- Why capabilities seem to "emerge" at certain scales rather than growing smoothly (Chapter 5)
- Anything in detail about hallucination, interpretability limits, or alignment (Chapters 6, 7, 8) — though the relevant seeds (sounds-true/is-true gap; the "knowing" debate; and now a freshly-warmed transparency thread) are all primed and ready

## Reader's likely questions going into next chapter
- **The chapter's own sharpened bridge question, close to verbatim**: "What actually changes, mechanically, when you take this same machinery — this same attention, this same architecture, this same fundamental task — and simply build it larger? Why does 'bigger' stop behaving like 'more of the same' and start behaving like something else entirely?" This is a more specific, more urgent version of the vague scale-curiosity the reader would have carried in unprompted — Chapter 4 did real work sharpening it
- **A continuing, deepening trust in the book's own honesty about its tools**: having now watched the book pre-empt a misconception about its own central metaphor ("attention" almost lying to you, and the book catching it before it could take root), the reader is primed to extend that same trust into Chapter 5's more contested territory — useful, since the brief flags Ch.5 as needing "extra care"
- **A reader who has just watched two genuine payoffs land back-to-back** (the "bank" puzzle resolved; "lost in the middle" named and correctly framed) and is now in the specific emotional register of "okay, this book delivers on what it promises — what's the next thing it's about to hand me?"

---

## Tone calibration
- Skepticism level: **holding steady at "actively curious, appropriately skeptical of even its own favorite tools"** — Chapter 4 didn't need to perform a live correction the way Ch.3 did (no famous claim needed checking here), but it *did* perform the related move of catching its own central metaphor before it could mislead, which reads to the reader as the same kind of vigilance in a different key. The trust built in Ch.3 carries forward intact and slightly reinforced.
- Technical tolerance: confirmed comfortable with concrete numbers attached to abstract claims (the quarter-million/million comparison counts) — this is new territory for the book's register (Chapters 1–3 mostly used proportional/relative framing — "scaled a billion-fold," "roughly quadruples") and the reader handled the shift to countable terms without strain. Worth noting as a register option available to later chapters when an abstraction needs grounding
- Emotional register: **moved from "grounded, trusting, anticipating the next mechanical reveal" (end of Ch.3) to satisfied-and-sharpened — a reader who was promised a direct answer, got one, watched it resolve the *exact* example that posed the question, and is now carrying a more precise, more urgent version of the next question than they would have generated on their own**. This is close to an ideal handoff state for a chapter that opens "HANDLE WITH EXTRA CARE" territory — the reader's goodwill is high, their question is sharp, and they're ready to sit with genuine open debate rather than needing to be coaxed into caring about it first

---

## Notes
- Track the implied reader's knowledge state so later chapters don't re-explain or skip steps
- Flag if a chapter introduces a concept that builds on something not yet established
- Chapter 5 can safely assume full fluency with: attention, multi-head attention, the context window, quadratic cost, "lost in the middle," and the now-twice-demonstrated "present a claim, then precisely calibrate how confident to be about it" move (Ch.3's live correction; Ch.4's settled-vs-illustrative distinction in the multi-head passage). It should NOT assume any familiarity with emergent capabilities, scaling laws, or anything from the "actively debated" bucket — that is genuinely new territory, and per the research brief, Ch.5 needs to be handled with extra care
- **This chapter delivered the arc-reviewer's recommended transparency-thread callback exactly as scoped** — one light sentence, correct placement, correct register, no elaboration. The thread is warm again heading into the back half of the book, three chapters ahead of its full payoff in Chapter 7
- **"Novelty is scale, not kind" remains correctly retired through this chapter** — one final, earned appearance is reserved for Chapter 5, which the research brief flags as needing special care. The reader has not seen this phrase since Chapter 3 and is not expecting it; its return in Ch.5 should feel like a culmination, not a repetition
