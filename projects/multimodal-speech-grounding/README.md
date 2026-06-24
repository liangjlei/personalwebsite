# Streaming Multimodal Speech Grounding for Real-Time Human–Robot Interaction

**Jinglei Liang** · Technical Report, 2026

## Abstract
We present an end-to-end voice-to-action stack that lets a mobile service robot
*hear*, *understand*, and *act* on spoken commands in noisy, far-field
conditions. The system grounds natural-language references to physical objects
by fusing streaming speech recognition with a vision–language perception stage,
and executes the resulting intent through a motion planner — all on device, with
latency low enough for fluid turn-taking.

## Pipeline
```
mic PCM → VAD (×3 gate) → streaming ASR → NLU → VLM / open-vocab segmentation
        → motion planner → TTS
```
Every stage is a decoupled ROS2 node coordinated by a state-machine
orchestrator, so components can be swapped or scaled independently.

## Contributions
- **Streaming ASR path** with stable 150–300 ms partial hypotheses for
  responsive barge-in and endpointing.
- **Three-stage voice-activity gate** that cuts downstream inference compute by
  **86%** and triples far-field recall under ambient noise.
- **Vision–language object grounding** replacing brittle HSV color heuristics,
  eliminating referent mis-rejections (e.g. "pick the blue one").
- **State-machine orchestration** that keeps a live, multi-stage interaction
  stable across hundreds of trials.

## Results
| Metric | Result | Setting |
|---|---|---|
| ASR + intent accuracy | 95%+ | quiet & noisy, on-robot |
| Streaming partial latency | 150–300 ms | cloud streaming path |
| VAD inference compute | −86% | three-stage gate |
| Far-field recall | ×3 | vs. single-stage VAD |

## Notes
Hardware identifiers, internal service endpoints, and proprietary data sources
have been omitted. Reported numbers come from on-robot evaluation logs.
