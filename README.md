It is written so that **anyone (you in 6 months, an interviewer, or a collaborator)** immediately understands:

- what this repo is
- how it is structured
- how to use it correctly
- what discipline rules are being followed

---

```markdown
# Traditional Machine Learning – Structured Revision Repository

## Purpose

This repository is a **systematic, end-to-end revision of Traditional Machine Learning**  
(excluding Deep Learning and heavy mathematical derivations).

The goal is to:

- Rebuild strong fundamentals
- Practice clean, reproducible ML workflows
- Develop industry-standard project structure
- Prepare for interviews and real-world ML work

This is **not a tutorial dump**.  
It is a **disciplined learning and revision system**.

---

## Scope

Included:

- Python fundamentals (ML-focused)
- NumPy, Pandas, Visualization
- Scikit-learn workflows
- Supervised & Unsupervised learning
- Feature engineering
- Model evaluation & tuning
- Common ML pitfalls
- One end-to-end ML project

Excluded (handled separately):

- Deep Learning (PyTorch / TensorFlow)
- Mathematical proofs
- Neural networks

---

## High-Level Structure
```

traditional_ml/
├── notebooks/ # All learning and experimentation notebooks
├── data/ # Dataset lifecycle (raw → processed)
├── utils/ # Reusable helper code
├── models/ # Saved trained models
├── outputs/ # Figures, tables, reports
└── README.md # This file

```

Each folder has **a single, well-defined responsibility**.

---

## Notebooks (`notebooks/`)

This is the **core of the repository**.

### Design Principles
- One notebook = one topic
- Notebooks are numbered and must be followed in order
- No random or scratch notebooks
- Each notebook contains:
  - Markdown explanations
  - Minimal, clean code
  - Clear takeaways

### Notebook Order

```

00_index_checklist.ipynb # Master checklist & progress tracker
00_setup.ipynb # Environment, imports, conventions
01_python_fundamentals.ipynb
02_numpy.ipynb
03_pandas.ipynb
04_visualization_eda.ipynb
05_ml_problem_types.ipynb
06_sklearn_basics.ipynb
07_data_preprocessing.ipynb
08_regression_models.ipynb
09_classification_models.ipynb
10_unsupervised_learning.ipynb
11_model_evaluation.ipynb
12_hyperparameter_tuning.ipynb
13_feature_engineering.ipynb
14_common_ml_pitfalls.ipynb
15_end_to_end_project.ipynb

```

> Rule: **Work strictly in numerical order.**

---

## Data (`data/`)

This folder represents the **data lifecycle**.

```

data/
├── raw/ # Original, untouched datasets (read-only)
├── processed/ # Cleaned, feature-ready datasets
└── external/ # Third-party or reference data (lookup tables, metadata)

```

### Rules
- `raw/` is never modified
- All cleaning & feature engineering outputs go to `processed/`
- `external/` is optional and may remain empty during revision

This separation prevents:
- Data leakage
- Accidental overwrites
- Loss of reproducibility

---

## Utilities (`utils/`)

Reusable helper code shared across notebooks.

```

utils/
├── metrics.py # Evaluation helpers
├── preprocessing.py # Scaling, encoding, transformations
├── visualization.py # Plotting helpers
└── **init**.py # Makes utils a Python module

````

### Why this exists
- Avoids copy-paste code
- Keeps notebooks focused on learning
- Enforces consistency
- Mirrors real-world ML projects

Usage example:
```python
from utils.metrics import classification_metrics
````

---

## Models (`models/`)

```
models/
└── saved/
```

This folder stores:

- Final trained models
- Serialized artifacts (`.pkl`, `.joblib`, etc.)

Rules:

- Only save meaningful models
- Do not save intermediate experiments

---

## Outputs (`outputs/`)

Anything produced by analysis that is **not data and not a model**.

```
outputs/
├── figures/   # Saved plots (PNG, SVG)
├── tables/    # CSV results, metric summaries
└── reports/   # Markdown or text summaries
```

Examples:

- ROC curves
- Model comparison tables
- Final experiment summaries

Predictions and labels **do not belong here** — they are data.

---

## Discipline Rules (Important)

- No editing files in `data/raw/`
- No mixing deep learning code here
- No unstructured notebooks
- No copy-paste across notebooks
- Reusable logic goes to `utils/`

These rules are intentional and non-negotiable.

---

## How to Use This Repository

1. Open `notebooks/00_index_checklist.ipynb`
2. Track progress as you revise
3. Complete notebooks sequentially
4. Write explanations as if teaching
5. Finish with `15_end_to_end_project.ipynb`

After completion, this repository serves as:

- A revision reference
- An interview discussion artifact
- A template for future ML projects

---

## Future Extension

Deep Learning will be handled separately under:

```
Revision/deep_learning/
```

With its own:

- Notebooks
- Utilities
- Data handling
- Training pipelines

This separation is intentional.

---

## Final Note

This repository is designed to build:

- Conceptual clarity
- Engineering discipline
- Long-term recall

If followed properly, it provides a **solid foundation for advanced ML and Deep Learning work**.
