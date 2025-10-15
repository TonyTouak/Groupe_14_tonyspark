# Titanic: Predicting Survival - Hackathon Challenge

Welcome to the **Titanic Survival Prediction Challenge**, a data science competition designed to explore one of the most iconic problems in machine learning.  
The objective of this project is to predict whether a passenger survived the Titanic disaster based on a variety of personal and travel attributes.


## Project Overview

This project was completed as part of a **Hackathon**, where teams of seven students collaborated to build the most accurate and well-structured predictive model possible.  
The challenge provided a real-world context to apply data analysis, feature engineering, and machine learning optimization techniques.

We approached this problem using a structured methodology:
1. **Exploratory Data Analysis (EDA):** Understanding data distributions and correlations.
2. **Feature Engineering:** Creating meaningful variables such as `Title`, `FamilySize`, `IsAlone`, `FarePerPerson`, and `Deck`.
3. **Model Selection and Optimization:** Testing multiple models and retaining only the most robust (Logistic Regression).
4. **Threshold and Ensemble Optimization:** Calibrating probability thresholds and fine-tuning model weights.
5. **Submission to Kaggle:** Evaluating final performance on the public leaderboard.

## Methodology

### 1. Data Exploration
- Analysis of missing data and value distributions.
- Visualization of correlations between variables and the target (`Survived`).
- Identification of patterns by passenger class, gender, and age.

### 2. Feature Engineering
New features were created to capture the most relevant aspects of the data:
- `Title` extracted from names.
- `FamilySize` and `IsAlone` to represent family relationships on board.
- `Deck` extracted from the cabin number.
- `FarePerPerson` and logarithmic transformations to normalize monetary values.
- `IsMother` and `IsChild` to represent social roles.

### 3. Model Development
Several models were initially tested (Support Vector Machines, Random Forest, Gradient Boosting).  
After empirical evaluation, **Logistic Regression** proved to be the most stable and generalizable model.

The final model:
- Uses a clean pipeline with scaling and one-hot encoding.
- Applies GroupKFold cross-validation to avoid data leakage between related passengers.
- Optimizes hyperparameters through `GridSearchCV`.
- Calibrates the decision threshold to maximize accuracy on out-of-fold predictions.

### 4. Evaluation and Results
- Out-of-Fold Accuracy (local validation): approximately **0.83 – 0.84**.
- Public Kaggle Score: **0.78708**.
- The model demonstrates consistent generalization and reliability, balancing accuracy and interpretability.


## Technical Stack

- **Language:** Python 3  
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn, xgboost  
- **Environment:** Jupyter Notebook / GitHub Codespaces  
- **Version Control:** GitHub Classroom  
- **Evaluation Platform:** Kaggle (Titanic Competition)


## Key Takeaways

- Feature engineering has a greater impact than model complexity.
- Clean validation using GroupKFold prevents overfitting.
- Logistic Regression, when properly optimized, remains a competitive baseline for structured tabular data.
- Ensemble and threshold optimization provide marginal but meaningful gains.

## Team Members

- **Tony TOUAK**  
- **Gilles SOUOP**  
- **Lorenz TRABBIA**
- **Nerva SONCY**  
- **Fadi AL MIKDAD**  
- **Alban VILLAIN**
