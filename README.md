Crime Dynamics in Canada: Crime Data Analysis and Prediction using Machine Learning

This project applies machine learning techniques to forecast crime incidents in Ontario, Canada, leveraging publicly available datasets from Statistics Canada (1998–2023). The goal is to provide data-driven insights for policymakers, law enforcement, and researchers to support predictive policing, resource allocation, and policy evaluation.

📌 Project Overview

Dataset: Statistics Canada Open Government Portal (1998–2023)

Scope: Ontario province, with crime types categorized as Violent Crime, Property Crime, and Drug Offenses

Records: Processed over 1M raw records → 306,551 structured entries

Key Considerations:

Cannabis legalization in 2018 (structural shift in drug violations)

Socioeconomic factor: unemployment rate (minimal predictive effect)

⚙️ Methodology
🔹 Data Preprocessing

Transposed crime violations into feature columns indexed by year

Removed columns with >50% missing values, mean-imputed others

Performed correlation analysis to reduce redundancy

Incorporated Ontario unemployment rate for exploratory analysis

🔹 Models Implemented

Six supervised ML algorithms were applied:

Decision Tree – interpretable, good for non-linear interactions

Random Forest – ensemble of trees, robust against overfitting

XGBoost – gradient boosting, effective in structured datasets

Ridge Regression – linear with L2 regularization, strong on sparse data

Elastic Net – hybrid of Ridge & Lasso, handles multicollinearity

Extra Trees – randomized ensemble, strong with noisy data

🔹 Evaluation Metrics

R² (Coefficient of Determination)

Accuracy (%) (custom measure of closeness to actual values)

📊 Results Summary

Ridge Regression excelled in low-frequency crimes (robbery, harassment, aggravated sexual assault).

XGBoost & Extra Trees performed best in high-volume crimes (theft, mischief, property crimes).

Cannabis legalization (2018) significantly altered drug violation patterns → required custom train/test splits.

Unemployment rate had negligible impact on predictive accuracy.

Ablation studies showed that reduced feature sets (Top 10 / Top 5) maintained competitive accuracy.

📈 Visualizations

The project includes:

Predicted vs Actual Crime Trends (per violation category)

Feature correlation heatmaps

Ablation study bar charts

🛠️ Tech Stack

Language: Python 3.10

Libraries:

pandas, numpy → Data processing

scikit-learn → ML models

xgboost → Gradient boosting

matplotlib, seaborn → Visualization

🚀 How to Run

Clone this repository:

git clone https://github.com/MeetAdalaja/ml-crime-trends-ontario.git
cd crime-prediction-canada


🎯 Key Contributions

Comprehensive preprocessing pipeline for large-scale Canadian crime data

Comparison of linear vs ensemble ML models

Demonstrated effect of policy change (cannabis legalization) on predictions

Provided insights for evidence-based policing & public safety strategies

📖 References

. Selected key works include:

Kshatri et al. (2021) Ensemble Crime Prediction using Stacked Generalization

Safat et al. (2021) Crime Forecasting using ML and DL

Zhang et al. (2020) Comparison of ML Algorithms for Crime Hotspots

👨‍💻 Authors

Meet Vishnubhai Adalaja, Algoma University, ON, Canada

Md Zamilur Rahman, University of Windsor / NORDIK Institute

Khaleda Begum, Police Headquarters, Dhaka, Bangladesh