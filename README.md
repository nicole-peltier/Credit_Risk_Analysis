# Credit_Risk_Analysis

## Overview
The purpose of this analysis was to 
- oversample the data using RandomOverSample and SMOTE algorithms
- undersample the data usong ClusterCentroids algorithm
- use a combinatorial approach of over and undersampling using the SMOTEENN algorithm
- compare the two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk
- evaluate the performance of these models

## Results

#### RandomOverSample Model

![randomoversample](https://github.com/nicole-peltier/Credit_Risk_Analysis/blob/main/images/Naive%20Random%20Oversampling.png)
- The balanced accuracy score is 65%
- The high-risk precision is about 1% with only 72% sensitivity which makes F1 about 2%
- Due to the high number of low_risk population, the precision is 99% with a sensitivity of 59%


#### SMOTE Model
![SMOTE](https://github.com/nicole-peltier/Credit_Risk_Analysis/blob/main/images/SMOTE.png)
- The balanced accuracy score is 66%
- The high-risk precision is about 1% with only 63% sensitivity which makes F1 about 2%
- Due to the high number of low_risk population, the precision is 99% with a sensitivity of 69%

#### ClusterCentroid Model
![clustercentroid](https://github.com/nicole-peltier/Credit_Risk_Analysis/blob/main/images/Cluster%20Centroids.png)
- The balanced accuracy score is 54%
- The high-risk precision is about 1% with only 69% sensitivity which makes F1 about 1%
- Due to the high number of false positives, the precision is 99% with a sensitivity of 40%

#### SMOTEENN Model
![smoteenn](https://github.com/nicole-peltier/Credit_Risk_Analysis/blob/main/images/SMOTEENN.png)
- The balanced accuracy score is 64%
- The high-risk precision is about 1% with only 79% sensitvity which makes F1 about 2%
- Due to the high number of false positives, the precision is about 99% with a sensitivity of 57%

#### BalancedRandomForestClassifier Model
![balancedrandomforest](https://github.com/nicole-peltier/Credit_Risk_Analysis/blob/main/images/Balanced%20Random%20Forest.png)
- The balanced accuracy score is 79%
- The high-risk precision is about 3% with 70% sensitivity which makes F1 about 6%
- Due to the low number of false positives, the low_risk sensitivity is now 87% with 100% precision

#### EasyEnsembleClassifier Model
![easyensemble](https://github.com/nicole-peltier/Credit_Risk_Analysis/blob/main/images/Easy%20Ensemble%20Classifier%20Model.png)
- The balanced accuracy score is about 93%
- The high-risk precision is 9% with 92% sensitivity which makes F1 about 16%
- Due to a low number of false positives, the low-risk sensitivity is now 94% with 100% precision


## Summary
The models used to preform the credit risk analysis show weak precision in determining if a credit risk is high. The EasyEnsembleClassifier Model was an improvement on the sensitivity of the high-risk credits. The EasyEnsembleClassifier Model shows a recall of 92% therefore it detects a majority of all high risk credit. However, with a low precision, low-risk credits are falsley detected as high-risk which could cause a problem for the banks. This of course is not as big as an issue. Therefore, the best model out of the choices would be the EasyEnsembleClassifier Model.  
