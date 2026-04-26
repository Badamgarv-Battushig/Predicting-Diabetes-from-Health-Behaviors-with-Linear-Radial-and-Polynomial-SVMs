# Predicting Diabetes from Health Behaviors using Support Vector Machines

---

## Overview
This project explores the use of **Support Vector Machines (SVMs)** to predict diabetes status using data from the **National Health Interview Survey (NHIS)** via IPUMS Health Surveys.  
The goal is to understand how **demographics and health behaviors** relate to diabetes outcomes.

---

## Dataset
- Source: NHIS (IPUMS Health Surveys)
- Focus: Adult respondents only  
- Target variable: `DIABETICEV` → recoded to **Yes / No diabetes**
- Includes:
  - Demographics (age, sex, education)
  - Health behaviors (activity, diet, smoking, sleep)
  - Health indicators (BMI, work hours)

---

## Models Used
Three SVM models were implemented and compared:
- 🔹 Linear kernel  
- 🔹 Radial (RBF) kernel  
- 🔹 Polynomial kernel  

---

## Methodology
- Data cleaning and recoding
- Removal of missing values (complete-case analysis)
- Train-test split (**70% / 30%**)
- Hyperparameter tuning (**5-fold cross-validation**)
- Evaluation on a held-out test set

---

## Evaluation Metrics
- Accuracy  
- Sensitivity (Recall)  
- Specificity  
- Precision  
- F1 Score  
- Balanced Accuracy  
- AUC (Area Under the Curve)

---

## Results
- Accuracy was high (~0.89), but **misleading due to class imbalance**
- Sensitivity was **extremely low**, meaning most diabetes cases were missed
- Polynomial kernel performed slightly better, but overall performance remained weak

---

## Key Findings
- Age, BMI, and physical activity are strong predictors
- Dataset is highly imbalanced (~10% diabetes cases)
- Models favor the majority class (**No diabetes**)

---

## Limitations
- Class imbalance reduces model effectiveness  
- Complete-case analysis reduces sample size  
- Results are **predictive, not causal**

---

## Conclusion
SVMs are useful for comparing linear and nonlinear boundaries, but they performed poorly for diabetes detection in this dataset.  
Future work should focus on:
- Handling class imbalance
- Exploring alternative models

---

## References
- IPUMS Health Surveys, Minnesota Population Center (2022) – NHIS data (accessed via course GitHub)  
- James et al. (2023), *An Introduction to Statistical Learning*  
- Meyer et al. (2023), *e1071 R package*

---
