# Neural Motion Retargeting for Affective Whole-Body Teleoperation

**Jinglei Liang** · Technical Report, 2026

## Abstract
An affective human–robot interaction system following a
*perceive → infer affect → generate motion → drive hardware* loop. The core
contribution is replacing analytic inverse-kinematics retargeting (which needs a
per-session T-pose calibration) with a learned model that maps wearable-IMU
streams directly to robot motion.

## Method
- **Transformer retargeting model** — 4 layers, ~1.0 M parameters, mapping a
  60-D IMU signal to a 10-D motion encoding.
- **Two-stage perception cascade** — a fast detector front-end followed by a
  vision–language stage for affect/intent, dropping per-frame latency from
  **1.5 s → ~920 ms**.
- **Calibration-free operation** — no T-pose reset between users.

## Outcome
Markedly smoother and more robust motion than the analytic IK baseline, with
lower latency and no manual calibration step, enabling expressive real-time
teleoperation.

## Notes
Specific robot platform and capture hardware are omitted by request.
