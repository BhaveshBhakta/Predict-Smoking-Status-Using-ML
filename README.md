## Predict Smoking Status

### Project Overview

This project aims to predict an individual's **smoking status** based on various biological and health-related signals. Utilizing a dataset containing demographic information (gender, age, height, weight), body measurements (waist, eyesight, hearing), blood parameters (hemoglobin, cholesterol, triglyceride, HDL, LDL, AST, ALT, Gtp), urine protein, serum creatinine, and oral health indicators (dental caries, tartar), the goal is to develop a machine learning model that can accurately classify whether an individual is a smoker or non-smoker.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Body Signal of Smoking](https://www.kaggle.com/datasets/kukuroo3/body-signal-of-smoking)
  * **Size**: 55692 entries, 27 columns
  * **Key Features**:
      * gender, age, height(cm), weight(kg), waist(cm), eyesight(left), eyesight(right), hearing(left), hearing(right), systolic, relaxation, fasting blood sugar, Cholesterol, triglyceride, HDL, LDL, hemoglobin, Urine protein, serum creatinine, AST, ALT, Gtp, oral, dental caries, tartar.
  * **Approach**:
      * Data Cleaning: Dropped 'ID' as it's a unique identifier. No missing values or duplicates were found.
      * Exploratory Data Analysis: Histograms, Boxplots, and Heatmaps were used for visualization to understand data distributions and correlations.
      * Label Encoding: Applied to all categorical features ('gender', 'oral', 'tartar') and the target 'smoking'. Numerical features were also implicitly converted if they were in object format, but they appeared to be numerical (`float64`, `int64`).
      * Binary Classification: The target variable 'smoking' indicates smoking status (1: smoker, 0: non-smoker). The dataset is imbalanced (35237 non-smokers vs 20455 smokers), but SMOTE was not explicitly applied in the provided code.
      * Models Used:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * 83.2% with Random Forest Classifier.
      * 81.2% with Bagging Classifier.
      * 78.1% with XGBoost Classifier and Decision Tree Classifier.

-----

### Purpose and Applications

  * Predict an individual's **smoking status** based on a range of physiological and health indicators.
  * Assist healthcare providers in identifying individuals at higher risk of smoking-related health issues for targeted interventions.
  * Support public health initiatives by enabling a deeper understanding of the correlates of smoking.
  * Provide insights for developing personalized health recommendations and prevention programs.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Predict-Smoking-Status-Using-ML.git
cd Predict-Smoking-Status-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Addressing the class imbalance explicitly using techniques like SMOTE or undersampling to potentially improve recall for the minority class.
  * Performing comprehensive hyperparameter tuning and cross-validation for all models to optimize performance.
  * Exploring advanced feature engineering techniques, such as creating health scores or ratios from various medical parameters.
  * Adding explainability (e.g., SHAP or LIME) to understand which body signals are the strongest predictors of smoking status.
