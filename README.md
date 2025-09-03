# Pancreatic Cancer Survival Prediction

A machine learning project that uses different and optimized models for survival status prediction in pancreatic cancer patients

# ABSTRACT
Pancreatic Cancer has one of the lowest survival rates among all cancers, with just 13 % because in most cases, it is diagnosed late as symptoms are mild during early stages. This project develops an optimized machine learning model to predict survival status in pancreatic cancer patients
Exploratory data analysis (EDA) revealed important observations and clinical patterns.  Late-stage diagnosis (Stage 3 and 4) was associated with high mortality, with chemotherapy showing better survival outcomes compared to radiation and surgery. Correlations revealed that survival time and stage at diagnosis are the strongest predictors of survival status as both are heavily and negatively correlated to each other, whereas most demographic and lifestyle factors showed very weak correlations

Due to severe class imbalance (87% non-survivors vs. 13% survivors), Synthetic Minority Oversampling Technique (SMOTE) was applied to balance the dataset as without SMOTE, model would be good at predicting majority class and bad at predicting minority class which is lethal. Three machine learning models—Logistic Regression, Random Forest, and XGBoost—were trained and optimized using cross-validation and hyperparameter tuning. Performance was monitored using Precision, F-1 Score, Confusion Matrix and Recall as Accuracy could be misleading sometimes.

Results showed that default models performed poorly on the minority survival class, but after hyperparameter tuning and threshold optimization, a significant change in performance was observed. Random Forest improved its F1-score from 0.11 to 0.23 at an optimal threshold of 0.028, while XGBoostimproved from 0.16 to 0.23 at a threshold of 0.006. Both models achieved nearly perfect recall (≈1.0), ensuring that no survival cases were missed. Logistic Regression was initially tested, but due to its poor performance in handling the complex non-linear relationships within the dataset, it was not included in the hyperparameter tuning stage. Threshold optimization maximized recall (≈1.0) but precision was still somewhat low, and F-1 Score being moderate. However, in some medical cases recall is more important as missing a positive case is much critical than raising false alarms.

This project demonstrated that using EDA, class imbalance handling, and threshold optimization can significantly improve model’s performance and its ability to predict survival status 

Keywords: Pancreatic Cancer, Machine Learning, Threshold Optimization, Survival Prediction, Healthcare Analytics

# AUTHOR-Shaurya Pandey
