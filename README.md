# NBA-MVP-model
Model to predict a player's MVP vote share based on their box & advanced stats

🔗 View full report: https://tsepo001.github.io/NBA-MVP-model/NBA_model.html

## Overview

This project builds and evaluates machine learning models to predict NBA player award outcomes using historical player performance data.

The goal is to demonstrate:

* End-to-end data analysis workflow
* Feature engineering and model building
* Model evaluation and comparison
* Clear communication of results

---

## Problem Statement

Can we predict how likely a player is to receive award votes (or award share) based on their season performance?

This is framed as a **supervised learning problem**, where:

* Inputs = player statistics (e.g. points, assists, efficiency metrics)
* Target = award share / voting outcome

---

## Dataset

The dataset includes:

* Player season statistics
* Shooting efficiency metrics
* Advanced metrics (where available)
* Award voting outcomes

> Note: Data was cleaned and preprocessed before modeling.

---

## ⚙️ Methodology

### Data Preparation

* Handling missing values
* Feature selection
* Scaling (for certain models)
* Train/test split

---

### Models Implemented

* Linear / Generalized Linear Models
* Regularized models (e.g. Lasso/Ridge via glmnet)
* Random Forest (including parallel implementation)
* Gradient Boosting (XGBoost)

---

### Model Evaluation

Models were evaluated using:

* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)
* RMSLE (Root Mean Squared Log Error)

These metrics provide different perspectives on prediction accuracy and robustness.

---

## Results

The models were compared on a held-out test set.

Key observations:

* Tree-based models captured non-linear relationships better
* Regularized models helped reduce overfitting
* Some models produced very similar performance, highlighting:

  * potential feature limitations
  * or convergence to similar predictive structures


---

## Key Insights

* Player scoring and efficiency metrics are strong predictors of award outcomes
* Model performance differences were smaller than expected, suggesting:

  * diminishing returns from model complexity
* Data quality and feature engineering are as important as model choice

---

## Challenges & Lessons Learned

* Ensuring consistent data structure between training and test sets
* Debugging model evaluation pipelines
* Handling edge cases in metrics (e.g. RMSLE with zero/negative values)
* Managing reproducibility between interactive sessions and report rendering

---

## Tools & Technologies

* R
* Quarto (.qmd) for reproducible reporting
* caret
* randomForest
* xgboost
* glmnet
* doParallel (for parallel computing)

---


## How to Run

1. Clone the repository
2. Open the `.qmd` file in RStudio
3. Install required packages
4. Click **Render**
5. 

## 📌 Final Note

🔗 View full report:
https://tsepo001.github.io/NBA-MVP-model/
