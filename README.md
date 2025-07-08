# ⚖️ MDL Case Outcome Prediction

This repository contains a supervised machine learning pipeline to predict the outcomes of Multi-District Litigation (MDL) cases based on structured metadata, judicial assignments, procedural history, and litigation characteristics. The project uses real-world data sourced from JPML and CourtListener APIs.

---

## 📂 Repository Structure

- `updated_MDL_Win_Prediction_Notebook.ipynb`  
  A complete notebook for preprocessing, feature engineering, model training, and evaluation.

- `mdl_dataset.csv`  
  Structured dataset with 258 MDL cases × 27 features.

- `README.md`  
  Project overview and usage guide.

---

## 📊 Dataset Overview

The dataset includes 258 observations and 27 features. Each record represents an MDL case enriched with:

- **Metadata**: MDL Number, Docket ID, Case Title  
- **Judicial Information**: Assigned Judge, Jurisdiction/District  
- **Timeline Variables**: Filing dates, hearing dates, discovery durations  
- **Procedural Features**: Number of motions filed, bellwether trials, settlement attempts  
- **Outcome**: Categorical label (Settled, Dismissed, etc.)

> **Missing Data:** Only 3 nulls (non-critical columns); imputation or removal is optional

---

## 🧠 Problem Formulation

The task is formulated as a **binary classification** problem:

- **Target Variable**: `Outcome` (transformed into `Win` vs `No-Win`)
- **Objective**: Predict favorable resolution (settlement or success) based on prior case characteristics

---

## 🧪 Model Pipeline

Implemented in `updated_MDL_Win_Prediction_Notebook.ipynb`:

1. **Data Preprocessing**
   - Categorical encoding for judge/district fields
   - Date parsing and timeline feature engineering
   - Handling of missing/non-standard entries

2. **Feature Engineering**
   - Derived durations (e.g., Discovery Length, Pre-Trial Delay)
   - Procedural event counts (motions, hearings)

3. **Model Selection**
   - Baseline model: `LogisticRegression()` from `sklearn`
   - 5-Fold Cross-Validation
   - Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC

4. **Model Evaluation**
   - Confusion matrix
   - ROC curve analysis
   - Class distribution analysis

---

## 🔧 How to Use

1. Clone the repository or upload files to Colab:

```bash
git clone https://github.com/your-org-name/mdl-case-prediction.git

# Load dataset
import pandas as pd
df = pd.read_csv('mdl_dataset.csv')




Run the notebook end-to-end or adapt the pipeline to use other ML models (e.g., RandomForest, XGBoost).


📦 Requirements

Install dependencies using pip:



pip install pandas numpy scikit-learn matplotlib seaborn jupyter


Data Sources
Judicial Panel on Multidistrict Litigation (JPML): Aggregated metadata on MDL proceedings

CourtListener API: Judge and docket-level augmentation


Notes
Scope: This is a proof-of-concept model, not a production deployment.

Limitations: Small sample size; generalization to future MDLs requires further validatio
