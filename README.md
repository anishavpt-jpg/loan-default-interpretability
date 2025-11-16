# 🏦 Loan Default Prediction with Explainable AI (LightGBM + SHAP + Counterfactuals)

This repository contains an **Interpretable Machine Learning** project for predicting loan default risk using **LightGBM**, enhanced with two powerful explainability techniques:

- **SHAP (SHapley Additive exPlanations)**  
  For understanding *why* the model makes specific predictions  
- **Counterfactual Explanations**  
  For understanding *how to change* a borrower's features to flip a prediction  
  (default → non-default)

The project demonstrates how explainability techniques make ML models **transparent**, **auditable**, and **actionable**, especially in financial decision-making.

---

## 📂 Repository Contents

loan-default-interpretability/
│
├── Counterfactual_Explanations_for_Loan_Default_Prediction.ipynb # Full end-to-end Colab notebook
│
├── outputs/
│ ├── models/
│ │ └── lgbm_loan_model.joblib
│ │
│ ├── roc_curve.png
│ ├── confusion_matrix.png
│ │
│ ├── shap/
│ │ ├── shap_summary.png
│ │ ├── shap_bar.png
│ │ ├── shap_local_case1.html
│ │ ├── shap_local_case2.html (if generated)
│ │ └── shap_local_case3.html (if generated)
│ │
│ └── counterfactuals/
│ └── fallback_counterfactuals_table.csv
│
└── report/
├── final_report.md
└── metrics.json


---

## 🎯 Project Objective

To build a **transparent and interpretable** loan default prediction model using:

### ✔ LightGBM — high-performance gradient boosting  
### ✔ SHAP — global + local feature impact  
### ✔ Counterfactual Explanations — actionable improvements

This helps financial institutions:

- Understand each prediction  
- Ensure fairness & accountability  
- Provide actionable feedback to borrowers  
- Improve trust in ML decision-making  

---

## 🧠 Model Overview

### 🔹 Model Used  
**LightGBMClassifier** (inside an sklearn Pipeline)

### 🔹 Preprocessing  
- One-hot encoding for categorical features  
- Median/mode imputation  
- Standard scaling for numeric features  

### 🔹 Training  
Used Train/Test split with stratified sampling.

### 🔹 Evaluation Metrics  
Stored in `report/metrics.json`:

- **AUC Score**
- **F1 Score**
- **Classification Report**
- **Confusion Matrix**

---

## 📊 Explainability Components

### 🔸 1. Global SHAP Explanations  
Files:
- `shap_summary.png`  
- `shap_bar.png`  

These visualizations show **which features influence the model the most**.

### 🔸 2. Local SHAP Explanations  
Files:
- `shap_local_case1.html`  
- `shap_local_case2.html`  
- `shap_local_case3.html`  

These explain **individual borrower predictions** with interactive plots.

### 🔸 3. Counterfactual Explanations  
File:
- `fallback_counterfactuals_table.csv`

This shows **what minimal changes** a borrower could make to shift from default → non-default.

---

## 📄 Final Report

A detailed written analysis is included:

📌 `report/final_report.md`

It contains:
- Model summary  
- Evaluation metrics  
- SHAP interpretation  
- Three local explanation cases  
- Counterfactual analysis  
- SHAP vs Counterfactual comparison  
- Feasibility of suggested actions  

---

## ▶️ How to Run the Notebook

1. Download or open `Loan_Project.ipynb`
2. Open it in **Google Colab**
3. Mount Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
