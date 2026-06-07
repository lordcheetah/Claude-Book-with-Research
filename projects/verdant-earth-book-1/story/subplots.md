# Subplot Registry — The Mycelial City

*Last updated: Chapter 6 (FINAL CHAPTER OF BOOK 1 — manuscript complete)*

---

## Status Summary — After Chapter 6 (Book 1 Complete)

| Status | Count |
|--------|-------|
| Open (healthy) | 0 |
| Open (⚠️ stalled) | 0 |
| Open — deliberately left for series / handoff | 2 |
| Planned (not yet introduced) | 0 |
| Resolved | 15 |

### Needs Attention — End of Book 1 Review
- **No threads are dangling by accident.** Every thread that closes in Chapter 6 closes on-page, with an explicit mechanism. Two threads remain open *by design* and are flagged below as potential series/sequel hooks rather than oversights.
- **CORP-01 (Altera director identity)** — closes-by-handoff, not resolution. Del names it explicitly as "a name for the Council's investigation now... not ours to chase any further." This is the single most natural sequel/series hook: a named, bounded, unresolved identity now sitting inside an active institutional investigation. If Book 2 (or a series) wants a thread to pick back up, this is the cleanest one — it was left open *on purpose* and *on the record*.
- **Emil Strand / negligence-vs-complicity** (sub-thread of CORP-01, distinct from REL-02 — REL-02/Yara-Nwosu is fully RESOLVED below) — explicitly held open by design. "A name on a signature... now part of the formal certification review record." Whether Strand knew what he signed is unresolved and is framed as belonging to a process that will run "real months" — a second clean series-level hook, also deliberate. Note: this is NOT the same thread as Yara/Nwosu (REL-02), which closes cleanly via Nwosu's resignation in this chapter.
- **CORP-02 (Rational Innovation)** — issues a public denial but is not otherwise confronted on-page; the Technical Council investigation continues "regardless of the denial." This is folded into the CORP-01 handoff rather than standing as its own loose end — the antagonist organization's fate is now explicitly a matter for an ongoing institutional process the book has chosen not to follow further.
- **Recommendation to orchestrator**: Book 1 can be considered structurally complete with no accidental dangling threads. The two items above are the natural candidates to seed a Book 2 synopsis, should the series continue — both were closed *as open questions*, which is a deliberate authorial choice rather than a gap.

---

## MAIN-01 — Biofilter Anomaly Investigation
**Type**: main plot
**Status**: RESOLVED (Chapter 6)
**Introduced**: Chapter 1
**Last active**: Chapter 6
**Summary**: Stations Seven, Eight, and Nine in the eastern inlet show consistent cyanobacteria elevation paired with a flat mycorrhizal coherence index — confirmed real by physical lab assay (chain of custody intact). Suppression is coordinated across both the Water Authority and the Accord, running for at least 47 days and predating any observable bloom formation. *Chapter 3 advance*: Mechanism fully identified (selective substitution rule on cyanobacteria threshold; coherence response masked). Altera Technical Services identified as the firmware installer. *Chapter 4 advance*: Escalation package filed; both Yara and Del suspended within four minutes; the official path is cut off. Clock at ~40 hours. *Chapter 5 advance*: Investigation phase completes; the Compact deposit package is built and armed for 5 AM upload. Clock at ~22h.
**Chapter 6 resolution**: The deposit fires at 5 AM and triggers exactly the cascade the Compact promised — independent verification by strangers within 19 minutes, automated Technical Council notification, Altera's certification contracts frozen citywide, the certification review formally opened with Strand's signature in the record, Rational Innovation's public denial, and Director Nwosu's resignation. In parallel, Yara walks the manual biofilter override sequence by hand at Stations Seven, Eight, and Nine — physically bending the cyanobacteria curve back before the Council's emergency team arrives. The team's lead confirms on-page that without Yara's manual remediation, "we'd be standing in a remediation that doesn't work" — the narrow window closed *because* she acted inside it. The chapter's final scene returns to Station Seven for a clean sensor check: "The smell was right and the numbers were right" — the lie that opened the book is gone, replaced by a true, routine, signed log entry. The investigation, the suppression mechanism, the institutional response, and the physical crisis all resolve in the same chapter, in the correct causal order (truth surfaces → institutions move slowly → competence closes the gap institutions can't close fast enough).
**Assessment**: Earned. The resolution doesn't let the institutional mechanism alone save the day (which would have undercut the book's thesis about correct process being both the danger and the cure) — it requires Yara's hands-on competence to close the gap, which pays off both her arc and the central thematic argument (see CHAR-01).

---

## MYST-01 — The Deleted Report
**Type**: mystery
**Status**: RESOLVED (Chapter 3)
**Introduced**: Chapter 1
**Last active**: Chapter 3
**Summary**: Report EI-2091-447 was deleted after submission. Chapter 2 confirms a second tier of deletion: the intake receipt (EI-2091-447-RCPT) has also been lifted from what should be an append-only receipt log — a level of access far beyond a misfile or administrative error. Yara briefed Director Nwosu with the notebook and lab results. Nwosu acknowledged the anomaly, invoked an internal process, and rotated Yara off the eastern inlet rather than acting on the evidence. Yara transferred her local report copy to a personal drive off the Authority network before the meeting. The two-tier deletion and the speed of Nwosu's response indicate that whoever cleared the report has reach inside the Authority's administrative infrastructure — and is watching. *Chapter 3 resolution*: Firmware mechanism confirmed as the underlying suppression vector. The deletion of EI-2091-447 is now understood as downstream of the firmware modification installed by Altera — the report surfaced an anomaly that the installed mechanism was designed to hide. The "how" of suppression is resolved; the who-coordinated and why questions are now carried by MYST-02 and MYST-03.
**Next expected**: No further movement expected on this specific thread; mechanism is resolved.

---

## MYST-02 — The Suppression Mechanism
**Type**: mystery
**Status**: OPEN
**Introduced**: Chapter 1
**Last active**: Chapter 4
**Summary**: Suppression is confirmed as coordinated: Del's 60-day historical pull shows it began 47 days ago, ahead of any detectable bloom formation. Within 9 hours of Del running his internal query, the Accord reclassified the affected inlet stations as "scheduled maintenance" — in the same 6-hour window as the deletion of Yara's report on the Authority side. The suppression is therefore active across two independent institutions and responding in near-real-time to investigative moves. *Chapter 3 advance*: Mechanism now fully identified. The firmware installed by Altera substitutes a synthesized nominal cyanobacteria reading above a set concentration threshold; below the threshold real data passes through, making wet-season fluctuations look genuine. It also masks the mycorrhizal coherence response, replacing the colonies' actual suppression signal with a nominal value before data leaves the node. The modification sits at the monitoring-software layer and is hardware-agnostic — it ran identically on Cascavel Biotech and Northbrook Biosystems equipment. Supply-chain compromise ruled out; the site visit was the vector. The open question is multi-layer coordination: who above Altera directed and benefited from the installation. *Chapter 4 advance*: The upper coordination layer is now explicitly named as an open gap in the evidence package. The package can name Altera, the firmware, and Rational Innovation — but it cannot name who inside the Authority gave them the door. Someone with extraordinary Authority credentials deleted EI-2091-447 from an append-only system and imposed Yara's rotation; that access vector is unidentified (see also INST-02). The inside actor gap is on record in the filed package.
**Next expected**: Chapter 5-6 — inside actor identity is a primary unresolved thread; the Compact filing may surface it or force it into the open.

---

## THREAT-01 — The Algal Bloom Clock
**Type**: subplot / escalating threat
**Status**: RESOLVED (Chapter 6) — contained, not eliminated
**Introduced**: Chapter 1 (implicit in pattern data)
**Last active**: Chapter 6
**Summary**: Yara ran explicit bloom projections from the raw 47-day data, arriving at a fixed target of chemical irreversibility at approximately Hour 114. *Chapter 3-5 advances*: Clock falls from ~66h to ~22h remaining as the deposit is built and armed for 5 AM upload. Two clocks run in parallel heading into the finale: the bloom's chemical countdown and the Compact's mandatory-response window.
**Chapter 6 resolution**: At Hour 92 (deposit fires), ~22 hours remain and the bloom clock has not moved — "The deposit firing had not moved the bloom one hour." Yara walks the manual override sequence by hand, station by station, bending the cyanobacteria curve back under the kill threshold, while the Council's emergency team is still en route. They arrive to find the worst of the curve already bent and confirm explicitly: "If this hadn't been started this morning, we'd be standing in a remediation that doesn't work. We're inside the window because somebody put us inside it before we got here." The narrowness is named as "specific and earned" — a few hours later and the colonies would have crossed the line while the powered gear was still being unloaded. The chapter closes on a clean sensor check at Station Seven: smell right, numbers right, certified function restored, logged in Yara's own hand.
**Assessment**: Earned and structurally clean. The clock doesn't resolve through the institutional mechanism alone (which would have been a deus ex machina given how slowly institutions move in this book) — it resolves because Yara's manual competence closes a gap that no credential or process could close fast enough. This is the precise mechanism the book has been building toward since Chapter 1: process surfaces the truth, but only hands-on expertise saves the system in time.

---

## HOOK-01 — Physical Samples Pending
**Type**: dangling hook
**Status**: PAID OFF (Chapter 2)
**Introduced**: Chapter 1
**Last active**: Chapter 2
**Summary**: Lab assay results returned overnight. Results confirm elevated cyanobacteria in all three samples (EI-S7-2091-0605), matching the raw sensor pattern precisely. Chain of custody is intact — the paper slip is in Yara's possession. The samples constitute physical, off-network evidence that the anomaly is real. Yara used the lab results as part of her briefing to Nwosu.
**Next expected**: No further movement expected on this thread; evidence is in hand and on personal drive.

---

## HOOK-02 — Del's Sixty-Day Historical Pull
**Type**: dangling hook
**Status**: PAID OFF (Chapter 2)
**Introduced**: Chapter 1
**Last active**: Chapter 2
**Summary**: Del arrived at his Upper Terraces office with the full 60-day historical pull for Stations 7, 8, and 9. The data reveals the suppression began 47 days ago — predating Yara's 30-day window and any observable bloom formation. This establishes the suppression as deliberate installation ahead of the thing it is hiding, not reactive cover-up. It also allowed Del to establish the coordinated 6-hour response window when his query triggered a reclassification on the Accord side.
**Next expected**: No further movement on this specific hook; data is in hand and has been analyzed.

---

## HOOK-03 — Station Seven Hardware Log Note
**Type**: dangling hook
**Status**: PAID OFF (Chapter 3)
**Introduced**: Chapter 1
**Last active**: Chapter 3
**Summary**: After discovering her report was deleted, Yara wrote a direct note to Station Seven's embedded hardware log — outside the incident system and the aggregation pipeline. Chapter 2 confirms this record is still in place and outside all affected systems (the deletion mechanism has not reached it). The note references the anomaly, the independent confirmation, the physical samples, and the missing report (EI-2091-447). Whoever is running the suppression may not know it exists or may not be able to reach it. *Chapter 3 payoff*: Yara physically visited Station Seven at night and confirmed her note in the hardware log, undisturbed. She photographed it. The hardware log is confirmed as outside the suppression reach — nobody came to the inlet to erase it. Thread resolved; the note's evidentiary function is now complete.
**Next expected**: No further movement expected; the note is confirmed intact and photographed.

---

## MYST-03 — The "Why" Question
**Type**: mystery
**Status**: RESOLVED (Chapter 4)
**Introduced**: Chapter 2
**Last active**: Chapter 4
**Summary**: At chapter close of Chapter 2, the motive for the suppression is explicitly blank — marked as an empty square. Characters know the what (coordinated suppression across two institutions, 47-day installation, responsive in near-real-time), the when (47 days ago), and the how-far (bloom irreversibility in ~78h). They have no hypothesis on why anyone would install suppression ahead of a bloom, what the suppression is protecting, or who benefits. The empty square is named and acknowledged between Yara and Del. *Chapter 3 advance*: The square now has a line drawn out of it to a name — Rational Innovation Infrastructure Advisory Group, identified through the Altera director's corporate registration. Del wrote "Rational Innovation" on the notepad beside the empty square and drew a single connecting line. The why is no longer purely blank; it has its first shape. The shape is not yet understood. *Chapter 4 resolution*: Motive fully resolved. Rational Innovation is a Technist-aligned advocacy organization pushing certification reform — faster pathways, lower independent-verification thresholds — across three jurisdictions including New Accra. Their argument: the Covenant's caution has calcified into obstruction. The bloom is not a goal; it is a demonstration. The sabotage is designed to produce a visible public failure of New Accra's certified biotech showcase, which Rational Innovation will then cite as proof that the certification system is inadequate. The clean monitoring record is the weapon — built from the Authority's own systems, and when it breaks, the break becomes the argument for deregulation. Del and Yara named it together: "It's a demonstration." The full map — Altera → firmware → bloom → failure-as-argument — was written out on Del's notepad and included in the escalation package.
**Next expected**: No further movement on the "why" mystery; motive is fully in hand. Rational Innovation remains active as named antagonist institution (see CORP-02).

---

## HOOK-04 — Del's Certification Log Pull Tonight
**Type**: dangling hook
**Status**: PAID OFF (Chapter 3)
**Introduced**: Chapter 2
**Last active**: Chapter 3
**Summary**: Del committed to pulling the certification logs for Stations 7, 8, and 9 from the Accord's public archive tonight (end of Day 2). Certification logs are public record and do not require internal access — they are outside the systems that have already responded to investigative moves. They may reveal firmware update records, calibration sign-offs, or maintenance entries that do not match the station's operational history. *Chapter 3 payoff*: Del had the printed certification records on his desk when Yara arrived. The pull revealed a full biotech-node recertification four months ago by Altera Technical Services — a fast single-day visit across all three stations, whose certification reference number matched the anomalous tag in Station Eight and Nine's physical hardware logs. The cert log was the cover for the site visit; cross-referencing Yara's physical-log photographs against Del's records confirmed Altera as the installer. Thread resolved; the hook delivered its investigative payoff.
**Next expected**: No further movement on this specific hook; cert log data is in hand and fully analyzed.

---

## REL-01 — Yara and Del: Alliance in Formation
**Type**: relationship
**Status**: OPEN
**Introduced**: Chapter 1
**Last active**: Chapter 2
**Summary**: Chapter 2 makes the alliance explicit — stated aloud between them, not merely implied by joint action. Del arrived with the historical pull and they worked through the coordinated response window together in his Upper Terraces office. The relationship has moved from complementary professional cooperation under uncertainty to a named, acknowledged off-channel partnership. Their dynamic (his institutional pattern-reading versus her technical specificity) is now operating under the additional pressure of knowing they are being watched. The question of how far Del will go is no longer hypothetical — he is already off official channels.
**Next expected**: Chapter 3 — continued off-channel collaboration; pressure on the alliance increases as bloom clock tightens and options narrow.

---

## REL-02 — Yara and Nwosu: Professional Trust Under Pressure
**Type**: relationship
**Status**: RESOLVED (Chapter 6)
**Introduced**: Chapter 1
**Last active**: Chapter 6
**Summary**: First on-page scene: Yara brought evidence to Nwosu directly; Nwosu rotated her off the investigation under a conflict-of-interest framing. *Chapter 5 advance*: Yara confronted Nwosu directly and alone with three sourced facts; Nwosu did not deny them, spoke in the language of process and panic-management, and stopped mid-sentence on "I told myself —" — arrested deliberately short of confession. Yara formed a private inference (misguided judgment call, not corruption) and chose to hold it as inference only.
**Chapter 6 resolution**: Resolves entirely off-page and through action rather than speech, exactly as the Chapter 5 plant promised. Del reports that Nwosu resigned that morning, "before the review could reach her" — framed internally as someone who "protected the process and the city's name" rather than someone implicated in sabotage. Yara receives this news mid-task (washing inlet mud from her gloves), stops, and lets it land as "the end of that unfinished sentence: not the words she would never say, but the office she had just walked out of." She allows herself "the small private grief of an account closed in the only way it could close. Not triumph. Not vindication." Her one-line eulogy — "She read a log faster than anyone I worked under" — is the entire scene's emotional payload, and Del knows enough not to add to it. The thread closes without ever becoming confrontation-to-confession; the resignation *is* the confession, translated into the only language Nwosu had left to speak it in.
**Assessment**: Earned and exactly on-plan. The Chapter 5 note specified that "I told myself —" should pay off "through what she does next, not through a retroactive confession" — Chapter 6 delivers precisely that, and lets Yara's grief be complicated (cost paid by the person who incurred it; "its own cold and exact kind of justice, and no comfort at all") rather than cathartic. A textbook example of a planted ambiguity resolving through action rather than exposition.

---

## CHAR-01 — Yara's Faith in Institutional Process / Del's Technist Background
**Type**: character beat
**Status**: RESOLVED (Chapter 6) — both halves complete
**Introduced**: Chapter 1 (Yara arc); Chapter 4 (Del subtext activated)
**Last active**: Chapter 6
**Summary**: Chapter 2 brought the arc's first hard turn — Yara's faith in process was falsified by direct evidence, not eroded by suspicion. *Chapters 3-5*: She moved from investigation to off-channel action without abandoning her values, choosing the Compact (an institutional mechanism that still worked) over either submission or vigilantism. Del's Technist-adjacent fluency surfaced in Chapter 4 as a non-confession ("You know this very well") and stalled through Chapter 5, flagged as the single most at-risk planted thread heading into the close.
**Chapter 6 resolution — Yara (systems-are-enough → systems-need-defending)**: The arc completes in two simultaneous registers. Institutionally, her filed deposit triggers the cascade exactly as designed — proof that the system, used correctly through its uncaptured channel, *works*. Physically, she is the one who closes the gap the system's slowness leaves open, walking the manual override by hand because "the suspension had taken neither [access nor competence]." The Council lead's verdict — "we'd be standing in a remediation that doesn't work... we're inside the window because somebody put us inside it" — confirms on-page that Yara's hands, not the institution's machinery, are what made the difference in time. Her arc resolves not into cynicism about systems nor blind faith in them, but into the mature synthesis the book has been building toward: systems are necessary but not sufficient; they must be *defended*, person by person, hour by hour, by people willing to do the unglamorous physical work no one writes songs about. The closing sensor-check scene — "The smell was right and the numbers were right" — returns her to the exact gesture that opened the book, now made true.
**Chapter 6 resolution — Del (Technist arc, closed-but-restrained)**: Receives exactly the small, bounded, unforced beat the bible called for and nothing more. In the walk-back scene, discussing the coming reckoning for Rational Innovation and the review, Del says: "I'm content to let it. That's new for me. I used to want to chase those all the way down myself." Yara notices "something underneath the way he said it... something settled, an account she had never seen the opening of, closing now in the ordinary afternoon. He did not explain it and she did not ask." Her closing line — "You earned letting it" — and his deflection ("Don't tell anyone") let the moment land and pass without ever naming what it was. The thread that has run since Chapter 4 (his too-fluent recitation of Technist talking points) closes on an implication, never a confession — precisely the restraint the character notes called for.
**Assessment**: Both halves earned. Yara's resolution is structurally embedded in the plot's mechanics rather than stated as theme — the thesis is *demonstrated* by what closes the gap, not asserted. Del's resolution is a model of restraint: a single suggestive line and a noticed-but-unspoken shift, leaving the reader to do the work the book has trained them to do all along (the same "competent reader draws the inference" move used for Nwosu and for the inside-actor line in the deposit).

---

## CORP-01 — Altera Technical Services
**Type**: corporate thread
**Status**: CLOSED-BY-HANDOFF (Chapter 6) — deliberate, named, on-page
**Introduced**: Chapter 3
**Last active**: Chapter 6
**Summary**: Altera Technical Services is a single-director firm whose fast recertification visit to Stations Seven, Eight, and Nine four months ago provided cover for installing the masking firmware. *Chapter 4*: mechanism fully confirmed and filed. *Chapter 5*: the certifying analyst, Emil Strand, was named and bounded precisely ("I don't know what he knew. I know what he signed") — the negligence-vs-complicity fork deliberately left open and folded into the deposit as sourced fact. The director-identity sub-thread remained dormant through Chapter 5, flagged as the most exposed loose end heading into the close.
**Chapter 6 resolution — institutional consequence lands**: Del reports that "Altera's certification contracts are frozen — every one, citywide, pending investigation," and that the formal certification review has opened with "Strand's signature... part of the record it's examining... Not our accusation. Their evidence now."
**Chapter 6 resolution — director-identity thread, closed by deliberate handoff**: Del names the gap explicitly and hands it off rather than closing it: "The Altera director — whoever sat on that board and made the contract — that's a name for the Council's investigation now. Subpoena power, financial records, the whole apparatus we don't have and shouldn't try to be. We took it as far as two people on a bench can take a thing honestly. The rest belongs to the process that exists to hold it." He follows with a small, telling character beat — "I'm content to let it. That's new for me. I used to want to chase those all the way down myself" — converting what could have read as an oversight into a stated thematic choice and a character-arc payoff simultaneously (see CHAR-01, Del).
**Assessment**: This is the cleanest possible resolution for a thread that genuinely could not be closed within the book's scope (a corporate director's identity requires subpoena power the protagonists don't have and structurally shouldn't acquire — that would break the book's own argument about amateur overreach vs. institutional process). Naming the limit on-page, in a character's voice, with a reason the audience has been trained to find satisfying (it's now "their evidence," not "our accusation") converts a potential loose end into both a thematic statement and a clean series hook. Recommend flagging this explicitly to the user as the natural Book 2 entry point if the series continues.

---

## CORP-02 — Rational Innovation Infrastructure Advisory Group
**Type**: corporate thread
**Status**: RESOLVED-BY-FOLD-IN (Chapter 6) — antagonist's fate handed to the same ongoing process as CORP-01
**Introduced**: Chapter 3
**Last active**: Chapter 6
**Summary**: Surfaced through Altera's corporate registration as a Technist-aligned advocacy organization pushing certification "reform" — its board-seat connection to Altera's director was the first shape the book's central "why" took. *Chapter 4*: function fully explained (the bloom is a deliberate demonstration designed to argue that certification itself is the problem). Named in the escalation package as the strategy's beneficiary. *Chapter 5*: offstage but reinforced via the Strand connection — "their network runs through Council connections, not just contracting firms."
**Chapter 6 resolution**: Responds to the public deposit with "a denial. Public, fast, lawyered — no involvement, no knowledge, full cooperation," and Del notes precisely why this doesn't matter: "The investigation continues regardless of the denial, which is the part the denial can't touch." The organization's antagonist arc thereby resolves not through confrontation or exposure but through institutional irrelevance — the mechanism it spent the book trying to discredit is the one now grinding forward against it, immune to its rhetoric. This folds cleanly into the same handoff Del names for CORP-01: both threads close into "a process that exists to hold it," not into a final on-page reckoning.
**Assessment**: Satisfying rather than abrupt. A organization whose entire strategy depended on *appearing* more responsive and modern than "calcified" institutional process is defeated by that same process simply refusing to be moved by a denial — a quietly ironic, thematically precise way to close out a Technist-aligned antagonist in a book about why correct, unglamorous process ultimately wins. Del's prior unexplained fluency with their talking points (CHAR-01) receives its restrained final beat in the same scene, tying the corporate and character threads together at the close.

---

## INST-01 — The Open Knowledge Compact
**Type**: institutional / resolution pathway
**Status**: RESOLVED (Chapter 6) — mechanism proven in practice, not just explained
**Introduced**: Chapter 4
**Last active**: Chapter 6
**Summary**: A Covenant-era founding commitment giving ecological monitoring data a public right of access — load-bearing, never repealed, reachable through credentials the Authority could not touch. *Chapter 5*: Del explained the mechanism in full and was explicit about its uncertainty — "the next part is exactly the thing we won't know until we do it." Yara built the full deposit package and armed the upload for 5 AM, unexecuted at chapter close.
**Chapter 6 resolution**: The Compact is vindicated in the most concrete way available to the book — by simply working, on-page, exactly as described, under direct observation. Yara watches the access log fill in real time: independent strangers (a Nairobi researcher, a delta-cities cooperative, a university name) begin pulling and verifying the record within 19 minutes, "each one independent... arriving, with no reason to protect anything, at the same wrong number she had arrived at alone." The "mandatory institutional response" materializes precisely as promised: an automated Technical Council notification fires without requiring a person to choose to notice ("a person didn't have to choose to notice, the mechanism noticed on its own and it can't pretend it didn't"). Del frames the thematic resolution directly: "Correct process is what almost killed us... And correct process is also what saved us — a different door, the same founding commitment to doing things right, and it can't be un-filed. Same machine. We just used the part of it they forgot was a machine."
**Assessment**: Earned and thematically central — this is the book's argument made literal. The same institutional machinery that enabled the suppression (by being slow, careful, and exploitable) is shown to contain, in its own founding charter, an uncapturable safeguard. The mechanism's uncertainty (explicitly named in Ch. 5 as unknown even to Del) makes its on-page success feel like a discovery rather than a guarantee — exactly the right note for a climax built on institutional trust rather than violence or revelation.

---

## INST-02 — The Inside Actor
**Type**: mystery / institutional
**Status**: RESOLVED (Chapter 6) — confirmed through action, never through confession
**Introduced**: Chapter 4
**Last active**: Chapter 6
**Summary**: Two access vectors enabled the suppression: Altera's door at the stations (identified and named) and an interior door inside the Authority — someone with Director-level access deleted report EI-2091-447 and imposed Yara's rotation. *Chapter 5*: Yara confronted Nwosu directly; Nwosu didn't deny the facts, rationalized in procedural language, and stopped mid-sentence on "I told myself —." Yara formed a private inference (misguided judgment call, not corruption) and wrote the deposit's inside-actor line as sourced fact only — no name, no accusation, left for a competent reader to complete.
**Chapter 6 resolution**: Confirmed through Nwosu's resignation rather than any direct statement. The internal framing Del relays — "she protected the process and the city's name... she held a flag back, judged it her call to make, and let the process run instead of the alarm" — matches Yara's private inference precisely, without ever crossing into the on-page confirmation that would have flattened the ambiguity into melodrama. Yara explicitly registers that "Nwosu had not confessed... and the shape was all the answer there would ever be, and Yara found she did not need more than the shape." The mystery resolves into certainty for the reader and the protagonist alike — but it does so through *behavior* (a resignation, a timing, a framing) rather than through speech, which is the exact mechanism the Chapter 5 plant called for.
**Assessment**: A model payoff for a deliberately incomplete plant. "I told myself —" finishes not with words but with "the office she had just walked out of" — a genuinely elegant piece of structural patience that trusts the reader to complete a sentence the character never finishes speaking.

---

## INST-03 — The Armed Deposit / The 5 AM Upload
**Type**: subplot / institutional climax mechanism
**Status**: RESOLVED (Chapter 6) — fires and produces full institutional cascade
**Introduced**: Chapter 5
**Last active**: Chapter 6
**Summary**: Yara spent the evening of Chapter 5 assembling the full Compact deposit package and armed the public upload for 5 AM — chosen for low traffic, so the record would be pulled and verified by independent strangers before anyone who might want to stop it woke up. The chapter ended with the deposit "armed but not yet executed... a single action between the truth and the public record," at ~22h remaining on the bloom clock.
**Chapter 6 resolution**: Fires exactly on schedule, with no drama in the mechanism itself — "the field that had read *armed* for seven hours simply read something else... That was all." What follows is the full cascade the book has been building toward: independent verification within 19 minutes (strangers in Nairobi, the delta cities, a university, all reaching the same number Yara reached alone "in the reeds three days ago"); an automated Technical Council notification that "a person didn't have to choose to notice"; Altera's certification contracts frozen citywide; the certification review formally opened with Strand's signature placed in the record; Rational Innovation's public denial (irrelevant to the process now in motion); and Director Nwosu's resignation. Del's secondment is quietly restored overnight — "somebody is trying to get ahead of this... not far enough." Every consequence promised by INST-01's mechanism explanation lands, in order, on-page, within a single morning.
**Assessment**: A clean, well-earned climax payoff. The chapter resists the temptation to make the upload itself dramatic (it reads "exactly like every other confirmed transaction she had run in ten years of correct work") and instead lets the *consequences* carry the climax's weight — which is correct for a book whose thesis is that the real drama of institutional change is procedural, distributed, and slow-building rather than a single cinematic confrontation. The two parallel clocks (upload/response vs. bloom chemistry) cross with exactly the narrow margin the book needed: the institutional response *worked*, but not fast enough on its own — see THREAT-01 and MAIN-01 for how Yara's manual intervention closes the remaining gap.
