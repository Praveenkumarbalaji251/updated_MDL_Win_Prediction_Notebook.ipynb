MDL Case Outcome Prediction
This repository contains a machine learning project for predicting Multi-District Litigation (MDL) case outcomes.

Files
mdl_dataset.csv: The main dataset containing 258 MDL cases with 27 features
updated_MDL_Win_Prediction_Notebook.ipynb: Jupyter notebook with the complete analysis and prediction model
README.md: This file
Dataset Overview
The dataset contains information about Multi-District Litigation cases including:

Case metadata (MDL Number, Docket Number, Case Title, etc.)
Judicial information (Assigned Judge, District)
Timeline data (Filing dates, hearing dates, discovery periods)
Case characteristics (Type, Status, Outcome, Complexity)
Procedural details (Motions count, Settlement attempts, etc.)
Dataset Shape: 258 rows × 27 columns

Key Features
Target Variable: Outcome (Settled, Dismissed, etc.)
Predictive Features: Case type, complexity, judge, district, timeline factors
Data Quality: Complete dataset with minimal missing values (only 3 missing in CourtListener Link)
Model Approach
The notebook implements a logistic regression pipeline with:

Data preprocessing and feature engineering
Target variable creation (Win vs No-Win classification)
Model training with cross-validation
Performance evaluation with ROC-AUC, accuracy, and confusion matrix
Usage
Load the dataset: pd.read_csv('mdl_dataset.csv')
Run the Jupyter notebook for complete analysis
Modify features or model parameters as needed
Data Source
Data compiled from JPML (Judicial Panel on Multidistrict Litigation) and CourtListener records.

Requirements
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
License
This is a proof-of-concept educational project.
