# Credit Risk Analysis using Machine Learning Models

## Overview

In this project we will to take a look at how all the factors from the loan_stats csv help predict whether someone is low or high risk candidate. We used imbalanced-learn and scikit-learn libraries to perform supervised machine-learning. We used various models and evalute them using a resampling method. In the first couple of models data was oversampled using RandomOversampler and SMOTE algorithms. Next, data was undersampled with the ClusterCentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, two machine learning models were compared to see which minimized bias: BalancedRandomForestClassifier and EasyEnsembleClassifier.

## Results

*Figure 1: Oversampling with RandomOversampler*

![Oversampling](https://user-images.githubusercontent.com/102441140/183497610-6ed5a1ba-1395-49ee-af0a-552342ecd97a.png)

**Naive Random Oversampling results: The balanced accuracy is 64%, the precision for the high_risk has a very low positivity at 1% and the recall is 70%**

*Figure 2: Oversampling with SMOTE*

![SMOTE_oversampling](https://user-images.githubusercontent.com/102441140/183497732-930f9768-a438-440e-ba57-37f2bd6c30e3.png)

**SMOTE Oversampling results: The balanced accuracy is 66%, the precision for the high_risk has a very low positivity at 1% and the recall is 63%**

*Figure 3: Undersampling*

![Undersampling](https://user-images.githubusercontent.com/102441140/183497860-dadeeced-29a1-4138-a18b-0008fdc91a32.png)

**Undersampling results: The balanced accuracy is 52%, the precision for the high_risk has a very low positivity at 1% and the recall is 69%**

*Figure 4: Under and Oversampling using SMOTEENN*

![UnderAndOverSampling](https://user-images.githubusercontent.com/102441140/183497952-32f22fa5-f0d5-4334-88a5-1737904169b6.png)

**Under and Oversampling results: The balanced accuracy is 65%, the precision for the high_risk has a very low positivity at 1% and the recall is 73%**

*Figure 5: BalancedRandomForest Classifier*

![BalancedRandomForest](https://user-images.githubusercontent.com/102441140/183498065-4acc1ca1-40ea-41da-83f9-c6a75445c446.png)

**BalancedRandomForest Classifier results: The balanced accuracy is 78%, the precision for the high_risk has a very low positivity at 3% and the recall is 87%**

*Figure 6: EasyEnsemble Classifier*

![Easy Ensemble](https://user-images.githubusercontent.com/102441140/183498270-decda663-4f5b-4539-b83f-e3109c88e0fe.png)

**EasyEnsemble Classifier results: The balanced accuracy is 93%, the precision for the high_risk is at 9% and the recall is 92%**

## Summary

In the first four models data was undersampled, oversampled and were under and oversampled to try and determine which model is best at predicting which loans have the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. However, it is apparent that the 'Easy Ensemble' model provides the best results as we are interested in the highest accuracy and the highest % coverage for the high_risk, and the highest recall for the high_risk. The significance of prioritizing the high_risk as opposed the low_risk is because the goal of the machine-learning model is to detect specifically 'high_risk'.
