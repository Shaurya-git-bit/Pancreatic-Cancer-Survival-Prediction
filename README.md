# Pancreatic Cancer Survival Prediction
Predicting survival outcomes for pancreatic cancer patients using machine learning

## Why This Matters
Pancreatic cancer has one of the lowest survival rates among all cancers—around 13%—largely because it's often diagnosed late when symptoms are still mild. I wanted to explore whether machine learning could help doctors identify high-risk patients earlier and make better treatment decisions.

## What I Did
I analyzed a dataset of pancreatic cancer patients and built machine learning models to predict survival status. The exploratory analysis revealed some clear patterns: late-stage diagnosis (Stage 3 and 4) was strongly associated with mortality, while chemotherapy generally led to better outcomes compared to radiation or surgery alone. 

The correlations showed that survival time and stage at diagnosis were the strongest predictors, whereas most demographic and lifestyle factors had surprisingly little effect.

## Key Challenges
The biggest challenge was dealing with severe class imbalance—87% non-survivors versus only 13% survivors. Without addressing this, my models would just predict "non-survivor" for everyone and still get 87% accuracy, which is completely useless in practice. I used SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset, which made a huge difference.

The other challenge was that the relationships between features were complex and non-linear. Simple models like Logistic Regression just couldn't capture these patterns effectively.

## How the Prediction Works
I trained and optimized three models: Logistic Regression, Random Forest, and XGBoost. Logistic Regression performed poorly due to the dataset's complexity, so I focused my hyperparameter tuning on Random Forest and XGBoost.

After tuning and threshold optimization, both models improved significantly. Random Forest's F1-score jumped from 0.11 to 0.23, while XGBoost went from 0.16 to 0.23. The threshold optimization was crucial—it pushed recall to nearly 1.0, meaning the model catches almost every survival case. 

Precision is still moderate, but in medical applications, missing a survival case (false negative) could be life-threatening, so maximizing recall was the right call. I'd rather have some false positives than miss someone who could survive with proper treatment.

## Real-World Impact
This project showed me how machine learning can assist doctors in identifying high-risk pancreatic cancer patients. By predicting survival outcomes, medical teams could prioritize treatments, plan follow-ups more carefully, and reduce the risk of missing critical cases. 

The key lesson was that building a model isn't just about accuracy—it's about understanding what matters in the real world. In healthcare, the cost of different types of errors is very different.

## How It Was Built
I started by collecting and cleaning patient data, then explored patterns through correlations and visualizations. Building the models was the easier part; figuring out how to handle class imbalance and optimize thresholds took a lot of trial and error. I evaluated performance using Precision, Recall, F1-Score, and Confusion Matrices rather than just Accuracy, since accuracy is misleading with imbalanced data.

The hardest part was honestly understanding the medical context well enough to make the right modeling decisions. I spent a lot of time reading about pancreatic cancer treatment to understand why certain features mattered and what clinicians would actually need from a prediction tool.

## Tools Used
Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn, Jupyter Notebook

## What I Learned
This project taught me that machine learning in healthcare requires a completely different mindset than typical ML projects. You can't just optimize for accuracy—you have to understand the real-world consequences of your predictions. It also showed me how important domain knowledge is. Without understanding the medical context, I would have made very different (and probably wrong) modeling choices.
