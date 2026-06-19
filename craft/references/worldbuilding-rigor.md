# Worldbuilding & Argument Rigor

A rigor toolkit for two jobs: keeping an invented world's rules **consistent**
(hard SF, fantasy magic, any story with invented systems) and keeping a
nonfiction argument **honestly grounded** (evidence actually supports claims).
Adapted from a metascience-derived framework (Ioannidis, Gelman, Taleb,
Hossenfelder, Pearl, Boyd, Page, Kahneman, Fuller).

Throughout, **"the rules"** means: for fiction, your established world rules /
canon (bible/universe, magic system, physics); for nonfiction, your thesis and
the established facts you're reasoning from. The reviewers that use this file:
`world-rules-reviewer` (SF/fantasy system logic) and `nonfiction-reviewer`
(evidence vs. claims).

---

## Part 1 — Operating Principles

**1. Mechanism over association.** "This feels consistent" is association. "This
is consistent *because* X causes Y" is mechanism. A world element (or a claim)
without an unbroken causal chain back to the rules is a coincidence that will
contradict something later. *Pearl's Ladder of Causation:* most reasoning sits
at Rung 1 (X correlates with Y); push audits to Rung 2 (what changes if we alter
X?) and Rung 3 (what would have happened if X hadn't occurred?). The key audit
question: **"If we remove this mechanism, what downstream content breaks?"**

**2. The Ioannidis corollaries** — six conditions that make a finding (or a piece
of worldbuilding/argument) structurally unreliable. When 3+ are present, slow
down, narrow scope, and pin down the rules before writing.

| Corollary | Worldbuilding / argument equivalent |
|---|---|
| Small sample | Checking one chapter/file and missing contradictions in the rest |
| Small effect | Elevating a micro-inconsistency (really just perspective) to a "violation" |
| Data dredging | Hunting for problems with no specific hypothesis → finding "issues" by chance |
| **Analytical flexibility** | **Reinterpreting a rule until the new content no longer violates it — the #1 danger** |
| Prejudicial interest | Writing what you want to be true and ignoring the constraints that prohibit it |
| Competition/heat | Rushing to ship without cross-checking → contradictions |

**3. The Garden of Forking Paths (Gelman).** If you would have written the rule
differently had the content come out differently — i.e. you adjusted the rule to
fit the content rather than testing the content against the rule — you're in the
Garden. *Detection:* did any rule/definition change in the same session as the
new content?

**4. The Aesthetic Fallacy (Hossenfelder).** "Elegant" and "fits the narrative
beautifully" are not consistency. *Test:* would you accept this mechanism if it
were ugly but consistent? If you'd reject a consistent thing because it "doesn't
feel right," you're applying aesthetics, not rules.

**5. The Humpty Dumpty problem (Taleb).** You can't validate a complex system by
checking one piece in isolation — the connections are where it breaks. *Test:*
have you traced this element through every system/claim that connects to it, not
just the immediate layer?

**6. Predictive power (BSI).** A rule that can't predict outcomes is decoration.
*Test:* could someone unfamiliar with your world derive the right answer from the
established rules alone? If the rules don't constrain the answer, they lack teeth.
(For nonfiction: does your framework predict cases beyond the ones you chose to
present?)

**7. Simple rules (Epstein).** If a rule needs constant exceptions, the rule is
wrong — fix the rule, don't patch around it.

**8. Avoid the new orthodoxy.** Rules should stay *diagnostic, not dogmatic.* If
a genuinely good idea is being rejected only because "the rules say no," check
whether the rule has become rigid beyond its purpose. Deliberate ambiguities in
a world (the things left unexplained on purpose) are escape valves — don't
force-resolve them.

---

## Part 2 — Triage Filters (separate real problems from noise)

Before acting on any flagged problem, run these six filters. Findings that fail
get downgraded or dropped; findings that pass get reported with exact location.

1. **Sample size** — was the *whole* manuscript/bible checked, or just one
   source? A rule consistent in one place may conflict elsewhere. (Grep first.)
2. **Effect size** — is the fix proportional to the severity? A low-priority
   drift doesn't justify a 20-file cascade.
3. **Confirmation bias** — was the content designed to fit the rules, or were the
   rules quietly reinterpreted to fit the content?
4. **Flexible analysis** — did any rule definition change this session? If so,
   don't clear it without explicit author approval.
5. **Replication** — does the rule hold across *all* cases subject to it, not
   just the one in front of you?
6. **Survivorship bias** — which files/claims that reference this concept
   *weren't* checked? Grep for every mention before declaring consistency.

---

## Part 3 — Adversarial Protocols

**Red-team escalation ladder.** Before accepting a new element, build the
strongest case *against* it (genuinely hostile, not devil's advocate):
1. Does it contradict any explicit rule?
2. Does it contradict any implicit constraint (downstream implications)?
3. Does it survive application across every case/culture it should govern?
4. Would a hostile reader find it inconsistent?
5. Strip the narrative beauty — is the bare mechanism still valid?
If any argument survives refutation, the element fails.

**Russell Conjugation stripping.** Synonyms carry the same fact with different
emotional charge ("I am firm / you are obstinate / he is pigheaded"). Restate the
proposal in the most boring, clinical language possible before judging it:

| Emotive framing | Neutral restatement |
|---|---|
| "This elegant mechanism unifies…" | "This connects X to Y via Z" |
| "This beautifully resolves the tension…" | "This removes the contradiction between A and B" |
| "This feels deeply wrong for the world…" | "This contradicts rule N in file Y" |

If it only holds in emotive framing, it's aesthetic, not rule-sound.

**Ensemble thinking (Page).** Never judge through a single lens. Apply several:
does it violate a world rule? does it follow established biology/economics/etc.?
is it consistent across all cases? does it create productive tension or just
contradiction? can you *derive* what happens next? does it hold aesthetics-
stripped? 4+ agreeing → high confidence; 2–3 disagreeing → investigate the
disagreement (it usually marks a real issue); all agreeing too easily → suspect
confirmation bias.

**Adversarial collaboration (Kahneman)** — when two readings of a rule conflict
(including author vs. agent): each states the other's position to its
satisfaction → both agree in advance what evidence resolves it → both pre-commit
to what would change their mind *before* checking → record the result either way.
No goalpost-shifting after the evidence is in.

**CADS four-quadrant consequence check (Fuller).** When designing a new system or
making a claim, fill all four: anticipated-desired, anticipated-undesired,
**unanticipated-desired, and unanticipated-undesired.** The fourth quadrant —
the bad thing you didn't predict — is the one that usually breaks consistency or
sinks an argument. Force yourself to name something in it.

---

## How to use this

- **world-rules-reviewer / world-assumptions-reviewer:** apply Part 1 (esp.
  mechanism, Humpty Dumpty, predictive power), triage findings through Part 2,
  and use the red-team ladder + ensemble lens from Part 3.
- **nonfiction-reviewer:** the Ioannidis corollaries, Garden of Forking Paths,
  triage filters, and CADS quadrants map directly onto "does the evidence
  actually support the claim, and what did the argument quietly skip?"
- **interrogating-design / civilization-builder / magic-system-designer:** use
  the red-team ladder and Russell Conjugation check when pressure-testing a
  single decision.
