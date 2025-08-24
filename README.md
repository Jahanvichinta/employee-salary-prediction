Project Overview

This project predicts whether an employee earns >50K or <=50K annually using the Adult Income dataset. The goal is to identify key demographic and work-related factors that influence salary and to build accurate classification models.

Dataset

Source: UCI Adult Income Dataset

Rows: ~48,000

Features: Age, Workclass, Education, Marital Status, Occupation, Relationship, Race, Gender, Hours-per-week, Native Country, etc.

Target: Income (<=50K or >50K)

⚙️ Data Preprocessing

Handled missing values (?) and merged rare categories.

Encoded categorical variables (Label Encoding / OneHot Encoding).

Balanced classes using SMOTE to handle target imbalance.

Removed noisy/rare categories in education, marital status, native country for better model stability.

📊 Exploratory Data Analysis (EDA)

Education, Age, Marital Status, Occupation, Hours-per-week emerged as strong predictors of salary.

Married individuals and those with higher education are more likely to earn >50K.

Men dominate higher salary brackets, showing gender bias in the dataset.

🤖 Models Trained

Decision Tree

KNN

Random Forest

XGBoost

Gradient Boosting

Hyperparameter Tuning: Applied GridSearchCV and RandomizedSearchCV.

📈 Results

XGBoost (baseline) achieved the best results, ~84% accuracy, outperforming tuned versions.

Gradient Boosting also performed competitively with ~83–84% accuracy.

Tree-based models (XGB, GBM, RF) consistently outperformed simpler models like Logistic Regression and Decision Tree.

 Observation:

Baseline XGBoost performed better than RandomizedSearchCV-tuned XGBoost, showing that default hyperparameters were already optimal for this dataset.

 Model Evaluation Metrics

Accuracy: ~84% (XGBoost/GBM)

Precision & Recall: Evaluated to ensure performance on the minority class (>50K).

F1-Score: Balanced trade-off between Precision & Recall.

Feature Importance: Education, Age, Marital Status, Occupation, and Hours-per-week were top contributors.

 Key Learnings

Data cleaning (handling rare/missing categories) improves model stability.

SMOTE helps mitigate class imbalance, but tuning doesn’t always guarantee better performance.

XGBoost’s default hyperparameters can sometimes outperform tuned versions, depending on dataset size and noise.

Feature importance analysis provides valuable business insights (e.g., education and work hours drive salaries).

 Tech Stack

Python, Pandas, NumPy, Scikit-learn, Imbalanced-learn, XGBoost, Matplotlib, Seaborn
