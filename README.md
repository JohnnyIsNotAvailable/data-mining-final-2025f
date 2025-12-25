

#  Lifestyle Habits and Psychoemotional Well-Being Analysis

This project explores how everyday lifestyle habits (sleep, screen use, physical activity, diet) are related to psychoemotional states such as stress, anxiety, fatigue, and overall well-being.
The analysis combines exploratory data analysis, supervised and unsupervised machine learning, and model interpretability techniques.

---

##  Project Structure

```
notebooks/
├── 01_data_cleaning.ipynb
├── 02_eda.ipynb
├── 03_supervised_modeling.ipynb
├── 04_unsupervised_clustering.ipynb
└── 05_shap_analysis.ipynb

data/
└── cleaned_data.csv
└── raw_data.csv
```

---

## Phase 1 — Data Cleaning & Preprocessing

**Notebook:** `01_data_cleaning.ipynb`

**Goal:**
Prepare raw survey data for analysis and modeling.

**Key steps:**

* Renaming columns into a consistent and readable format
* Handling missing values and inconsistent responses
* Converting ordinal and categorical answers into numeric representations
* Creating helper variables (e.g., binary indicators for night awakenings)
* Validating data types and ranges

**Output:**
Cleaned and structured dataset ready for EDA and modeling.

---

## Phase 2 — Exploratory Data Analysis (EDA)

**Notebook:** `02_EDA.ipynb`

**Goal:**
Understand distributions, relationships, and temporal patterns in the data.

**Key analyses:**

* Distributions of stress, anxiety, fatigue, and life satisfaction
* Lifestyle behavior patterns (sleep quality, screen use after 22:00, workouts)
* Relationships between habits and psychoemotional states:

  * Sleep duration → stress
  * Screen use after 22:00 → sleep quality
* Temporal dynamics (today vs week ago vs month ago)
* Correlation analysis

**Novelty element:**
Construction of **composite indices**:

* `stress_index` — average of stress (today, week, month)
* `wellbeing_index` — average of life satisfaction and sub-dimensions

**Output:**
Validated assumptions, feature insights, and motivation for modeling.

---

## Phase 3 — Supervised Learning

**Notebook:** `03_supervised_modeling.ipynb`

**Goal:**
Assess whether lifestyle and psychoemotional features can predict elevated stress levels.

**Approach:**

* Binary classification task (low vs high stress)
* Models used:

  * Logistic Regression (interpretable baseline)
  * Random Forest (nonlinear ensemble model)
* Feature scaling and train/test split
* Model evaluation using:

  * Accuracy
  * Precision, Recall, F1-score
  * ROC-AUC, PR-AUC
  * Confusion matrices

**Outcome:**
Both models demonstrated strong predictive performance, confirming the presence of structured patterns in the data.

---

## Phase 4 — Unsupervised Learning (Clustering)

**Notebook:** `04_unsupervised_clustering.ipynb`

**Goal:**
Identify typical lifestyle–well-being profiles without predefined labels.

**Approach:**

* Feature standardization
* K-means clustering
* Cluster validation and interpretation
* Dimensionality reduction (PCA) for visualization

**Output:**
Clusters representing distinct behavioral and psychoemotional patterns.

---

## Phase 5 — Model Interpretation (SHAP)

**Notebook:** `05_shap_analysis.ipynb`

**Goal:**
Explain *why* the supervised model makes its predictions.

**Method:**

* SHAP (SHapley Additive exPlanations)
* Feature importance at global and local levels
* “What-if” interpretation of lifestyle changes

**Value:**
Transforms black-box predictions into interpretable insights, supporting analytical conclusions rather than diagnostic claims.

---

## Key Takeaways

* Lifestyle habits are systematically linked to psychoemotional well-being
* Sleep quality and late screen use play a particularly important role
* Composite indices enhance analytical depth and originality
* Machine learning models are used as analytical tools, not medical predictors

---

## Limitations

* Self-reported data
* Cross-sectional design
* Moderate sample size

---
