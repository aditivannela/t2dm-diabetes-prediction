# t2dm-diabetes-prediction
## Predicting Type 2 Diabetes Risk Using Python and XGBoost

This project uses machine learning to predict the risk of Type 2 Diabetes Mellitus (T2DM) onset using clinical patient data. It was developed as part of a Python course presentation and extends my capstone research project, which examines the use of explainable machine learning models for T2DM risk prediction using multimodal data.
The model produces a risk probability score (0–1) for each patient, where a higher score indicates a greater likelihood of diabetes.

## Dataset

Pima Indians Diabetes Dataset:

768 female patients of Pima Indian heritage
8 clinical features: Glucose, BMI, Age, Blood Pressure, Insulin, Skin Thickness, Diabetes Pedigree Function, Pregnancies
1 outcome: Diabetes (1 = yes, 0 = no)
Source: National Institute of Diabetes and Digestive and Kidney Diseases
Available on Kaggle
Download diabetes.csv from Kaggle and place it in the same folder as the notebook before running.

## Model: XGBoost (Extreme Gradient Boosting)

XGBoost builds many small decision trees sequentially, with each new tree correcting the mistakes of the previous one. It is widely used in published T2DM prediction research and performs well on tabular clinical data.

## What the Notebook Does:

Loads and explores the dataset using pandas
Splits data into training (80%) and test (20%) sets
Trains an XGBoost classifier
Evaluates the model using a classification report and AUC-ROC score
Visualizes feature importance to show which clinical variables matter most

## Results

After running the notebook you will see:
Classification report — precision, recall, and F1-score for each class
AUC-ROC score — how well the model separates diabetic from non-diabetic patients (above 0.80 is considered good for a medical model)
Feature importance chart — Glucose consistently ranks as the most important feature, which aligns with clinical knowledge of T2DM

## How to Run

Clone or download this repository
Download diabetes.csv from Kaggle and place it in the same folder
Open t2dm_xgboost_final.ipynb in Jupyter Notebook or JupyterLab
Install XGBoost if needed:
pip install xgboost
Run all cells top to bottom (Kernel → Restart & Run All)

## Libraries Used

pandas — data loading and exploration
scikit-learn — train/test split and evaluation metrics
xgboost — XGBoost classifier
matplotlib — feature importance visualization


Limitations

Dataset is limited to one population group (Pima Indian women)
Only clinical variables are included — my full capstone model also incorporates lifestyle and neighborhood data
Class imbalance (65% no diabetes, 35% diabetes) is not addressed in this version
Small dataset (768 patients) compared to real-world clinical studies
