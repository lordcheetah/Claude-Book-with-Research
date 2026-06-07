# Knowledge State — Thinking Machines

## Chapter
1 — Learning Without Instructions (complete)

---

## Concepts introduced to reader (accumulates across chapters)

### Established vocabulary

| Term | Plain-language gloss given in Ch.1 | Notes for later chapters |
|------|-------------------------------------|--------------------------|
| **Weight** / **parameter** | "An adjustable setting inside the system" — a number that goes up or down a little; the concrete thing being changed during training | Used interchangeably in Ch.1 ("a weight, sometimes called a parameter"). Later chapters can use either term once introduced — no need to re-gloss, but stay consistent with "adjustable setting" as the underlying plain-language anchor |
| **Training** | "The process of nudging enormous numbers of these settings, a little at a time, based on how well the system is currently performing" — defined as the *name* for the repeated guess/measure/adjust/repeat cycle | Do not redefine; later chapters can say "during training" and rely on the reader knowing this means the loop, not a single event |
| **Loss function** | "Just a number that measures how wrong the guess was" — a confident wrong guess produces a high loss, a close guess a low one | Introduced as the mechanism that makes the loop *measurable*. Chapter 6 (hallucination/failure modes) will likely need to revisit what loss functions do and don't capture |
| **Gradient descent** | "The process by which the system figures out which direction to nudge each dial" — mechanical, blind, local correction; explicitly NOT "wanting," "trying," or "deciding" | Carries the skier-in-fog analogy as its permanent visual anchor (see below). The "good-enough, not best-possible" framing attached to this term is load-bearing for later chapters on failure modes and alignment |

### Analogies in play

| Analogy | Specific job it does | Status / future use |
|---------|----------------------|----------------------|
| **Teaching someone to recognize birds** (showing examples and correcting guesses, vs. handing over a feature manual) | Establishes "teaching by example, not by explanation" as the core alternative to rule-writing — the chapter's first load-bearing idea | Active. Could be echoed lightly if a later chapter needs a quick callback to "examples vs. explicit instruction," but its main job is done — don't overuse |
| **A control panel with a million unlabeled dials** | Makes "weight/parameter" concrete; does double duty by also dismantling the "weights are exotic/magical" misconception (novelty is *scale*, not *kind*) | Active and load-bearing. Chapters 4–5 (attention, emergent capabilities from scale) should be able to lean on "the reader already accepts that scale — not a different kind of thing — is what produces unexpected results." Do not contradict by suggesting any individual weight or component "knows" something |
| **A skier descending a mountain in fog** | Makes gradient descent vivid and *simultaneously* pre-empts the "finds the best possible answer" misconception — the skier reaches *a* low point reachable from their starting position, not necessarily the lowest point on the mountain | Active and explicitly flagged in-text as something that "will resurface, in different shapes, more than once before this book is done." Likely needed again in Chapter 6 (failure modes/hallucination — "good enough from where it started" is directly relevant to why models fail in locally-plausible-but-wrong ways) and possibly Chapter 8 (alignment — optimizing for a measurable proxy isn't the same as optimizing for the real goal) |

### Claims made

| Claim | Hedging level | Notes |
|-------|---------------|-------|
| ML systems learn by being shown labeled examples and adjusting their own internal settings — not by being given explicit rules | **Settled / consensus** (per research brief — this is foundational, uncontested ML mechanics) | This is the chapter's central thesis-claim. Treat as bedrock; later chapters build directly on top of it without re-litigating |
| A trained system's "knowledge" lives in the *pattern* across all its weights together, not in any individual weight | **Settled / consensus** | Directly supports the Ch.7 interpretability discussion — don't let a later chapter imply any single component "contains" a concept in isolation |
| Gradient descent finds a locally-reachable good answer, not a guaranteed global best | **Settled / consensus** (standard description of how the optimization method works) | Foundational for the "powerful but imperfect optimizer" thread — keep the hedging consistent: this is presented as "what the method *is*," not a criticism or a surprising flaw |
| The difficulty of fully explaining what a trained system "knows" is structural — built into the method itself, not a bug, oversight, or sign of sloppy work | **Settled / consensus**, but framed rhetorically as something the reader may not have considered this way before | This is the seed claim for Chapter 7. It is presented gently, as reframing rather than alarm — later chapters revisiting it should preserve that register, not suddenly treat it as a crisis the book hasn't been honest about |
| "Powerful" and "difficult to fully explain" are the same property seen from two angles, not two separate properties that happen to co-occur | **Settled / consensus** as a logical consequence of the prior claims (this is an inference the chapter walks the reader through, not an external citation-needing fact) | This is the chapter's emotional and argumentative payoff — the "defusing" move. Later chapters (especially 6–7) can refer back to "as Chapter 1 showed, these aren't separate problems" |

---

## Argument state

### Established
- **Machine learning as pattern-finding from examples** (Chapter 1) — DONE. Includes: why rule-based approaches fail at scale/over time; what "adjusting internal settings" concretely means; the training loop (guess/measure/adjust/repeat) and its components (loss function, gradient descent); and the consequence that follows necessarily from the method — patterns that can't be fully read back out, which is the root of the book's transparency thread

### Pending (will be introduced)
- **Next-token prediction as the LLM training task** (Chapter 2) — NOW FIRST IN QUEUE. Chapter 1 ends by explicitly handing the reader this exact question ("what, mechanically, is a system doing... when it produces the next word of a sentence?") — Chapter 2 must open by picking this up directly, not by re-deriving it
- Embeddings and vector space representation (Chapter 3)
- Attention mechanism and context windows (Chapter 4)
- Emergent capabilities from scale (Chapter 5)
- Hallucination as training/inference gap (Chapter 6)
- Black box / interpretability limits (Chapter 7)
- Alignment problem, consciousness question, open trajectory (Chapter 8)

---

## Analogy continuity tracker

| Analogy | Chapter introduced | Still active? | Notes |
|---------|-------------------|--------------|-------|
| Teaching someone to recognize birds (examples vs. explanation) | 1 | Yes — light/background | Job mostly done; available for brief callback only, not re-explanation |
| Control panel with a million dials (weights/parameters; novelty-is-scale) | 1 | Yes — load-bearing | Expect direct reliance in Chapters 4–5; do not contradict "no single dial knows anything" |
| Skier in fog (gradient descent; locally-reachable-not-globally-best) | 1 | Yes — load-bearing, explicitly flagged for return | Expect direct reliance in Chapter 6 (and possibly 8); the text itself promises this analogy will recur "in different shapes" |

---

## Notes
- Track introduced vocabulary so later chapters can reference without re-explaining
- Track analogies to ensure consistency (don't contradict a prior analogy in a later chapter)
- Flag when a prior claim is complicated or nuanced by a later chapter
- **Chapter 1 content is tagged "settled/consensus" throughout per the research brief** — this is uncontested ML mechanics, not a contested or speculative claim. Later chapters introducing more contested material (e.g., emergent capabilities, alignment, consciousness) should make the hedging-level shift legible to the reader by contrast, since Ch.1 has now established what "settled" sounds like in this book's voice
