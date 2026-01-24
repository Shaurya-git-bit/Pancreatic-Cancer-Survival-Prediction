# Pancreatic Cancer Survival Prediction
Predicting survival outcomes for pancreatic cancer patients using machine learning

# Why This Matters
Pancreatic cancer has one of the lowest survival rates among all cancers, around 13%, because it’s often diagnosed late. Early prediction of survival status can help doctors make better treatment decisions and improve patient care.

# What I Did
I analyzed a dataset of pancreatic cancer patients and built machine learning models to predict survival status. Exploratory data analysis (EDA) revealed key patterns: late-stage diagnosis (Stage 3 and 4) is linked to high mortality, and chemotherapy generally gives better survival outcomes than radiation or surgery.

# Key Challenges
- **Class imbalance:** 87% non-survivors vs. 13% survivors  
  - Without balancing, models would predict the majority class well but fail on survivors.  
  - I used **SMOTE** (Synthetic Minority Oversampling Technique) to address this.  
- **Complex relationships:** Many features interact non-linearly, making simple models like Logistic Regression less effective.

# How the Prediction Works
Three models were trained and optimized:
- **Random Forest:** Improved F1-score from 0.11 → 0.23 after tuning  
- **XGBoost:** Improved F1-score from 0.16 → 0.23 after tuning  
- **Logistic Regression:** Tested but excluded from tuning due to poor performance  
- **Threshold optimization** was used to maximize **recall** (~1.0), ensuring no survival cases were missed — which is critical in medical applications.

Performance was monitored using Precision, Recall, F1-Score, and Confusion Matrices rather than Accuracy alone, since class imbalance could mislead results.

# Real-World Impact
This project shows how **machine learning can help doctors identify high-risk pancreatic cancer patients**. By predicting survival outcomes, medical teams can prioritize treatments, plan follow-ups, and reduce the risk of missing critical cases.  

# How It Was Built
- Explored patterns and correlations in patient data  
- Handled class imbalance with SMOTE  
- Built and tuned machine learning models  
- Optimized thresholds to maximize recall for survival prediction  

# Tools Used
Python | Pandas | NumPy | Scikit-learn | XGBoost | Matplotlib | Seaborn | Jupyter Notebook  

# Notes
This project focuses on **practical healthcare analytics**, showing how careful data preparation, model tuning, and threshold optimization can make predictive models **more reliable for critical medical decisions**.
