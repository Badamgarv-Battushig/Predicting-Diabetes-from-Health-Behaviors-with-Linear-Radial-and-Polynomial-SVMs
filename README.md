Project Title:

Predicting Diabetes from Health Behaviors using Support Vector Machines



Overview:

This project explores the use of support vector machines (SVMs) to predict diabetes status using data from the National Health Interview Survey (NHIS), accessed through IPUMS Health Surveys. The analysis focuses on understanding how demographic characteristics and health behaviors relate to diabetes outcomes.



Dataset:

The dataset contains survey responses on demographics, health conditions, and lifestyle behaviors such as physical activity, diet, smoking, work hours, and sleep. The target variable (DIABETICEV) was recoded into a binary outcome indicating diabetes status (Yes/No). The analysis was restricted to adult respondents and cleaned to remove missing or non-substantive values.



Models Used:

Three SVM models were implemented and compared:

\- Linear kernel

\- Radial (RBF) kernel

\- Polynomial kernel



Methodology:

\- Data cleaning and recoding of categorical variables

\- Removal of missing values (complete-case analysis)

\- Train-test split (70% training, 30% testing)

\- Hyperparameter tuning using 5-fold cross-validation

\- Model evaluation on a held-out test set



Evaluation Metrics:

The following metrics were used to evaluate model performance:

\- Accuracy

\- Sensitivity (Recall)

\- Specificity

\- Precision

\- F1 Score

\- Balanced Accuracy

\- Area Under the Curve (AUC)



Results:

All models achieved high accuracy (\~0.89), but this was driven by strong performance on the majority “No diabetes” class. Sensitivity was extremely low across all models, meaning most true diabetes cases were not identified. The polynomial kernel performed slightly better than the radial and linear models based on balanced accuracy and AUC, but overall performance remained weak.



Key Findings:

\- Age, BMI, and physical activity were among the strongest predictors of diabetes.

\- The dataset was highly imbalanced (\~10% diabetes cases), which negatively affected model performance.

\- Models tended to predict the majority class, leading to poor detection of diabetes cases.



Limitations:

\- Strong class imbalance limits model effectiveness

\- Complete-case analysis reduces sample size and may introduce bias

\- Observational data means results are predictive, not causal



Conclusion:

While SVMs provide a useful framework for comparing linear and nonlinear decision boundaries, they performed poorly as practical tools for diabetes detection in this dataset. Future improvements could include better handling of class imbalance and alternative modeling approaches.



References:

IPUMS Health Surveys, Minnesota Population Center. (2022). NHIS data (accessed via course GitHub).

