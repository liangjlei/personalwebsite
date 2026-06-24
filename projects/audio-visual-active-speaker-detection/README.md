# A Comparative Study of Audio–Visual Active Speaker Detection in Unconstrained Scenes

**Jinglei Liang** · Survey / Technical Report, 2026

## Abstract
"Who is speaking to me?" is a prerequisite for natural human–robot dialogue in
crowds. We survey three audio–visual paradigms from coarse to fine and select a
deployable real-time pipeline.

## Paradigms compared
1. **Semantic audio–visual segmentation** — pixel-level sounding-object masks.
2. **Audio–visual instance segmentation** — per-instance sounding objects.
3. **Active speaker detection** — per-face speaking/not-speaking over time.

## Findings
A two-stage **detect → track → ASD** pipeline best matches the in-the-wild
exhibition setting: model **< 20 MB**, real-time throughput, and robust to
multiple candidate faces. We benchmark all three along task alignment, accuracy,
latency, and deployability, and motivate the final design choice.

## Notes
Reproductions use publicly described model families; deployment data is omitted.
