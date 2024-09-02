## Knowledge Discovery report

The purpose of this project is to extract useful, valid, novel and understandable patterns from the 1994 Census income, available at [ML repository](https://archive.ics.uci.edu/dataset/2/adult). The goals is to uncover insights to determine the factors influencing whether a person earns more than $50K a year or not.

### Abstract

This project leverages Python as the primary software tool for pre-processing, exploring, and mining the 1994 Census Income dataset. Python was chosen for its extensive libraries, which support efficient data processing and advanced machine learning. The key objective is to classify income levels (<=50K and >50K) using Decision Trees (DT), Random Forest (RF), and Logistic Regression algorithms (LR).
A significant focus of the project is the extraction of decision rules from DT and RF models. These rules provide transparent, interpretable insights into the factors influencing income levels. While Decision Trees offer straightforward decision paths, Random Forest, with its ensemble of trees, not only improves predictive accuracy but also aggregates decision rules, ensuring robust knowledge extraction. 

### Summary of the key sections:

Selected Software:

Tools Used: Python, Scikit-learn, Pandas, NumPy, and other relevant data analysis libraries.
Purpose: These tools were chosen for their robustness in handling data preprocessing, feature engineering, model training, and evaluation.
Selected Data Mining Algorithms:

Algorithms: Random Forest, Decision Tree, Logistic Regression.
Usage: These algorithms were selected for their interpretability and effectiveness in classification tasks, particularly in extracting meaningful patterns from the dataset.
Knowledge Discovery From Census Data: Complete Analysis:

Objective: A thorough analysis of the Census Income dataset to uncover patterns that distinguish between income levels (≤50K vs. >50K).
Approach: The analysis involves preprocessing, feature engineering, model training, and evaluation to extract valuable insights.
Main Observations from the Exploratory Data Analysis (EDA):

Key Findings: Initial exploration highlighted correlations between income levels and features like education, occupation, and work hours.
Visualizations: Graphical representations helped in understanding the distribution of income and identifying potential outliers or anomalies.
Handling Missing Data:

Strategies: Missing values were addressed by either removing rows with NaNs or using imputation techniques.
Impact: The choice of method impacted the dataset size and the overall model performance, leading to a preference for SMOTE to mitigate information loss.
Feature Creation:

New Features: Age groups, education categories, and other derived features were created to capture more granular insights.
Purpose: These features were designed to improve model performance by providing more meaningful input variables.
Feature Transformation:

Techniques Used: One-hot encoding, normalization, and standardization were applied to prepare features for modeling.
Goal: Ensure that features are on a comparable scale and categorical variables are properly represented.
Feature Selection:

Methodology: PCA, Random Forest importance, and backward selection were employed to identify the most impactful features.
Result: A refined set of features was selected to reduce dimensionality and enhance model accuracy.
Handling Data Imbalance:

Approach: SMOTE was used to balance the class distribution of the target variable.
Outcome: This technique helped improve model robustness by addressing the skewed distribution of income classes.
ML Algorithms: Model Creation:

Models Trained: Multiple models including Random Forest, Decision Tree, and Logistic Regression were created and evaluated.
Performance Metrics: ROC-AUC scores and other metrics were used to compare model effectiveness in predicting income levels.
Interesting Rules Discovered:

Insights: The analysis uncovered specific rules that were particularly predictive of higher income levels, such as certain combinations of occupation, education, and work hours.

Interpretation: These rules provide actionable insights for understanding income determinants.

### Python libraries required
name: Census_Income
channels:
  - conda-forge
  - defaults

dependencies:
  - python=3.12.4 
  - numpy
  - pandas
  - matplotlib
  - seaborn
  - plotly
  - networkx
  - scipy
  - shap
  - scikit-learn
  - imbalanced-learn
  - mlxtend
  - statsmodels
  - treeinterpreter
  - tqdm
  - pip:
    - treeinterpreter
### Conclusions
In this project, the 1994 Census Income dataset is analysed to uncover factors influencing whether a person earns more than $50K annually. DT and RF models, decision rules are extracted decision rules that provide clear, interpretable insights into the income classification process. The DT rules revealed that marital status, capital gains, and education levels are significant factors in determining income. These rules were validated by comparing them with RF feature importance, which highlighted similar key features, confirming the consistency of our findings.

The results showed that different DT depths provided varying levels of detail, with a depth of 4 offering a good balance between accuracy and simplicity. The RF model supported this by emphasizing the importance of hours worked per week, marital status, and education level. Overall, the combination of DT and RF methods allowed us to effectively understand and validate the factors influencing income, with the recommendation to use a maximum depth of 4 for Decision Trees to avoid overfitting while maintaining robust predictive performance.
