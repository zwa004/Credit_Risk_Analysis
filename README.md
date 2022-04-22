# Credit_Risk_Analysis

## Overview
The purpose of this analysis is to classify loan applications as either high risk or low risk based on a large number of independent variables. The "target", or dependent variable, was the "loan status", while there were 86 distinct "features", or independent vriables.  

## Results
6 different machine learning models were evaluated using the imblearn function classification_report_imbalanced by 3 metrics: precision (% of correct predictions), recall (% all true high risk loans found), and F1 score (a weighted average of true low risk loans where 1 is best and 0 is worst). Low risk loans were encoded as "0" and high risk loans were encoded as "1"



### Naive Random Oversampling (NRO)
This model scored 0.01 precision for low risk applications and 1 for high risk while its ability to find all low an high risk was 0.62 and 0.64, respectively. NRO had an F1 score of 0.02 for low risk and 0.78 for high risk loans. It has an accuracy of 63%. 

![image](https://user-images.githubusercontent.com/91761393/164740716-bdc61ac6-8b07-4ab8-b445-22ca296df34f.png)

### Synthetic Minority Oversampling Technique (SMOTE) 
This model was as precise as NRO for each risk of loan. However, SMOTE was evaluated to recall low risk loans at 0.51 and high risk at .068. It also recorded an F1 of 0.02 for low risk and 0.81 for high risk loans. It has an accuracy of 59%.

![image](https://user-images.githubusercontent.com/91761393/164740626-744ee22b-8bcd-423c-a112-e57700cf4571.png)


### Clustered Centroid
This model recorded a rrecision of 1 for finding high risk loans and 0.01 for finding low risk loans. For recall, the clustered centroid model found 56% of low risk loans and 46% of high risk. The F1 score for this model was 0.01 for low and 0.63 for high risk loans. This model has an accuracy score of 51%

![image](https://user-images.githubusercontent.com/91761393/164740535-16ddcb25-ea91-4783-8dff-ddbefdb2533a.png)


### Synthetic Minority Oversampling Technique (and) Nearest Edited Neighbor SMOTEENN
In this model, the low risk loans were found with a precision of 0.01 while high risks were found at a precision of 1. The recall of SMOTEENN for low risk loans was 0.7 and high risk loans was 0.57. This model recorded F1 values of 0.02 for low risk loans and 0.73 for high risk loans. It has an accuracy score of 63%

![image](https://user-images.githubusercontent.com/91761393/164740347-42a3eacc-d460-4c99-9103-aef8c38fb1df.png)


### Random Forest
The random forest model had a precision rate of 1 for low risk loans and 0.04 for high risk loans. The Random Forest method found 91% of low risk loans and 66% of high risk loans. The F1 score was 0.95 for low risk loans and 0.07 for high risk loans. Random Forest had an accuracy score of 77%

![image](https://user-images.githubusercontent.com/91761393/164739291-e67453f0-c8eb-4795-acaf-5dde97f390ff.png)

The following image ranks the most influential features (independent variables)
![image](https://user-images.githubusercontent.com/91761393/164739521-ba035dda-69aa-400e-88bb-add0fff826b1.png)


### Adaptive Boosting Ensemble
This model reported high risk loans with a precision of 8% and low risk with a precision of 100%. Its recall was 0.87 for high risk loans an 0.95 for low risk. The F1 value for this model was 0.15 for high risk and 0.97 for low risk. It had an accuracy score of 91%

![image](https://user-images.githubusercontent.com/91761393/164740220-8ffeff1a-3680-48bf-9903-cc1d957d4cfc.png)



## Summary
In terms of low risk loans, the both the Random Forest and Adaptive Boosting models scored over 0.95 making them highly reliable. I can't recommend any of the 6 tested machine learning models for finding high risk loans as none scored over 0.15. The most accurate of the models was the Adaptive Boosting model while the most accurate of the under/over sampling models was the SMOTEENN model. The under/over sampling model with the best F1 score was the SMOTE model (0.02 high and 0.81 low risk) while the most accurate of the 3 was the SMOTEENN with a score of 63%. If the company is trying to find high risk loans, I can't recommend any of the models. 
