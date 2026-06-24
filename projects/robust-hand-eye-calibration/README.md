# Robust Hand–Eye Calibration via SE(3) Maximum-Likelihood Estimation

**Jinglei Liang** · Open-source toolkit, 2026

## Abstract
A minimal but complete toolkit for camera intrinsics and hand–eye extrinsics
calibration, supporting both **eye-on-base** (fixed, third-person) and
**eye-on-hand** (wrist-mounted) configurations via the classic AX = YB
formulation, with real-time 3D visualization for at-a-glance verification.

## Method
- **Targets:** checkerboard (intrinsics) and AprilTag 36h11 (extrinsics).
- **Estimator:** maximum-likelihood estimation with Gauss–Newton optimization on
  the SE(3) manifold under a Huber robust loss, reaching millimeter-level
  residuals.
- **Visualization:** a live viewer overlays the estimated camera pose on the
  robot model, making misalignment obvious before deployment.

## Reliability
The toolkit underpinned a long-running automated assembly demonstration:
**20/20** consecutive successful runs across **10+** public showings.

## Repo layout (reference)
```
intr_calib.py     # camera intrinsics
extr_calib.py     # hand–eye extrinsics (AX = YB)
cameras.py        # capture abstraction
outputs/          # intrinsics.yaml, extrinsics.yaml
```

## Notes
Robot/camera model identifiers and internal paths have been removed.
