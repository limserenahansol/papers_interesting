# Open-field center vs corner neurons (for CEA-Ntsr1 mini2p)

## User message that triggered this

New 2026-09-11 mini2p sessions (open field + pin/heat pain). Asked to cluster neurons as “center” vs “corner” from open-field location, and to search papers.

## Paper IDs / links

- Ziv et al., *Nat Neurosci* 2013 — long-term CA1 place codes; occupancy-normalized rate maps in open fields. https://pmc.ncbi.nlm.nih.gov/articles/PMC3784308/
- Eliav et al., 2021 — dorsal CA1 multi-scale maps; fields split as wall / corner / middle. https://par.nsf.gov/servlets/purl/10294326
- Sun et al., *Nature* 2024 — subicular neurons encode concave/convex corners; ~4–7% corner cells vs ~0.6% in CA1. https://doi.org/10.1038/s41586-024-07139-z
- Cacucci / Rochefort-range spatial information in freely moving mice (cited in Frontiers 2021 floating-track paper). https://www.frontiersin.org/articles/10.3389/fncel.2021.618658/full

## Summary given in chat

Open-field location coding is well established in hippocampus (occupancy-normalized place fields; wall/corner vs middle over-representation). Explicit **corner cells** are strongest in **subiculum** (Sun 2024), not CA1. CEA-Ntsr1 cortical imaging should be treated as a **location-preference cluster** (center vs corner occupancy-normalized ΔF/F, k=2), not as classical place cells.

## Conversation recap

- Integrated SBI-553 dual-view scoring into mini2p pain pipeline.
- EXTRACT first on both 2026-09-11 sessions.
- Open-field analysis: track MiceVideo2, occupancy-normalize, k=2 center vs corner.
