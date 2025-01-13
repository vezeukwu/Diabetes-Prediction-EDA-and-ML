# Diabetes-Prediction-EDA-and-ML

![image](https://github.com/user-attachments/assets/404824a1-89a8-4609-ace5-aec236e039fb)


Stark Health Clinic aims to develop a robust diabetes prediction model to accurately identify individuals at risk of developing diabetes allowing for timely and targeted preventive measures.

## Project Description:
Stark Health Clinic is a private owned hospital located in Lagos, Nigeria. It was founded in 1972 by an astute medical professional. The hospital provides a wide range of medical services, including but not limited to general medicine, surgery, pediatrics, obstetrics and gynecology. The Hospital is known for its state-of-the-art facilities, modern equipment, and highly skilled medical professionals. It was then observed that an increasing number of patients presented themselves with complains including chest pains, blood pressure related issues, cholesterol level declines and stroke in some cases, hence an inquiry into the possibility of patients being at risk of a heart disease.

This project focuses on exploring and analyzing a heart disease dataset, using exploratory data analysis (EDA) and machine learning techniques to predict the likelihood of heart disease in individuals. The primary goal is to uncover key patterns and relationships within the data that can assist in identifying at-risk patients. Through Exploratory Data Analysis, I gained insights into factors such as age, cholesterol levels, blood pressure, and other clinical attributes. I then applied machine learning algorithms, to predict the probability of a patient having a heart disease, aiming to improve early detection and inform better clinical decision-making.

## Dataset Description
Source: Collected data from approximately 100,000 medical patients evaluated for diabetes.

Target Variable: Binary outcome indicating diabetes presence (1) or absence (0).

Independent Variables: information believed to have an influence on the outcome to predict. Eg Age, Hypertension, Blood glucose level etc

This Diabetes Dataset contains information about 100,000 medical patients evaluated for the presence of diabetes. Each record provides details on different patient characteristics that may influence the likelihood of a diabetes diagnosis. The dataset includes the following attributes:

## FEATURE NAME & DECRIPTION OF THE DATASET
gender - Gender of the individual (e.g., 'Male', 'Female').

age - Age of the individual in years.

hypertension - Whether the individual has hypertension (0 = No, 1 = Yes).

heart_disease - Whether the individual has heart disease (0 = No, 1 = Yes).

smoking_history - Smoking history of the individual (e.g., 'never', 'former', 'current').

bmi - Body Mass Index (BMI) of the individual.

HbA1c_level - Hemoglobin A1c level, indicating average blood sugar levels over the past 3 months.

blood_glucose_level - Current blood glucose level of the individual.

diabetes - Target variable indicating whether the individual has diabetes (0 = No, 1 = Yes).

## Data Preparation (EDA)
Loading the Data
Data Cleaning
Handling Missing Data
Model Building and Predictions
Summarizing and Visualization
Model Evaluation Summary

Data Cleaning and Transformation I checked for missing values and data inconsistencies in the dataset, standardizing data to maintain model integrity. Some outliers were noted and converted to their positive counterparts as they were suspected to be entry errors. This ensured logical consistency across the dataset.

Model Building The data was split into training and testing sets, with 80% of the data used for training the model and 20% for testing. This provided an unbiased evaluation of the model’s performance. I reviewed logistic regression and further examined 4 other machine algorithms to determine the model with optimal effectiveness in other to reduce issues arising from false predictions as human lives are involved and the project essence is to achieve early detection and avoid needless deaths.

Model Evaluation The Logistic Regression model, along with the Random Forest and other models, achieved an exceptional performance, delivering 100% accuracy and precision. This indicates that the models were not only able to correctly classify all instances but also had no false positives.

Based on the displayed results, here’s an evaluation of the model’s performance:

Accuracy Score:
All models have achieved close to or exactly 100% accuracy.
This suggests that the models are highly effective at predicting the correct labels across the dataset.

Precision:
Precision for all models is 100%.
This indicates that when a positive prediction is made, it is always correct. There are no false positives in the predictions.

Recall:
Most models have 100% recall, except for the k-Nearest Neighbors model with 97.44% recall.
This means that most models have successfully identified all actual positive instances (low or no false negatives), while the k-Nearest Neighbors model missed a small portion of positive cases.

ROC Score:
The ROC scores for all models are close to 100%, showing that they have excellent discrimination ability between positive and negative classes.

2. Confusion Matrix Analysis:
The confusion matrix shows:

True Positives (TP): 1721 instances were correctly predicted as positive.
True Negatives (TN): 17,509 instances were correctly predicted as negative.
False Positives (FP): 0 instances were incorrectly predicted as positive.
False Negatives (FN): 0 instances were incorrectly predicted as negative.
This indicates perfect performance, with all predictions being correct.


## Conclusion
The evaluation of the models demonstrates exceptional performance, with the majority achieving perfect or near-perfect accuracy, precision, recall, and ROC scores. The confusion matrix further confirms the robustness of the models, showing no false positives or false negatives, and a complete alignment between actual and predicted values. Among all models, XGBoost, Random Forest, Logistic Regression, and Decision Tree have consistently delivered flawless predictions, making them strong candidates for deployment in real-world scenarios.

The slightly lower recall of the k-Nearest Neighbors model indicates it may not capture all positive cases as effectively as the other models, though its overall performance remains strong.

However, the uniformly high scores suggest the possibility of data imbalance or overfitting. To ensure the reliability and generalizability of these results, additional validation through cross-validation and testing on diverse datasets is recommended. If confirmed robust, these models are well-suited for deployment in applications requiring high accuracy and reliability.

The XGBoost classifier, with its combination of efficiency and performance, is particularly well-positioned as a top choice for implementation.
