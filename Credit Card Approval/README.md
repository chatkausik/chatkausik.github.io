### Credit Card Approval Prediction
<img width="961" alt="image" src="https://user-images.githubusercontent.com/13950516/162689751-fc969dda-3e58-4d0e-bb66-53c93199fce9.png">


### <img src="https://user-images.githubusercontent.com/13950516/162672483-4d953e53-2d6b-49d6-81ba-e7daa4a54351.png" width="40" height="40" /> &nbsp; Problem Statement:

A Bank wants to automate the Credit Card eligibility process based on customer detail provided while filling online application form & Credit history of customer.

They have given a problem to identify the customers segments which are eligible for Credit Card approval, so that they can specifically target these customers.

The decision of approving a credit card or loan is majorly dependent on the personal and financial background of the applicant. Factors like, age, gender, income, employment status, credit history and other attributes all carry weight in the approval decision. Credit analysis involves the measure to investigate the probability of a third-party to pay back the loan to the bank on time and predict its default characteristic. Analysis focus on recognizing, assessing, and reducing the financial or other risks that could lead to loss involved in the transaction. 

There are two basic risks: one is a business loss that results from not approving the good candidate, and the other is the financial loss that results from by approving the candidate who is at bad risk. It is very important to manage credit risk and handle challenges efficiently for credit decision as it can have adverse effects on credit management. Therefore, evaluation of credit approval is significant before jumping to any granting decision.



### <img src="https://user-images.githubusercontent.com/13950516/162672846-869bf047-63a7-489f-9b33-4f4a3beab1b2.png" width="40" height="40" /> &nbsp; Dataset
- Data Source: www.kaggle.com
- Data Sets: Two csv files – Application record and credit record.
- Data Variables: age, gender, income, education, years employed, credit history, months balance, status(default payment of not) among others.


### <img src="https://user-images.githubusercontent.com/13950516/162673233-e0f5d3ac-ccf7-430e-9a56-46e202098648.png" width="40" height="40" />&nbsp; Variable Descriptions
<img width="265" alt="image" src="https://user-images.githubusercontent.com/13950516/162690075-73bca0c0-7549-4c11-8880-ae39d8931c02.png">



### <img src="https://user-images.githubusercontent.com/13950516/162673345-5ea37d71-b9e4-47b7-aa6e-c43921d7b2d0.png" width="40" height="40" />&nbsp; Approach

<img width="945" alt="image" src="https://user-images.githubusercontent.com/13950516/162690212-7141b2b2-b01d-483b-8804-117a7d667bd7.png">

![image](https://user-images.githubusercontent.com/13950516/162690852-5c821b26-11e9-4bab-ab9a-c0aec92c87b4.png)

### Challenges
- Observation in one class was higher than the observation in other class which created a class imbalance.
- Majority class had over 35,000 observations whereas minority class had 768 observation or 78.43% majority to 21.56% minority class
- Resulting in higher accuracy in majority class and low or 0 in minority class thus failing to capture the minority class.

### Resolution
- We used synthetic minority oversampling technique(SMOTE) to deal with imbalanced classes.
- The technique generates synthetic data for the minority class.
- Its algorithm works by:
  - Choosing a minority class as the input vector.
  - Finding its k nearest neighbors (k_neighbors is specified as an argument in the SMOTE() function)
  - Choosing one of these neighbors and place a synthetic point anywhere on the line joining the point under consideration and its chosen neighbor
  - Repeating the steps until data is balanced
  - After SMOTE technique we had balanced on each class: 50-50


### <img src="https://user-images.githubusercontent.com/13950516/162673481-c1ce4edf-5240-43be-ae07-e7ef061be0c6.png" width="40" height="40" />&nbsp; Conclusion
- We split the dataset into two subsets –Train (80%) and Test (20%)
- We took 2 passes at the Machine learning models, one with initial data and other with balanced data after performing SMOTE technique.
- SMOTE Sampling methods provided much better results compared to raw data.
- XGBoost Model is giving the highest accuracy of 84.14 %. 
Model
Accuracy
Logistic Model Accuracy         
50.60 %
Decision Tree Model Accuracy
69.55 %
Random Forest Model Accuracy
76.00 %
Support Vector Classifier Accuracy
49.79 %
KNN Model Accuracy
45.98 %
XGBoost Model Accuracy
84.14 %
<img width="463" alt="image" src="https://user-images.githubusercontent.com/13950516/162691472-edd84f6e-ae4a-4c4f-9381-90770fb1eec3.png">
