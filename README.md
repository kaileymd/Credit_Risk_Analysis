# Credit Risk Analysis
This analysis aims to train a supervised machine learning model to accurately predict credit worthiness based on a credit card dataset from Lending Club. This analysis will review the six models tested to see if any performs well enough to be recommended for use.

## Results
After cleaning the data and splitting it into training and testing variables, I trained the models using oversampling, undersampling, etc.

#### Naive Random Oversampling
![ROS.png](https://github.com/kaileymd/Credit_Risk_Analysis/blob/main/images/ROS.png)

Using this model, I was able to reach:
- a balanced accuracy score of 67%
- a precision of 100% for the majority class, but 1% for the minority class
- a recall score between 60 and 75% for both classes

Due to its extremely low precision, I would not recommend this model.

#### SMOTE Oversampling
![SMOTE.png](https://github.com/kaileymd/Credit_Risk_Analysis/blob/main/images/SMOTE.png)

Using this model, I was able to reach:
- a balanced accuracy score of 66%
- a precision of 100% for the majority class, but 1% for the minority class
- a recall score between 60 and 70% for both classes

Due to its extremely low precision, I would not recommend this model.

#### Cluster Centroids Undersampling
![Cluster_Centroids.png](https://github.com/kaileymd/Credit_Risk_Analysis/blob/main/images/Cluster_Centroids.png)

Using this model, I was able to reach:
- a balanced accuracy score of 54%
- a precision of 100% for the majority class, but 1% for the minority class
- a recall score of 40% for the majority class and 69% for the minority class

Due to its extremely low accuracy and precision, I would not recommend this model.

#### Combination (Over and Under) Sampling with SMOTEENN
![SMOTEENN.png](https://github.com/kaileymd/Credit_Risk_Analysis/blob/main/images/SMOTEENN.png)

Using this model, I was able to reach:
- a balanced accuracy score of 68%
- a precision of 100% for the majority class, but 1% for the minority class
- a recall score of 40% for the majority class and 69% for the minority class

Due to its extremely low accuracy and precision, I would not recommend this model.

#### Balanced Random Forest Classifier
![RBF.png](https://github.com/kaileymd/Credit_Risk_Analysis/blob/main/images/RBF.png)

Using this model, I was able to reach:
- a balanced accuracy score of 76%
- a precision of 100% for the majority class, but 3% for the minority class
- a recall score of 89% for the majority class and 64% for the minority class

Due to its extremely low precision, I would not recommend this model. 

#### Easy Ensemble AdaBoost Classifier
![EEC.png](https://github.com/kaileymd/Credit_Risk_Analysis/blob/main/images/EEC.png)

Using this model, I was able to reach:
- a balanced accuracy score of 91%
- a precision of 100% for the majority class, but 5% for the minority class
- a recall score of 90% for the majority class and 93% for the minority class

Although the precision score is still very low, the recall of 93% does mean that most of the fraudulent cases in this set were caught, even if the model is over-predicting fraud cases. If a bank needed to use any model, I would choose this one.

## Summary
All of the tested models had very low precision for the minority class, which means that the cases selected as 'positive fraud cases' were usually incorrect. Also, the percentage of actual fraud cases that were caught (as shown by the recall score) were mostly unsatisfactory to make up for that low of a precision score.

With all of that taken into account, I would recommend the Easy Ensemble AdaBoost Classifier model for use since over 90% of the fraud cases were caught. While the precision is still low, it is more important that the true cases of fraud are caught, and therefore over-predicting fraud is a less concerning issue.
