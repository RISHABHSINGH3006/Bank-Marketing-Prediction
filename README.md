# Classification Model Analysis

## Task Overview
This project focuses on understanding and applying AI principles in decision-making processes. The goal is to build and analyze a classification model that predicts customer subscription to a term deposit based on marketing interactions.

## Learnings
- How to build a classification model using Python.
- Techniques for analyzing feature importance in a classification model.
- Methods to visualize and interpret model predictions.

## Project Background
A large bank has requested an evaluation of its retail banking marketing algorithm, which predicts whether a client will subscribe to a term deposit. The bank optimizes its phone marketing strategy based on these predictions. Management seeks to understand how classification models influence decision-making and how explainability can be enhanced.

## Dataset
The dataset used in this project is **bank-additional-full.csv**, which contains information on customer demographics, past interactions, and economic indicators. The target variable (`y`) indicates whether a customer subscribed (`yes=1`, `no=0`).

## Steps in the Analysis

### 1. Data Preprocessing
- Loaded dataset and checked for missing values.
- Dropped the `duration` column, as it occurs after the target event.
- Transformed categorical variables using:
  - Binary encoding (`default`, `housing`, `loan`)
  - Label encoding (`education`, `month`, `day_of_week`)
  - One-hot encoding (`job`, `marital`, `contact`)
- Removed duplicate records.
- Dropped highly correlated features (`emp.var.rate`, `euribor3m`).

### 2. Exploratory Data Analysis
- Generated bar plots to visualize feature distributions.
- Created a correlation heatmap to analyze feature relationships.
- Identified key features influencing customer subscription.

### 3. Model Building
- Implemented logistic regression as a baseline model.
- Used correlation analysis to refine feature selection.
- Evaluated feature importance based on model coefficients.

### 4. Model Interpretation
- Analyzed how frequency of contact and economic indicators affect predictions.
- Examined negative correlations (e.g., higher `nr.employed` linked to lower subscription rates).
- Assessed the impact of previous customer interactions (`previous`, `pdays`).

### 5. Visualizations
- Correlation heatmaps for numerical variables.
- Feature importance plots to interpret model decisions.

## Key Findings
- Regular and positive communication increases subscription likelihood.
- Customers who were previously contacted and responded positively are more likely to subscribe.
- The number of employees (`nr.employed`) negatively impacts the likelihood of subscription.

## Future Improvements
- Test other classification models (e.g., decision trees, random forests, or XGBoost).
- Implement SHAP values for deeper interpretability.
- Conduct fairness analysis to ensure unbiased decision-making.

## Installation & Requirements
To run this project, install the required dependencies:
```bash
pip install pandas numpy scikit-learn seaborn matplotlib
```

## Running the Analysis
1. Load the dataset and preprocess it.
2. Perform exploratory data analysis.
3. Train and evaluate the classification model.
4. Visualize and interpret results.

## Conclusion
This project highlights the importance of AI in financial decision-making. By improving explainability, businesses can make more informed, ethical, and defensible AI-driven decisions.

