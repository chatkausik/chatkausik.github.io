# American Express - Default Prediction Predict if a customer will default in the future

The project aims to leverage machine learning techniques to build a predictive model that assesses the probability of a customer defaulting on their credit card balance within American Express. By accurately predicting default events, American Express can optimize lending decisions, enhance risk management strategies, and improve the overall customer experience. 

![Customer Segmentation](/assets/img/AMEX.jpeg)

## 1.0 Business Problem

* Whether out at a restaurant or buying tickets to a concert, modern life counts on the convenience of a credit card to make daily purchases. It saves us from carrying large amounts of cash and also can advance a full purchase that can be paid over time. How do card issuers know we’ll pay back what we charge? That’s a complex problem with many existing solutions—and even more potential improvements, to be explored in this competition.

* Credit default prediction is central to managing risk in a consumer lending business. Credit default prediction allows lenders to optimize lending decisions, which leads to a better customer experience and sound business economics. Current models exist to help manage risk. But it's possible to create better models that can outperform those currently in use.

* American Express is a globally integrated payments company. The largest payment card issuer in the world, they provide customers with access to products, insights, and experiences that enrich lives and build business success.

* I will apply machine learning skills to predict credit default. Specifically, I will leverage an industrial scale data set to build a machine learning model that challenges the current model in production. Training, validation, and testing datasets include time-series behavioral data and anonymized customer profile information. 


## 2.0 Datasets

The objective is to predict the probability that a customer does not pay back their credit card balance amount in the future based on their monthly customer profile. The target binary variable is calculated by observing 18 months (about 1 and a half years) performance window after the latest credit card statement, and if the customer does not pay due amount in 120 days (about 4 months) after their latest statement date it is considered a default event. 

The dataset contains aggregated profile features for each customer at each statement date. Features are anonymized and normalized, and fall into the following general categories: 

D_* = Delinquency variables 

S_* = Spend variables 

P_* = Payment variables 

B_* = Balance variables 

R_* = Risk variables 

with the following features being categorical: 

['B_30', 'B_38', 'D_114', 'D_116', 'D_117', 'D_120', 'D_126', 'D_63', 'D_64', 'D_66', 'D_68'] 
 

Task is to predict, for each customer_ID, the probability of a future payment default (target = 1). 

## 3.0 Methods

The project will follow a structured approach: 

1. Data Exploration and Preprocessing: This phase involves loading the datasets, handling missing values, outliers, and performing exploratory data analysis (EDA) to understand the distributions and relationships between features and the target variable. 

2. Feature Engineering: Feature engineering will be crucial for creating meaningful predictors. Techniques such as one-hot encoding for categorical variables, creating new features based on ratios, trends, or rolling averages, and normalization or scaling of numerical features will be applied. 

3. Model Selection and Training: We will experiment with various machine learning algorithms suitable for binary classification, including Random Forest, Gradient Boosting Machines (GBM), XGBoost, and possibly deep learning models like neural networks. Using techniques like grid search or random search will optimize model performance. 

4. Model Evaluation: The evaluation metric, a combination of Normalized Gini Coefficient and default rate captured at 4%, will be used to assess model performance. Cross-validation and validation sets will help in evaluating the model's generalization capability. 

5. Prediction and Submission: Once the model is trained and evaluated, we will use it to predict the probability of default for customers in the test dataset and prepare submissions in the required format. 

## Ethical Considerations

Ethical considerations in this project include ensuring data privacy and confidentiality by anonymizing customer information, addressing potential biases in the data or model predictions to avoid discriminatory outcomes, and transparently communicating the purpose and implications of the credit default prediction model to stakeholders, including customers. 
 
 ## Challenges/Issues

Challenges may arise from handling imbalanced data due to the subsampling of negative labels, feature selection from many variables to avoid overfitting, addressing potential model interpretability issues, and ensuring model fairness and transparency. 

