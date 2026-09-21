# IGNIS Fire Classifier — weakly-supervised fire-behavior classification

> Part of the **IGNIS** platform — NASA Space Apps Challenge 2026, challenge #9
> *Harmonization of MODIS and VIIRS Hot Spots*. **Private during judging.**

Classifies each FIRMS hotspot detection into ISOLATED / SCATTERED / EMERGING / ESTABLISHED / MEGAFIRE from per-detection features (FRP, confidence, diurnal phase, sensor family, multi-scale local density). Labels are weak supervision from the IGNIS DBSCAN complex segmentation engine (the app's Fire Cluster Lab). Temporal holdout: accuracy 0.75, macro-F1 0.55 on the fully held-out day 2026-09-20.

## Contents
- `train_classifier.py` — full reproducible training pipeline (real NASA FIRMS data)
- model artifacts (scikit-learn joblib bundles) + `metrics.json`
- `LICENSE` — MIT

## Hugging Face
The same model, with the full model card, lives at
**https://huggingface.co/Nabidnur/ignis-fire-classifier** (private; request access or see the main repo).

## Main project
https://github.com/Hisernberg/ignis-spaceapps2026 — live app:
https://ignis-spaceapps2026.vercel.app

## Provenance
All training data derives from NASA FIRMS active-fire detections (public domain),
harmonized across MODIS (Terra/Aqua) and VIIRS (S-NPP/NOAA-20/NOAA-21) by the IGNIS
pipeline. No synthetic data is used for supervised labels.
