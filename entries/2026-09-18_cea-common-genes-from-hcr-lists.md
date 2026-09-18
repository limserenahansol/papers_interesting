# Which listed genes are common in CEA?

## User message that triggered this

Among HCR/stock gene lists (GCaMP8m…Nr1; Xiaochun Pdyn…Nts; ordered-new Krt14…Tshz2), which are very common in CEA?

## Paper IDs / links

- O’Leary et al., *eLife* 2023 — multimodal CEA cell types/projections. https://elifesciences.org/articles/84262
- Yao et al., *Nature* 2023 — Allen WMB atlas; CEA-BST subclasses 079/082/083. https://doi.org/10.1038/s41586-023-06812-z
- Local % detecting cells: `Genelist_analysis_WMB/v3/outputs/subclass_markers_gse283418/Subclass_Discriminating_Markers_long.csv` (BMAp dissection, Allen subclasses)

## Full summary

Among the user’s lists, the genes that actually cover a large fraction of CEA neurons are **Vgat (Slc32a1)**, then **Calb1, Penk, Pdyn, Sst**, then **Tac1, Pnoc, Ntsr1, Crym, Drd1, Drd2, Nts**. Xiaochun’s opioid/amygdala stock is the CEA-relevant set. The first list is mostly cortex/indicators; “Ordered new” is mostly not CEA. **Prkcd is the classic common CEA type marker and is missing from all three lists.** Atlas % are from CEA-BST subclasses in a BMAp dissection, not a spatial CEA mask.

## Conversation recap

- Ranked genes by Allen subclass detection % (079 n=4675, 082 n=6966, 083 n=214) plus O’Leary/Yao literature.
- Stated limitations: pan-neuronal genes (Malat1, Fos, GCaMP) are common everywhere, not CEA-specific.
