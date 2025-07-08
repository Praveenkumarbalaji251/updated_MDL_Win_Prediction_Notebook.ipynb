
# 🏛️ MDL Case Outcome Prediction

This repository contains a machine learning project designed to predict outcomes of Multi-District Litigation (MDL) cases using structured case metadata, judicial assignments, procedural timelines, and litigation characteristics.

---

## 📁 Files

- `mdl_dataset.csv` – Primary dataset containing 258 MDL cases with 27 features  
- `updated_MDL_Win_Prediction_Notebook.ipynb` – Complete analysis and ML pipeline in a Jupyter notebook  
- `README.md` – Project overview and usage instructions

---

## 📊 Dataset Overview

The dataset captures detailed information for 258 MDL cases, including:

- **Case metadata:** MDL Number, Docket Number, Case Title, etc.  
- **Judicial information:** Assigned Judge, District  
- **Timeline data:** Filing date, hearing date, discovery periods  
- **Case characteristics:** Type, Status, Outcome, Complexity  
- **Procedural details:** Number of motions, settlement attempts, and more

**Shape:** 258 rows × 27 columns  
**Missing values:** Minimal (only 3 missing entries in the CourtListener Link column)

---

## 🧠 Key Features

- **🎯 Target Variable:** `Outcome` (e.g., Settled, Dismissed, etc.)
- **🔍 Predictive Features:** Case type, complexity, judge, district, timeline metrics
- **📊 Data Quality:** Clean and well-structured dataset

---

## 🛠️ Model Approach

Implemented in `updated_MDL_Win_Prediction_Notebook.ipynb`:

1. **Data Preprocessing & Feature Engineering**
2. **Target Labeling:** Binary classification for “Win” vs. “No-Win”
3. **Modeling Technique:** Logistic Regression with Cross-Validation
4. **Performance Metrics:** ROC-AUC, Accuracy, Confusion Matrix

---

## 🚀 Usage

To run the notebook:

```python
# Load the dataset
import pandas as pd
df = pd.read_csv('mdl_dataset.csv')
