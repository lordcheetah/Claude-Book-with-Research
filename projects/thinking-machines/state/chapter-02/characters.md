# Reader State — Thinking Machines

## Chapter
2 — Reading as Prediction (complete)

---

## Nonfiction reader state (replaces character states)

This file tracks the implied reader's knowledge and expectations across the book.
Update via state-updater after each chapter.

---

## What the reader knows
(after Chapter 2, cumulative)

**Carried forward from Chapter 1**: the rules-vs-examples distinction; weights/parameters as adjustable settings ("a million dials," now known to scale to billions); the training loop by name and mechanism (guess → measure via loss function → adjust via gradient descent → repeat); the three corrected Ch.1 misconceptions; the transparency-problem implication; the "powerful AND hard to explain" reframe.

**New in Chapter 2**:
- **What a token is, and why tokens aren't words**: text reaches and leaves the system as chopped-up sub-word pieces drawn from a fixed kit (the LEGO-kit picture) — sometimes whole words, sometimes fragments, sometimes single characters or punctuation. The reader has had the "strawberry" letter-counting oddity explained concretely and satisfyingly: the system may never see "strawberry" as eight letters at all, only as whatever pieces its kit happens to break it into
- **Next-token prediction as the entire training objective, stated with full confidence**: every large language model behind the recent headlines was trained to do exactly one thing — given everything so far, guess which token comes next — repeated an almost incomprehensible number of times, across nearly everything humans have digitized and written down. Not a hidden second task. Not "understand," "know," or "be helpful." One job, one sentence, nothing else mixed in
- **The "Paris" mechanism**: the reader has been walked, slowly and concretely, through *why* a system trained only to predict produces fluent, correct-sounding output — not retrieval from a labeled cell, but reproduction of a statistical pattern so dense that one continuation overwhelms every alternative. "Paris" isn't looked up; it's the single most likely next piece, by an enormous margin
- **The stochastic-parrots debate, named fairly and left open**: the reader now knows this is a live, serious, unresolved argument among people who have spent careers on it — one camp (Bender, Mitchell, et al.) holding that fluency is not understanding, full stop; another holding that this framing increasingly strains against what these systems visibly do. The reader has been told plainly: nobody currently knows, and the book isn't going to pretend otherwise
- **The structural sounds-true/is-true gap**: the reader now understands, as a matter of structure rather than flaw, that a system optimized purely for "sounds right" has no built-in way to distinguish that from "is right" — and that this single fact is the root of both the fluency just explained and a failure mode the book will return to directly in Chapter 6

## What the reader does NOT yet know
- What the system holds *internally* that makes its predictions this good — representations, embeddings, vector space, "what the model knows" as a structural/spatial fact (Chapter 3's territory entirely, and the literal question Chapter 2 ends on)
- Attention mechanism and context windows (Chapter 4)
- Why/how capabilities seem to "emerge" at scale (Chapter 5)
- Anything about failure modes, hallucination, or alignment in detail (Chapters 6, 8) — though the *seed* for Chapter 6 (the sounds-true/is-true gap) has now been planted and named

## Reader's likely questions going into next chapter
- **The literal bridge question Chapter 2 ends on, verbatim in spirit**: "If prediction is the task, what is the system actually *holding*, internally, that makes its predictions this good? What does 'the capital of France is Paris' look like inside something that's never seen a map?" — the reader has been handed this explicitly and is owed a direct answer, the same way Chapter 2 opened by directly answering Chapter 1's bridge question
- A quieter, more unsettled question likely sitting underneath: "If nobody can even agree whether this counts as 'understanding' — and the book just told me so, plainly — how am I supposed to feel about systems built this way being this capable?" (Chapters 5 and 8 territory; the seed is now planted, and the reader has been primed to expect the book to handle hard disagreements by naming them rather than dodging them)

---

## Tone calibration
- Skepticism level: **shifted from "oriented and engaged" (post-Ch.1) to actively curious and slightly unsettled, in a productive way** — Chapter 2 walked the reader through the field's single most contested live debate without protecting them from its genuine difficulty, and didn't resolve it. That's a different emotional texture than Ch.1's "click of recognition" — it's closer to "huh, I didn't expect the experts to be this divided either," which is itself a small trust-building move (the book demonstrably isn't oversimplifying to make itself sound authoritative).
- Technical tolerance: confirmed willing to sit with genuine unresolved ambiguity, not just multi-step analogies — the chapter asked the reader to hold "this looks exactly like knowing, and nobody knows if it is" without rushing to relieve that tension, and the reader (per the chapter's own design) should come away feeling respected rather than left hanging.
- Emotional register: **moved from "grounded and ready" to grounded, engaged, and primed for the "what's underneath" turn** — the reader has just been told, in effect, "we know *what* it's doing in full mechanical detail, and that still doesn't fully explain *why* it works this well." That's the exact emotional setup Chapter 3 needs to open into: not anxiety, but genuine appetite for the next layer down.

---

## Notes
- Track the implied reader's knowledge state so later chapters don't re-explain or skip steps
- Flag if a chapter introduces a concept that builds on something not yet established
- Chapter 3 can safely assume full fluency with: token/tokenization, next-token prediction as the training objective, the "Paris" mechanism (pattern density vs. retrieval), the stochastic-parrots debate (named, unresolved, must stay unresolved), and the sounds-true/is-true structural gap (seeded, due back in Ch.6). It should NOT assume any familiarity with embeddings, vector space, geometric/spatial metaphors for "meaning," or attention — those are Chapter 3 and 4's territory entirely, and the reader is actively waiting to be handed them.
