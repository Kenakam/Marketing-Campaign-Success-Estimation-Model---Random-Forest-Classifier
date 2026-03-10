# Marketing Campaign Success Estimation Model

## 📌 Project Overview
This repository contains a machine learning pipeline designed to estimate the success of marketing campaigns. The goal is to predict whether a customer will respond positively ('yes') to a campaign based on demographic data and previous interaction history.

The project utilizes a **Random Forest Classifier**, a powerful ensemble method capable of capturing non-linear relationships and providing insights into feature importance.

## 🛠️ Project Workflow
1.  **Pre-processing**:
    * **Descriptive Analysis**: Initial exploration of data distributions and identifying potential issues.
    * **Feature Encoding**: Categorical variables (e.g., job, education) were transformed using `LabelEncoder` and manual mapping.
    * **Target Transformation**: The target variable was converted to a numerical format for binary classification.
2.  **Baseline Modeling**:
    * Implementation of a standard Random Forest model to establish a performance benchmark.
3.  **Hyperparameter Tuning**:
    * Utilized **RandomizedSearchCV** to explore the optimal parameter space for `n_estimators`, `max_depth`, and `min_samples_split`.
4.  **Evaluation**:
    * Performance was measured using **Gini Coefficient**, **Precision**, and **Recall**.
    * Analyzed **Feature Importance** to determine which factors (e.g., age, balance, contact method) most influence campaign success.
5.  **Deployment Simulation**:
    * A dedicated script to process new "production" data and output the **Probability of Interest** for prospective customers.

## ⚠️ Notes & Constraints
* **Local Machine Iteration**: This model was developed and trained on a local machine with limited computational resources. As a result, the hyperparameter tuning and model iterations were not exhaustive. Further optimization (e.g., larger search grids or more folds in Cross-Validation) could yield improved results.
* **Task-Specific Thresholds**: The classification thresholds and specific outlier boundaries applied in this notebook were tailored for a specific exercise requirement. They are **not intended as universal best practices** and should be adjusted based on the specific business cost of false positives vs. false negatives.

## 📊 Performance Summary
The initial baseline model showed significant overfitting (100% Gini on training data vs. ~53% on test data), which was addressed during the hyperparameter tuning phase to ensure better generalization on unseen data.

## 💻 Technologies Used
- **Python 3.x**
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn, SciPy

## 🚀 Usage
1. Clone the repository.
2. Ensure `marketing.csv` and `marketing_test.xlsx` are in the project folder.
3. Run `Marketing Campaign Success Estimation Model - Random_Forest_Classifier.ipynb` to view the analysis and training steps.
