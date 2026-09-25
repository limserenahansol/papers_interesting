# Click matcher for in vivo and confocal, before Soma-print

## User message that triggered this

Make a tool that shows in vivo and confocal (max or mean) together, with clicks to mark the same neuron in both windows, and an option to rotate.

## Paper IDs / links

- Wang, Jiang, Sun et al., *bioRxiv* 2026, TRU-FACT. The paper's pre-alignment is manual control points (`cpselect`) before Soma-print. https://doi.org/10.64898/2026.04.28.719500

## Full summary

`trufact_click_match.py` opens two panels. The left is the pain-session average (max or mean, video 1 or 2). The right is confocal GCaMP (one slice, 3-slice max, or the whole stack). A pair is one click on the left and one click on the right. Either image rotates in 90° steps and existing points move with it. Saved pairs are the affine control points. Soma-print is not run.

## Conversation recap

- Starts on video 2, 90° CCW, confocal slice 34, because that was the best score at 90°.
- Keys: i/c rotate, v video, m max/mean, [ ] slice, p view, u undo, s save.
