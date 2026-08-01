# 👋 Hi, I'm Davide Deplano

🎓 BSc in Applied Computer Science and Data Analytics — University of Cagliari, July 2026  
🎯 MSc Computer Engineering, Cybersecurity & AI (CyberAI) — UniCa, from September 2026  
📍 Cagliari, Sardinia, Italy | 🌍 Open to remote and international opportunities  
📧 [davide.deplano@gmail.com](mailto:davide.deplano@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/davide-deplano-a331a812a)

---

## 🛰️ Research & Internship Project

**Technosignature Search at INAF – Sardinia Radio Telescope** (9 months)

Adaptation and validation on real SRT data of a multi-stage anomaly-detection pipeline for
SETI-like radio signals, based on the methodology of Pardo et al. (AJ 2025). Candidates pass a
density-based pre-filter (cross-correlation features, UMAP embedding, per-category KDEs) trained
on simulated cadences, are then scored by a bagged-GMM frequency filter and an ON/OFF similarity
metric in UMAP space, and ranked to prioritise human inspection.

Main contribution: an **NCC-max cross-correlation extractor** tolerant to frequency drifts,
validated against a Pearson baseline. Two exploratory branches — a Keras Tuner–optimised
convolutional autoencoder and a Random Forest on handcrafted ON/OFF contrast features — were also
implemented; the Random Forest result is a documented negative one, high accuracy on the synthetic
domain and indistinguishable score distributions on real data, which quantifies the
simulation-to-reality gap of the training set.

Built as a reproducible framework: YAML configuration, pluggable filter interface, UML
documentation, memory-mapped training for 1.28M synthetic cadences, and an interactive UMAP
reverse-search tool for cluster and RFI investigation.

🔗 [srt-anomaly-detection](https://github.com/DavideDeplano/srt-anomaly-detection)   

---

## 🧩 Selected Projects

### [🛡️ deepfake-detection-cnn-adversarial](https://github.com/DavideDeplano/deepfake-detection-cnn-adversarial)
Binary CNN deepfake detector (RGB vs grayscale) evaluated under PGD white-box and transfer
black-box attacks, hardened with PGD adversarial training (Madry et al., 2018).

| Model | Clean | PGD ε=0.01 | PGD ε=0.02 |
|---|---|---|---|
| RGB, undefended | 97.9% | 62.1% | 9.6% |
| RGB, adversarially trained | 99.2% | 87.9% | 41.3% |
| Grayscale, undefended | 98.3% | 71.7% | 20.8% |
| Grayscale, adversarially trained | 97.9% | 85.4% | 47.1% |

Imperceptible perturbations collapse undefended detectors from ~98% to ~62–72%; adversarial
training recovers ~26 points on RGB at ε=0.01 at negligible cost in clean accuracy. At ε=0.05
the defense no longer generalises — both models still collapse.

### [🔐 cyber-intrusion-detection](https://github.com/DavideDeplano/cyber-intrusion-detection)
Network intrusion detection on KDD Cup 1999 (10% subset), comparing supervised and
unsupervised approaches with hyperparameter tuning and feature interpretation.

Random Forest F1 ≈ 0.999 · One-Class SVM F1 ≈ 0.994 · MLP F1 ≈ 0.990 · VAE F1 ≈ 0.969

### [📊 credit-default-risk-ml](https://github.com/DavideDeplano/credit-default-risk-ml)
Credit card payment default prediction on the UCI *Default of Credit Card Clients* dataset
(22% positive class). Random Forest, KNN, Naive Bayes and two custom classifiers, each evaluated
across five preprocessing configurations (scaling, variance-threshold selection, SMOTE
balancing), with GridSearchCV tuning optimised for F1 on the minority class.

Random Forest is the strongest model: accuracy 0.82, ROC-AUC 0.76. SMOTE raises recall on the
default class from 0.37 to 0.47 (F1 0.50) at the cost of precision — the recall/precision
trade-off that matters in credit risk.

### [🐠 aquarium-adventures](https://github.com/DavideDeplano/aquarium-adventures)
Software-engineering project (with Sebastiano Seu): a composable data pipeline over simulated
aquarium sensor data, computing per-tank stress metrics and statistics on large volumes.

Built as production-style Python rather than a script: `uv` with a lockfile for reproducible
installs, unit and acceptance test suites under `pytest`, static typing checked with `mypy`,
linting with `ruff`, pre-commit hooks, and a GitHub Actions workflow running lint, type-check and
tests on every push and pull request. Optional run logging to Weights & Biases. Designed from UML
use-case, class and sequence diagrams.

Performance work with the **Scalene** profiler: the hot path `pairwise_stress_function` is
JIT-compiled with Numba and parallelised with Joblib, bringing `computations.py` down to 14.3% of
total runtime (966 ms of 6.765 s); the interactive profiling report is committed to the repo.
Data handling uses Polars.

---

## 🔧 What I work on

**Machine Learning & Deep Learning** — CNNs, autoencoders, VAEs, GMMs, manifold learning
(UMAP), tree-based and kernel methods. Supervised and unsupervised pipelines on real data.

**AI Security** — Adversarial robustness of deep models: evasion attacks (PGD, transfer) and
adversarial training defenses.

**Data Science** — End-to-end pipelines: preprocessing, feature extraction, anomaly detection,
evaluation on imbalanced data.

**Software Engineering** — Modular Python packages, configuration-driven design, unit and
acceptance testing with pytest, static typing (mypy), linting (ruff), CI with GitHub Actions,
UML design documentation, and profiling-driven optimisation.
---

## 🛠️ Stack

`Python` `TensorFlow/Keras` `scikit-learn` `imbalanced-learn` `UMAP` `pandas` `NumPy` `Git` `SQL` `C`

---

⭐ Feel free to explore my pinned repositories or connect on
[LinkedIn](https://www.linkedin.com/in/davide-deplano-a331a812a).
