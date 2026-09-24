# TRU-FACT is the next step after the Mini2P pain pipeline

## User message that triggered this

Where is the whole pipeline for Mini2P pain assay, and is the current stage later alignment with TRUFACT ex vivo?

## Paper IDs / links

- Wang, Jiang, Sun et al., *bioRxiv* 2026, TRU-FACT. https://doi.org/10.64898/2026.04.28.719500
- Earlier: [2026-09-14_trufact-ntsr1-pain-assay-email.md](2026-09-14_trufact-ntsr1-pain-assay-email.md)

## Full summary

Yes. The in vivo Mini2P pain+OF pipeline is in `pain_2plane_pipeline\` (working copy on OneDrive Desktop). Raw data + z-stack are on `D:\`. That analysis is finished (keep-mask, scoring, pain-DOWN cell IDs). The remaining step is TRU-FACT: register those same cell IDs to postmortem HCR using the z-stack / max-Z FOV as the in vivo anatomical reference.

## Conversation recap

- User asked for pipeline location and confirmation that what remains is ex vivo TRU-FACT alignment.
- Answered with code, data, wiki, and z-stack paths. Wiki updated locally; no wiki push.
