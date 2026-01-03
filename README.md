# Undergraduate-Research--Algorithmic-Fairness-in-ML-Models
Fairness-Audit-UCI-Credit: A comparative audit of Logistic Regression and XGBoost models exploring Proxy Bias and Disparate Impact across Age, Sex, and Marital Status. Includes Proxy Reconstruction (AUC) and Outcome Parity (DIR) analysis.

**Project Overview**
  This project performs a comprehensive Algorithmic Fairness Audit on the UCI Default Credit Card dataset. The goal is to determine if "Fairness by Oblivion" (deleting protected columns) is an effective strategy to prevent discrimination. We investigate whether machine learning models can "reconstruct" protected identities—Age, Sex, and Marriage, through behavioral proxies.

**Audit Methodology**: 
  We compare two modeling approaches: Logistic Regression (Linear) and XGBoost (Non-Linear). The audit is split into two frameworks:

Proxy Reconstruction (Identity Leakage): We train "throwaway" detectors to see if financial features (like payment history and credit limits) can predict the hidden protected attributes. This is measured via AUC.

Outcome Parity (Disparate Impact): We measure the Disparate Impact Ratio (DIR) of the final credit models to see if approval rates are equal across demographic groups.

**Key Findings**

<img width="769" height="194" alt="Image" src="https://github.com/user-attachments/assets/4a008a26-11be-435a-b626-59a708cc8df1" />


<img width="767" height="184" alt="Image" src="https://github.com/user-attachments/assets/276ed738-30b9-46f1-b8f3-aaadc7eac965" />

**Key Features**
- Double-Blind Audit: Models are trained without access to sensitive attributes.
- Proxy Identification: Uses SHAP (SHapley Additive exPlanations) and Logistic Coefficients to identify exactly which features leak identity.
- Fairness Dashboard: Visualizes the trade-off between model accuracy, identity leakage, and outcome parity.


**Repository Structure**
- _data/:_ Contains the UCI Credit Card dataset.
- _notebooks/:_ Modular Jupyter notebooks for Data Prep, Proxy Audits, and DIR calculations.
- _scripts/:_ Python scripts for generating the Fairness Dashboard.
- _results/:_ Saved plots (ROC curves, SHAP summary plots, and DIR bar charts).

**Installation & Usage**
1. Clone the repo: git clone https://github.com/yourusername/Fairness-Audit-UCI.git
2. Install dependencies: pip install xgboost shap scikit-learn pandas matplotlib
3. Run the audit: jupyter notebook notebooks/fairness_audit.ipynb


Author: Jayaram

Topic: Undergraduate Research - Algorithmic Fairness in Machine Learning

**References**
1. Barocas & Selbst (2016): Big Data's Disparate Impact.
2. Lundberg & Lee (2017): A Unified Approach to Interpreting Model Predictions (SHAP). 
3. UCI Machine Learning Repository: Default of Credit Card Clients Dataset.
