# Credit-Risk-Modeling-Using-XGBoost-and-Neural-Networks

## Project Description
📌 Project Overview
This project develops a credit risk model to predict the likelihood of customer default using real-world credit card data. The goal is to support better decision-making by classifying customers into different risk segments and recommending credit assignment strategies.

We built and compared two machine learning models — XGBoost and a Neural Network — to estimate default probability. These models were evaluated not only by their predictive accuracy (AUC) but also by how well they rank-order customer risk and support practical credit strategies (e.g., conservative vs. aggressive approval thresholds).


## Data Description and Methodology
We used customer-level credit card data spanning November 2017 to April 2018, focusing on new accounts originated in April 2018. The dataset includes features on customer balances, spending, payment history, risk behavior, and more.
    
    The methodology involved:
Data Preprocessing: One-hot encoding, missing value imputation, outlier treatment (1st/99th percentile capping), and normalization.
Feature Engineering: Created rolling statistics (e.g., 6-month averages, minimums, and maximums) to capture behavioral trends.
Feature Selection: Used XGBoost-based importance and SHAP analysis to select the most predictive variables.
Modeling: Trained and tuned both XGBoost and Neural Network models using grid search and AUC scoring.
Evaluation: Assessed models on AUC, rank ordering, and business metrics like default rate and revenue at various thresholds.

## Results & Insights
Both XGBoost and Neural Network models achieved strong AUC scores (~0.95), with XGBoost performing slightly better and showing more stable rank ordering across samples.
Rank ordering charts confirm that both models effectively separate high-risk from low-risk customers, but XGBoost did so with smoother, more monotonic bin trends.

Strategic threshold analysis revealed a trade-off: lower thresholds reduce default risk but also reduce accepted customers and revenue. A threshold of 0.3 (conservative) and 0.5 (aggressive) were chosen based on performance and default limits.
SHAP analysis offered interpretability, showing features like payment behavior and delinquency duration as top predictors of default.

📂 For detailed performance metrics, visualizations, and strategy explanation, see the PowerPoint presentation.

