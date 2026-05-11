# Lecture Exercises — AI/ML: Analysis, Visualization, and Sustainability

Two companion notebooks for a lecture series on applied machine learning.
Each notebook is self-contained: every code cell is annotated, synthetic data
are generated inline, and no external datasets need to be downloaded.

---

## Notebooks

### 1. `data_analysis_visualization.ipynb` — AI Outputs: Analysis & Visualization

Companion to the lecture *"Advanced Data Analysis & Visualization for AI Outputs"*.

| Section | Topic | Methods |
|---------|-------|---------|
| 1 | Performance metrics beyond accuracy | Confusion matrix, ROC-AUC, Precision-Recall curve, AUPRC |
| 2a | Tabular explainability | LIME (`LimeTabularExplainer`) on a Random Forest |
| 2b | Text explainability | LIME (`LimeTextExplainer`) on TF-IDF + Logistic Regression (20 Newsgroups) |
| 3 | Dimensionality reduction | PCA, t-SNE, UMAP side-by-side on the Digits dataset; scree plot |
| 4 | Distribution shift detection | Two-sample KS test with CDF visualization |

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/data_analysis_visualization.ipynb)

---

### 2. `ai_ml_sustainability.ipynb` — AI & ML for Sustainability

Companion to a lecture on AI applications in environmental monitoring and resource management.

| Section | Topic | Methods |
|---------|-------|---------|
| 1 | Regression baseline | Random Forest regressor for water demand prediction; feature importances; skill score vs. mean baseline |
| 2 | Concept drift | Simulated level shift in a time series; RMSE comparison pre/post drift |
| 3 | Geographic bias | Train on Region A (temperate), evaluate on Region B (semi-arid); transfer error analysis |
| 4 | Anomaly detection | Isolation Forest on an environmental sensor stream; precision/recall trade-off via `contamination` |

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/ai_ml_sustainability.ipynb)

---

## Requirements

All exercises run on the standard Colab Python environment. The only non-default
packages are:

```
pip install lime umap-learn
```

Both notebooks include a setup cell that loads all imports and prints a confirmation
message. Run that cell first.

| Package | Version tested | Purpose |
|---------|---------------|---------|
| `scikit-learn` | ≥ 1.3 | Classification, regression, dimensionality reduction, anomaly detection |
| `numpy` | ≥ 1.24 | Array operations |
| `pandas` | ≥ 2.0 | Tabular data manipulation |
| `matplotlib` | ≥ 3.7 | Visualization |
| `scipy` | ≥ 1.11 | KS test (`scipy.stats.ks_2samp`) |
| `lime` | ≥ 0.2 | Local interpretable model-agnostic explanations |
| `umap-learn` | ≥ 0.5 | Uniform Manifold Approximation and Projection |

---

## Running in Google Colab

1. Click the **Open in Colab** badge above the notebook you want.
2. In Colab, run the setup cell (first code cell) to install missing packages and
   load all imports.
3. Execute cells in order with **Runtime → Run all**, or step through them manually.

> **Note on badges:** the badges point to
> `https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/<notebook>.ipynb`.
> Replace `YOUR_USERNAME` and `YOUR_REPO` in this README and inside each notebook's
> badge cell with your actual GitHub username and repository name before pushing.

---

## Repository structure

```
.
├── README.md
├── data_analysis_visualization.ipynb
└── ai_ml_sustainability.ipynb
```

---

## License

The notebooks are released for educational use. All datasets are synthetic and
generated at runtime; no third-party data redistribution is involved.
The 20 Newsgroups corpus used in Section 2b of the first notebook is fetched
at runtime via `sklearn.datasets.fetch_20newsgroups` under its original license.
