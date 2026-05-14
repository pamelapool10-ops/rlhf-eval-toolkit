# RLHF Evaluation Toolkit

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![License](https://img.shields.io/badge/License-MIT-green)
![Stars](https://img.shields.io/badge/Stars-340%2B-yellow)

A modular Python library for **Reinforcement Learning from Human Feedback (RLHF)** data quality assessment. Built to solve real-world problems in large-scale LLM training pipelines.

---

## 🔍 What It Does

When training frontier AI models, the quality of human preference data directly determines model behavior. This toolkit automates the most tedious and error-prone parts of that process:

- **Preference Ranking Validation** — detects inconsistent or contradictory ranker decisions across annotation batches
- **Inter-Rater Agreement (IRA) Scoring** — computes Cohen's Kappa, Krippendorff's Alpha, and custom weighted agreement metrics
- **Annotation Consistency Scoring** — flags individual annotators or batches that fall below quality thresholds
- **Batch-Level Quality Reports** — generates structured JSON + HTML reports summarizing dataset health

---

## 🛠️ Tech Stack

| Layer | Tools |
|---|---|
| Core language | Python 3.10+ |
| Data processing | pandas, NumPy, polars |
| Agreement metrics | scikit-learn, custom implementations |
| Data validation | JSON Schema, Pydantic |
| Reporting | Jinja2 (HTML reports), rich (CLI output) |
| Testing | pytest, unittest |

---

## 📂 Project Structure
rlhf-eval-toolkit/
├── src/
│   ├── validators/         # Preference ranking validation logic
│   ├── agreement/          # IRA computation (Kappa, Alpha, custom)
│   ├── scoring/            # Annotation consistency scoring
│   └── reports/            # HTML + JSON report generation
├── tests/                  # Unit and integration tests
├── examples/               # Sample datasets and usage notebooks
├── notebooks/              # Jupyter analysis notebooks
└── README.md
