# Assets & Content Checklist

The site is fully built and live-ready with placeholders. To finish it, supply the
items below. Search the code for the marker text in `( )` to find where each goes.

## 1. Identity & contact  (required)
- [ ] **Preferred display name** — currently `Jinglei Liang`. Confirm, or switch to
      e.g. `Jinglei (Amy) Liang`. (`index.html`: `<title>`, `.nav-name`, `<h1>`, footer)
- [ ] **Email** — replace `YOUR_EMAIL@example.com` (2 places: hero + contact section)
- [ ] **Google Scholar URL** — replace `href="#"` next to "Google Scholar" (or delete the link)
- [ ] **LinkedIn URL** — replace `href="#"` next to "LinkedIn" (or delete the link)
- [ ] **CV PDF** — drop a file at `assets/CV_Jinglei_Liang.pdf` (or remove the CV link)
- [ ] GitHub is already set to `github.com/liangjlei` — confirm it's right.

## 2. Photos  (1 required, rest optional)
- [x] **Portrait** — `assets/profile.jpg` already placed (your 职业照).
- [ ] **5 project thumbnails** (4:3, ~480×360+) replacing the navy placeholders in
      `assets/projects/`. Good choices:
  - `perception-pipeline` → the ASR→VAD→NLU→VLM→planner→TTS block diagram
  - `pi05-libero` → a LIBERO success-rate bar chart or a rollout filmstrip
  - `teleop-retargeting` → robot mirroring a human pose / IMU→pose figure
  - `asd-survey` → annotated multi-face frame with the "speaking" box highlighted
  - `calibration` → AprilTag / checkerboard board or a hand–eye residual plot
  > Any screenshot from your 8 PDFs works. Crop to ~4:3. PNG/JPG both fine —
  > if you keep the `.svg` names, just overwrite; otherwise update the `src=` paths.

## 3. Data / figures worth adding  (recommended, high academic value)
These turn the page from "claims" into "evidence":
- [ ] **π0.5 / LIBERO bar chart** — per-suite success (Spatial / Object / Goal / Long),
      vanilla-LoRA vs your recipe. You already have the numbers (92.2→94.2, Long 88.8).
- [ ] **Ablation table image** — the 5-component table (SLP/LIP/TAE/EMA/FCR, ΔMean).
      Either as a figure or rebuilt as an HTML table — tell me and I'll add it.
- [ ] **On-robot results** — the join-test table (ASR+intent 95%+, nav 94.6%,
      grasp 78.0%, place 80.4%, lateral-reach 95.0%, scan 100%). Currently summarized
      in the "Selected Results" table; say the word to expand it into its own section.
- [ ] **Latency / compute deltas** — partial latency 150–300 ms, VAD −86%, frame
      1.5 s → 920 ms. Good as a small before/after chart.

## 4. Links  (optional but strong for an academic page)
- [ ] Per-project `report` / `code` / `demo video` links (currently `href="#"`).
      Public GitHub repos, a hosted PDF, or a YouTube/Bilibili demo clip.
- [ ] A short **demo video** (even 20–30 s of the robot completing a place task) is
      the single most compelling thing you can add.

## 5. Optional sections I can add on request
- **Education** (degree, school, dates) — not in the current report; send me the line.
- **Publications** — if/when you have papers or arXiv preprints.
- **Bilingual toggle** (EN / 中) like the reference site — say the word.

---
### Preview locally
```bash
cd personalwebsite && python3 -m http.server 8000
# open http://localhost:8000
```
### Publish (GitHub Pages)
Settings → Pages → Branch: `main` → `/ (root)`. Then commit & push.
