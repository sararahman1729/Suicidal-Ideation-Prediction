# Suicidal-Ideation-Prediction
This research project focuses on the use of machine learning techniques to predict suicidal ideation risk in individuals diagnosed with Major Depressive Disorder (MDD) using clinical, psychological, and demographic data. After comprehensive data preprocessing and feature selection, multiple classification models—including Logistic Regression, Decision Tree, Random Forest, AdaBoost, and KNN—were evaluated using stratified cross-validation. The Random Forest model achieved the best performance, reaching 100% accuracy and an AUC of 1.0, demonstrating strong generalization capability. To ensure transparency and clinical relevance, LIME-based explainable AI was applied, revealing PHQ-9 and emotional sensitivity as the most influential predictors. The results highlight the effectiveness of ensemble learning combined with interpretability for reliable suicide risk assessment.

System Architecture & Methodology
* Data Architecture

  * Dataset: Clinical data from 201 MDD patients collected in psychiatric hospitals (Iran).
  
  * Input Features:
  
    * Psychological scales: PHQ-9, Emotional Reactivity Scale (ERS), PTSD Scale (PVSS-21)
  
    * Trauma history: Adverse Childhood Experiences (ACE)
  
    * Cognitive and behavioral indicators: Probabilistic Reward Task (PRT)
  
    * Demographics (age, education, etc.)

  * Target Variable:
    Suicidal ideation categorized into four risk classes based on Beck Scale of Suicidal Ideation (BSSI):
  
    * No Risk (0–7)
    
    * Low Risk (8–15)
    
    * Moderate Risk (16–25)
    
    * High Risk (26–38)

* Data Preprocessing Pipeline
  - Handled missing categorical values using mode imputation and verified numerical features for completeness.
  - Performed outlier detection using the Interquartile Range (IQR) method to ensure data quality.
  - Applied correlation-based feature selection and removed redundant features to avoid multicollinearity and target leakage.
  - Normalized numerical features using Min–Max scaling and encoded categorical variables using one-hot encoding.
  - Encoded suicidal ideation into four risk levels (No, Low, Moderate, High) based on Beck Scale scoring.
    
* Model Architecture
  - Implemented a comparative machine learning framework including Logistic Regression, Decision Tree, Random Forest, AdaBoost, and K-Nearest Neighbors (KNN).
  - Used an 80/20 train–test split with stratified k-fold cross-validation to handle class imbalance.
  - Applied hyperparameter optimization using RandomizedSearchCV and Bayesian Optimization to improve model performance.
  - Integrated explainable AI using LIME (Local Interpretable Model-Agnostic Explanations) for transparent and interpretable predictions.

* Results 
  - Random Forest achieved the best performance with 100% accuracy, precision, recall, F1-score, and an AUC-ROC of 1.0.
  - Decision Tree and KNN models also demonstrated strong performance with high AUC scores.
  - Feature importance analysis revealed PHQ-9 and Emotional Sensitivity as the most influential predictors of suicidal ideation risk.
  - The results confirm the effectiveness of ensemble learning combined with explainable AI for clinical risk prediction.
