# Confocal GCaMP slices vs the two in vivo averages

## User message that triggered this

Change MATLAB paths now that the disk is `I:\`. Align confocal to the two attached in vivo averages. Be ready for Cellpose and Soma-print, but show confocal GCaMP max projections first so the slices can be chosen.

## Paper IDs / links

- Wang, Jiang, Sun et al., *bioRxiv* 2026, TRU-FACT. https://doi.org/10.64898/2026.04.28.719500
- Prior entry: [2026-09-23_trufact-confocal-prealign-not-somaprint.md](2026-09-23_trufact-confocal-prealign-not-somaprint.md)

## Full summary

The two alignment targets are the pain-session plane averages `AVG_CellVideo #1.tif` and `#2.tif` (ETL 65 µm and 15 µm, 50 µm apart), not a single full-volume max. The paper matches each in vivo plane to a thin ex vivo GCaMP slab (about 3 slices), then affine, then Cellpose on GCaMP, then Soma-print. Slice contact sheets were written. Cellpose is scripted and not run. Soma-print is held until two slice windows are chosen.

## Conversation recap

- Drive letter in the pipeline scripts was updated from `D:\` to `I:\`.
- User still has to pick which confocal slices match each of the two in vivo images.
