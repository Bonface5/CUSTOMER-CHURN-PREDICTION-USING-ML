# CUSTOMER-CHURN-PREDICTION-USING-ML
Capstone Project 
PROJECT SUMMARY: Customer Churn Prediction Using Machine Learning
1. Introduction
Customer churn is a critical challenge for subscription-based businesses. Accurately predicting which customers are likely to leave enables a company to take preventative action, improve customer retention, and increase overall profitability.
This project builds a machine learning-based churn prediction system to classify customers as either likely to churn or remain active. The goal is to identify early warning signs using historical customer behavior data, and then provide actionable insights for the business.

2. Business Objective
The main objectives were:
•	Predict churn using machine learning classification models.
•	Compare model performance using F1-score, ROC-AUC, and optimal decision thresholds.
•	Identify key drivers of churn through feature importance and model interpretation.
•	Deliver a deployable prototype for real-world use by the customer retention team.

3. Data Overview
The dataset contained multiple customer attributes, including:
•	Demographics: age, gender, senior citizen
•	Account Information: tenure, contract type, payment method, monthly charges
•	Services: phone, internet, streaming, protection add-ons
•	Target Variable: Churn (Yes/No)
Key preprocessing steps:
•	Handling missing values
•	Encoding categorical variables
•	Balancing the target using class weights
•	Feature scaling (for Logistic Regression)
•	Train-test split (80/20)

4. Modeling Approach
Four machine learning models were trained and evaluated:
1.	Logistic Regression
2.	Random Forest Classifier
3.	XGBoost Classifier
4.	LightGBM Classifier
To improve fairness and scoring stability:
•	Each model was tuned with threshold optimization to maximize F1-score.
•	Performance was measured on the test set only.
•	Evaluation metrics:
o	F1-Score (primary metric due to churn imbalance)
o	ROC-AUC
o	Best Decision Threshold

5. Model Performance Summary
Model	Test F1	ROC-AUC	Best Threshold
LightGBM	0.66	0.64	0.99
Random Forest	0.6562	0.6365	0.99
XGBoost	0.6562	0.6365	0.99
Logistic Regression	0.6385	0.5908	0.01

6. Best Model: LightGBM
LightGBM achieved the highest performance:
•	F1-Score: 0.66 (highest)
•	ROC-AUC: 0.64 (highest)
•	Strong performance under class imbalance
•	Fast training and good generalization
This makes LightGBM the best model for deployment in the churn prediction system.

7. Key Insights From the Model LightGBM
Based on the feature importance visualization, the LightGBM model identified the following top predictors of customer churn:
1. Customer Age – Younger customers churn more
2. Tenure – New customers are at highest risk
3. Support Calls – Frequent complaints strongly signal churn
4. Usage Frequency – Low/declining usage predicts churn
5. Last Interaction – Customers who haven’t engaged recently are drifting away
6. Payment Delay – Late payments correlate with churn
These features give the business clear, actionable targets for reducing churn.


8. Final Deliverables
•	Cleaned dataset ready for production use
•	Jupyter Notebook with full EDA, modeling, evaluation, and interpretations
•	Model performance dashboard (comparison table)
•	Presentation slides summarizing the work (up next)
•	A working prototype architecture

10. Conclusion
The project successfully developed a robust machine learning system for predicting customer churn. LightGBM outperformed all other models and is recommended for deployment due to its superior F1-score, stability, and ability to handle non-linear relationships in the data.
This model gives the company a practical tool to:
•	Reduce churn
•	Improve customer satisfaction
•	Increase long-term revenue
•	Make data-driven retention decisions

