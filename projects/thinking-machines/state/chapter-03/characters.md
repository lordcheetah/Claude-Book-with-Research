# Reader State — Thinking Machines

## Chapter
3 — Representation: A Map With No Master Plan (complete)

---

## Nonfiction reader state (replaces character states)

This file tracks the implied reader's knowledge and expectations across the book.
Update via state-updater after each chapter.

---

## What the reader knows
(after Chapter 3, cumulative)

**Carried forward from Chapters 1–2**: the rules-vs-examples distinction; weights/parameters as adjustable settings (now known to scale to billions); the training loop (guess → measure → adjust → repeat); tokens and tokenization (the LEGO-kit picture); next-token prediction as the entire training objective, stated with full confidence; the "Paris" mechanism (pattern density, not retrieval); the stochastic-parrots debate, named fairly and left open; the structural sounds-true/is-true gap (seeded for Chapter 6).

**New in Chapter 3**:
- **Representation as position**: the reader now knows, concretely and by name, what the system holds internally — not facts, not records, but *positions*. Every token corresponds to a specific point ("an embedding") in an enormous structured space, and the reader has the plain-language definition of "embedding" as a coordinate-list, paired with the everyday "three blocks east, two blocks north" image
- **The map-with-addresses picture, caveat included**: the reader has been given the central organizing image for "meaning as geometry" — concepts that are close in meaning sit close together on the map — with the honest caveat (the real geometry is messier than any map a person could draw) delivered up front, not as a footnote
- **A famous claim, checked in real time**: the reader has watched the book do, live and on the page, exactly the kind of skepticism it has spent two chapters teaching — taking a decade-old, widely-repeated demonstration ("king − man + woman ≈ queen"), asking "has anyone gone back and checked it?", and reporting honestly what the check found (the popular version doesn't survive; one detailed review called it "fake news"). Crucially, the reader has also been walked carefully through *what survives* — the underlying claim that relationships are encoded as directions and distances remains "settled... every bit as solid as the first [claim]" — so the correction lands as a model of precision, not as a debunking that undermines the chapter's own foundation
- **The mechanism beneath "Paris," one layer deeper**: the reader now knows not just *that* "Paris" emerges from pattern density (Chapter 2) but *what kind of thing* produces it — no drawer, no record, but a "standing relationship between locations," a distributed pattern across a structure with no architect, exactly like a city that organized itself into neighborhoods with no zoning office ever involved
- **Distributed representation, named and defined**: "information that exists as a pattern spread across a structure, with no single piece of it responsible for the whole" — and the reader has been shown, explicitly, that this is the *same shape* as ideas already encountered twice before ("novelty is scale, not kind," now paying off for a third time)
- **The "knowing" question, reopened one layer deeper**: the reader has been told, in the book's most Carroll-influenced moment yet, that whether functional "knowing" (reliable correct output, no locatable record) amounts to a lesser kind, a different kind, or a sign that our definitions were never crisp to begin with — "is not a question this book is going to resolve for you. It can't. Nobody currently can." And critically: the reader has been shown this is *the same disagreement* as the stochastic-parrots debate from Chapter 2, just visible at a new depth now that the geometry underneath the fluency is in view

## What the reader does NOT yet know
- **The mechanism that relocates a position in real time, word by word, as context changes** ("bank" near "river" in one sentence, near "interest rate" in the next — the same starting point, *moved*, on the fly) — this is the concrete, specific, named puzzle Chapter 3 closes on, and it is Chapter 4's territory entirely
- The architecture itself — attention, context windows — has not been named or even gestured at beyond "something has to be doing that relocating... [it] lives inside an architecture this book hasn't named yet"
- Why/how capabilities seem to "emerge" at scale (Chapter 5)
- Anything about failure modes, hallucination, or alignment in detail (Chapters 6, 8) — though both seeds (sounds-true/is-true gap; the now-twice-reopened "knowing" question) are planted and primed

## Reader's likely questions going into next chapter
- **The literal bridge question Chapter 3 ends on, verbatim in spirit**: "What is the *thing*, precisely, that reads a sentence and decides, word by word, where everything in it actually belongs — this time, and not the last time, and not the time after that?" — the reader has been handed this explicitly, with the concrete "bank" example doing the work of making it feel urgent rather than abstract, and is owed a direct answer the same way Chapter 3 opened by directly answering Chapter 2's question
- **A growing meta-awareness of the book's own method**: having now watched the book name a live debate and refuse to resolve it (Ch.2), and then check a famous claim, find it wanting, and precisely bound the correction (Ch.3), the reader is likely starting to *expect* this pattern — and to trust the book somewhat more because of it. This is a genuine asset going into Part 2; later chapters can lean on this earned trust rather than re-establishing it from scratch
- **A sharpened version of the "knowing" unease from Chapter 2**: the reader now holds a more precise version of "if nobody can agree whether this counts as understanding, and I can now *see* the geometry underneath the fluency and it still doesn't settle the question — what does that tell me about the question itself?" (Chapters 5 and 8 territory; the seed has now been planted twice, at two depths, and the reader is primed for the book to keep treating it with the same evenness)

---

## Tone calibration
- Skepticism level: **shifted from "actively curious and slightly unsettled" (post-Ch.2) to actively curious, appropriately skeptical of even its own favorite tools, and quietly more trusting of the book itself** — Chapter 3 didn't just describe skepticism, it *performed* it, live, on a claim a less careful book might have leaned on uncritically. That performance is itself a trust-building move with a different texture than Ch.2's "the experts are this divided" — it's closer to "this book will tell me when something I might have read elsewhere doesn't hold up, even if it's a claim *this book* would benefit from being true."
- Technical tolerance: confirmed comfortable holding two ideas in tension at once — "the famous proof of this idea is broken" and "the idea itself is more solid than ever" — without collapsing them into a single verdict. The chapter explicitly modeled how to do this ("that would be exactly the wrong lesson... let's be precise about what actually got disproved and what didn't"), and the reader should come away from it slightly more capable of holding that kind of nuance going forward, not just having watched the book hold it.
- Emotional register: **moved from "grounded, engaged, and primed for the 'what's underneath' turn" to grounded, trusting, and now actively anticipating the next mechanical reveal** — the chapter closed not on an abstract gesture but on a vivid, concrete, almost itchy question (why does "bank" move?) that the reader can feel rather than merely register intellectually. That's the precise emotional setup Chapter 4 needs to open into — not dread, not cliffhanger anxiety, but the specific kind of "wait, how DOES that work?" that makes a reader turn the page.

---

## Notes
- Track the implied reader's knowledge state so later chapters don't re-explain or skip steps
- Flag if a chapter introduces a concept that builds on something not yet established
- Chapter 4 can safely assume full fluency with: embeddings/positions/the map-with-addresses picture, distributed representation, the "settled vs. corrected vs. open" three-way distinction as demonstrated live (not just described), and the specific "bank relocates by context" puzzle as a named, concrete, felt question. It should NOT assume any familiarity with attention, context windows, or any mechanism for *how* a position changes in real time — that is Chapter 4's territory entirely, and the reader is actively waiting, with unusual specificity this time, to be handed it.
- **This chapter marks the close of Part 1 ("What it does").** Chapter 4 opens Part 2 ("What it knows") — the reader's tone calibration above reflects a reader who has just finished a satisfying first movement and is leaning forward into the second, not one who needs re-orientation or re-grounding. Chapter 4 can open at full speed, the same way Chapter 2 and Chapter 3 both did.
