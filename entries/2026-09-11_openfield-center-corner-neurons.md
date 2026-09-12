# Open-field center vs corner neurons (for CEA-Ntsr1 mini2p)

## User message that triggered this

(2026-09-11, follow-up) Manual scoring for pain video with SBI-553; open-field neurons by mouse location (center vs corner, search papers); pain classes pin / heat / non-responsive / behavior-responsive (6 behaviours); raw, z-score, and event-locked ΔF/F. Do this in parallel without interrupting another MATLAB EXTRACT session.

Earlier same day: cluster neurons as center vs corner from open-field location, and search papers.

## Paper IDs / links

- Ziv et al., *Nat Neurosci* 2013 — long-term CA1 place codes; occupancy-normalized rate maps in open fields. https://pmc.ncbi.nlm.nih.gov/articles/PMC3784308/
- Eliav et al., 2021 — dorsal CA1 multi-scale maps; fields split as wall / corner / middle. https://par.nsf.gov/servlets/purl/10294326
- Sun et al., *Nature* 2024 — subicular neurons encode concave/convex corners; corner score −1 (centroid) to +1 (corner); ~7% corner cells in square vs ~0.6% in CA1. https://doi.org/10.1038/s41586-024-07139-z
- Poulter et al., *Nat Commun* 2024 — subiculum boundary vector cells; environment geometry reshapes BVCs. https://doi.org/10.1038/s41467-024-45098-1
- Cacucci / Rochefort-range spatial information in freely moving mice. https://www.frontiersin.org/articles/10.3389/fncel.2021.618658/full

## Full summary

Open-field location coding is well established in hippocampus using **occupancy-normalized** rate maps (Ziv 2013). Fields are often split as wall / corner / middle (Eliav 2021). Explicit **corner cells** (Sun 2024) are a subiculum phenomenon (~7% in a square, almost none in CA1); they use a corner score from −1 at the centroid to +1 at a corner, plus shuffle and stability criteria. Poulter 2024 shows subiculum boundary-vector cells also depend on environment geometry.

For CEA-Ntsr1 cortical mini2p this is implemented as a **location-preference cluster**, not a place-cell claim: track the mouse inside the bright arena, take occupancy-normalized mean ΔF/F in a center disk vs the four corner regions, then k-means (k=2). A Sun-style corner score is stored as a continuous extra column.

Pain analysis (separate): SBI-553 dual-view scoring (2 reflex + 4 affective; this session key 1 = pin, key 2 = heat). After scoring, each cell gets raw ΔF/F, z-scored traces, and event-locked ΔF/F with F0 = mean of [−3, −1] s vs post [1, 3] s. Classes: pin-responsive, heat-responsive, behavior-responsive (any of the six), non-responsive (none of those).

## Conversation recap

- User asked to proceed with scoring + OF place + pain classification without interrupting another MATLAB using the same codes/data.
- EXTRACT left untouched. Analysis writes to `output/analysis_place/` and `output/analysis_pain/`; scoring to `output/scoring/`.
- OF video is top-down of a bright plastic box with a dark mouse and a mini2p tether; tracking is cropped to the bright floor so the cable is not treated as the mouse.
- Scoring GUI launched as a **new** MATLAB desktop (`RUN_scoring_ceantsr1`). Event-lock runs after `ScoringAB_*.mat` appears.
