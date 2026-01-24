# Pancreatic Cancer Survival Prediction
Predicting survival outcomes for pancreatic cancer patients using machine learning

# Why This Matters
Pancreatic cancer has one of the lowest survival rates among all cancers, around 13%, because it’s often diagnosed late when symptoms are mild. Being able to predict survival status early can help doctors make better treatment decisions and provide timely care to patients.

# What I Did
I analyzed a dataset of pancreatic cancer patients and built machine learning models to predict survival status. Exploratory data analysis revealed that late-stage diagnosis, particularly Stage 3 and 4, is associated with high mortality, while chemotherapy generally leads to better outcomes compared to radiation or surgery. Correlations showed that survival time and stage at diagnosis are the strongest predictors, whereas most demographic and lifestyle factors had little effect.

# Key Challenges
The dataset was highly imbalanced, with 87% non-survivors and only 13% survivors. Without addressing this, models would perform well on the majority class but fail to predict survivors accurately, which could be dangerous in real-life applications. I used SMOTE (Synthetic Minority Oversampling Technique) to balance the data. The relationships between features were also complex and non-linear, making simple models like Logistic Regression less effective.

# How the Prediction Works
I trained and optimized three models: Logistic Regression, Random Forest, and XGBoost. Logistic Regression performed poorly due to the dataset's complexity and was not included in hyperparameter tuning. Random Forest and XGBoost showed significant improvement after tuning and threshold optimization. Random Forest’s F1-score increased from 0.11 to 0.23, while XGBoost improved from 0.16 to 0.23. Threshold optimization maximized recall to nearly 1.0, ensuring that no survival cases were missed, which is critical in medical settings. Precision remained moderate, but recall is the priority when missing a positive case could be life-threatening.

# Real-World Impact
This project demonstrates how machine learning can assist doctors in identifying high-risk pancreatic cancer patients. By predicting survival outcomes, medical teams can prioritize treatments, plan follow-ups, and reduce the risk of missing critical cases. The focus was on developing models that are not only accurate but also actionable in real healthcare scenarios.

# How It Was Built
I collected and cleaned patient data, explored patterns through correlations and visualizations, and trained machine learning models. The models were fine-tuned for optimal performance, and threshold optimization was applied to maximize recall. Performance was evaluated using Precision, Recall, F1-Score, and Confusion Matrices, rather than Accuracy alone, to ensure reliability in this high-stakes application.

# Tools Used
Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn, Jupyter Notebook

# Notes
This project emphasizes practical healthcare analytics. It shows how careful data preparation, handling class imbalance, and optimizing model thresholds can make predictive models more reliable and useful for real-world medical decision-making.
