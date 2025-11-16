
# 📘 Interpretable Machine Learning Project  
### Loan Default Prediction with SHAP + Counterfactual Explanations

---

## 1. Model Performance Summary
- **Test AUC:** 0.8677685950413223
- **Test F1 Score:** 0.7058823529411765

---

## 2. Included Artifacts
✔ Model: `outputs/models/lgbm_loan_model.joblib`  
✔ ROC Curve: `outputs/roc_curve.png`  
✔ Confusion Matrix: `outputs/confusion_matrix.png`  
✔ SHAP Global Summary: `outputs/shap/shap_summary.png`  
✔ SHAP Feature Importance Bar: `outputs/shap/shap_bar.png`  
✔ SHAP Local Explanation (Case 1): `outputs/shap/shap_local_case1.html`  
✔ Counterfactual Table: `outputs/counterfactuals/fallback_counterfactuals_table.csv`  
✔ Metrics JSON: `report/metrics.json`

---

## 3. SHAP Global Feature Interpretation

Top features influencing loan default are shown in `shap_bar.png` and `shap_summary.png`.  
SHAP helps understand **why** the model predicted default by showing feature contributions.

---

## 4. Local SHAP Explanations (3 Test Cases)
For each selected high-risk borrower, SHAP explains:
- which features increased risk, and  
- which features decreased risk  

Use `shap_local_case1.html`, `case2`, and `case3` for interactive visualizations.

---

## 5. Counterfactual Explanations
Counterfactuals show **how to change the prediction** from default → non-default.

The file:  
`fallback_counterfactuals_table.csv`  
includes at least 3 actionable counterfactuals, such as:
- increase income  
- reduce loan amount  
- improve credit history score  

These provide **real-world recommendations** for risk reduction.

---

## 6. SHAP vs Counterfactuals (Comparison)
**SHAP**  
- tells *why* the model made a prediction (feature contribution)  
- useful for fairness, transparency, and model debugging  

**Counterfactuals**  
- tell *how to change* the outcome  
- useful for borrowers & analysts  

Together, both provide strong interpretability for ML models.

---

## 7. Practical Feasibility
Some counterfactuals are realistic (e.g., increasing documentation income).  
Others (e.g., changing property area) may not be practical.  
This should be discussed in the final write-up as part of interpretability.

---

End of Report.
