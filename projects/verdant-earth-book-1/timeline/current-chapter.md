# Timeline — Current Chapter

## Chapter in progress
Chapter 2 (not yet written)

---

## Chapter 1: Station Seven — Completed events

**Story date**: Day 1, 2091. (All events within a single calendar day, pre-dawn to evening.)

### Pre-dawn — Station Seven, eastern inlet
- Yara Osei walks the maintenance path to Station Seven before sunrise, field kit over one shoulder
- She smells the biofilter before touching anything — the smell is correct (green, mineral, clean fungal warmth)
- On the manifold port: cyanobacteria load reading is slightly elevated; mycorrhizal coherence index reads nominal — the two readings cannot both be true
- She runs the sweep twice more, including a hard-line diagnostic, eliminating wireless error as a cause
- She takes three physical samples from the inlet outflow, hand-labels each: **EI-S7-2091-0605**; stows them in the field kit cold pocket
- She adds a routine flag to the station log: *"Anomalous sensor correlation. Manual check required. Samples taken for lab."*

### Transit stop — morning commute
- On the bench at the transit stop, Yara reviews Station Seven's last thirty days of raw data
- Finds the same impossible pairing (cyano up, coherence flat) on four separate occasions over three weeks; each below the notification threshold; none followed up

### Morning — Water Authority building, mid-terrace office
- Yara submits samples EI-S7-2091-0605 to the lab queue; standard 24-hour turnaround; chain of custody logged; counter receipt retained
- At her terminal: she pulls a comparative grid for all eight eastern inlet stations, thirty days of raw data
- Stations 7, 8, 9 (all eastern-inlet, estuary-adjacent) show the same intermittent pattern; the other five are clean
- She pulls the regional summary feed for comparison: all three affected stations read fully nominal in the summary — the elevations are not there at all
- She traces one anomalous reading through the aggregation algorithm step by step: the elevated value goes into normalization normal, then somewhere between normalization and regional roll-up it is reclassified into the noise floor — smoothed flat, not deleted
- She repeats with two other readings; same result; checks other stations: the reclassification only affects Stations 7, 8, 9
- Working hypothesis formed: *aggregation algorithm error — systematic misclassification of this cyano signature*

### Mid-morning — same office
- Yara writes and submits formal anomaly report to Director Adaeze Nwosu's queue
- Report titled: *Preliminary Anomaly Report: Eastern Inlet Stations 7–9, Recurring Sensor Correlation Discrepancy*
- Report reference: **EI-2091-447**; system confirms receipt: *"Routed to Director Nwosu for review. Estimated review window: 48 hours."*
- Yara writes confirmation number EI-2091-447 in her paper field notebook
- Decides not to escalate to urgent flag: "an urgent flag on a medium-priority anomaly was a way of teaching people to ignore your urgent flags"

### Afternoon — same building
- Tomas stops at the doorway about a maintenance window on Station Twelve; Yara gives him the correct procedure
- Plans two more field sites before end of shift

### End of shift / dusk — external staircase landing, Water Authority building
- Del Marchetti arrives unannounced at Yara's office
- He has been on the inlet monitoring brief for the Accord — independent sensors, separate network
- His raw Accord feed shows the same three-station anomaly (Stations 7, 8, 9); the Authority summary that his dashboard reads shows all three as nominal
- He has been flagging it up his own chain; someone checks the summary; summary says nominal; he is dismissed
- They compare raw feeds side by side on the staircase landing
- Del's independent hardware sees the same pattern — the same impossible sentence, different network, different equipment
- A calibration fault in Authority equipment cannot be the whole story: two independent sensor networks don't drift the same wrong way
- Del identifies the structural implication: *"Whatever's flattening these readings, it's happening before the data leaves the Authority's system."*
- Neither says the word *deliberate*
- They agree on next steps: Del will pull the Accord's full historical feed for all three stations, sixty days; Yara will run the full comparison
- Del departs

### Evening — Yara's apartment courtyard
- Yara walks home along the public wetland path; pauses at the overlook; can see Station Seven as a small lit post in the reeds
- At home, checks lab queue: samples EI-S7-2091-0605 still pending (nine hours elapsed; fifteen hours remaining)
- Opens incident management system to attach a note about Del's observation to the report
- **Report EI-2091-447 is not in her queue.** No record found by number, by date, by station reference, or in her submission history. The system holds no record that she filed anything today.
- She has the local draft on her personal system and the confirmation number in her paper notebook
- She does not panic; she acts within the tools still available to her
- She writes an urgent flag directly to **Station Seven's embedded hardware log** — outside the incident system and the aggregation feed: *"Anomaly pattern confirmed across independent sensor networks. Physical samples pending, lab ref EI-S7-2091-0605. Prior report ref EI-2091-447 not appearing in system — investigating."* Saved locally and to the station hardware.
- She refreshes the queue one more time: **No record found**

---

## What changed in Chapter 1

| What changed | Details |
|---|---|
| Anomaly discovered | Stations 7, 8, 9; cyano elevation + flat coherence; absent from summary feed |
| Physical samples collected | EI-S7-2091-0605; in lab queue; 24h turnaround |
| Report filed | EI-2091-447; submitted, confirmed, then deleted |
| Paper record created | Notebook: confirmation number EI-2091-447 |
| Hardware log note created | Station Seven embedded log; outside the incident system |
| Del Marchetti engaged | Independent Accord data confirms same pattern; agreed to pull 60-day history |
| Official record state | Report deleted; no official record exists that Yara filed anything |
| Bloom clock | Running; ~96 hours from chapter start |
