# How TRU-FACT aligns confocal to in vivo (before Soma-print)

## User message that triggered this

Channel map for `I:\Hansol_BLA_TRUFACT_test1_Image1_z55_6ch.tif`: 405 DAPI, 488 GCaMP, 546 Crh, 594 Vipr1, 646 Ntsr1; ignore cyan. Can Cellpose quantify Vipr1 ∩ GCaMP ∩ Ntsr1? How does the TRU-FACT paper align confocal to in vivo, and how to superimpose the mini2p projection in `pain_2plane_pipeline`? Do not start Soma-print.

## Paper IDs / links

- Wang, Jiang, Sun et al., *bioRxiv* 2026. https://doi.org/10.64898/2026.04.28.719500
- Hands-on notes: protocol §§11.2–11.5 and §16. Local PDF already in [files/2026-09-14_trufact.pdf](../files/2026-09-14_trufact.pdf)

## Full summary

TRU-FACT does not overlay the images by intensity warping. Order: (1) GCaMP-488 is the shared fiducial; (2) pick the ex vivo z slab that matches the in vivo plane and max-project only a few slices (paper recipe: 20×, 2 µm z, project n=3); (3) rotate/crop in Fiji to the in vivo FOV; (4) affine (`cpselect` / `fitgeotrans` or Icy) on vessels and a few obvious GCaMP cells; (5) Cellpose **both** maps; (6) only then Soma-print (m≈15, n≈10). Molecular labels are mean intensity inside the Cellpose mask, not a separate segmentation per gene.

This confocal stack is 512×512 × 55, 1.264 µm/px, 3 µm z (~647 × 165 µm). Mini2p functional FOV is 512×440 at 0.898 µm/px (~460 × 395 µm). A full-volume max of either side is the wrong overlay. Cellpose is the right counter, run once on GCaMP. It was not installed here, so no cell count was invented. Filename says BLA; the in vivo pipeline is CEA — do not assume they are the same field until landmarks match.

## Conversation recap

- User gave dye→channel map and asked for Cellpose triple-positive counts plus the paper’s alignment, explicitly not Soma-print.
- Pre-alignment contact sheets written under `trufact_prealign_20260923/`. `D:\` was offline, so the functional `AVG_CellVideo` was not opened.
