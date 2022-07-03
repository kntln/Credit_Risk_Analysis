# Credit Risk Analysis
![Credit Risk](https://media.marketrealist.com/brand-img/3s7UQMyYo/2160x1130/uploads/2019/10/bank-credit-risk.jpg)
## Overview of the Analysis
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, different techniques will be needed to employ to train and evaluate models with unbalanced classes. Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the data will be oversampled using the **`RandomOverSampler`**  and **`SMOTE`**  algorithm. In addition, the data will undergone undersampling using the **`ClusterCentroids`** algorithm. Then, a combination approach of over- and undersampling using the **`SMOTEENN`** algorithm will also be employed. Next, two new machine learning models that reduce bias, **`BalancedRandomForestClassifier`** and **`EasyEnsembleClassifier`** will be compared to predict credit risk. The performance of these models will then be evaluated and based on the results, a writen recommendation on whether the machine learning models should be used to predict credit risk.

## Result

### Naive Random Oversampling
- The balanced accuracy score for **`RandomOverSampler`** is 60.4%.

![naive_random_oversampling_accuracy.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/naive_random_oversampling_accuracy.png)

- For High Risk, the precision rate is 1%, the recall rate is 58% and an F1 score of 2%.
- For Low Risk, the precision rate is 100%, the recall rate is 62% and an F1 score of 77%.

![naive_random_oversampling.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/naive_random_oversampling.png)


### SMOTE
- The balanced accuracy score for **`SMOTE`** is 65.8%.

![smote_oversampling_accuracy.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/smote_oversampling_accuracy.png)

- For High Risk, the precision rate is 1%, the recall rate is 63% and an F1 score of 2%.
- For Low Risk, the precision rate is 100%, the recall rate is 68% and an F1 score of 81%.

![smote_oversampling.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/smote_oversampling.png)


### Cluster Centroids - Undersampling
- The balanced accuracy score for **`ClusterCentroids`** is 54.4%.

![undersampling_accuracy.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/undersampling_accuracy.png)

- For High Risk, the precision rate is 1%, the recall rate is 69% and an F1 score of 1%.
- For Low Risk, the precision rate is 100%, the recall rate is 39% and an F1 score of 57%.

![undersampling.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/undersampling.png)

### SMOTEENN
- The balanced accuracy score for **`SMOTEENN`** is 64.8%.

![SMOTEENN_accuracy.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/SMOTEENN_accuracy.png)

- For High Risk, the precision rate is 1%, the recall rate is 72% and an F1 score of 2%.
- For Low Risk, the precision rate is 100%, the recall rate is 57% and an F1 score of 73%.

![SMOTEENN.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/SMOTEENN.png)


### Balanced Random Forest Classifier
- The balanced accuracy score for **`BalancedRandomForestClassifier`** is 78.9%.

![balanced_random_forest_classifier_accuracy.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/balanced_random_forest_classifier_accuracy.png)

- For High Risk, the precision rate is 3%, the recall rate is 70% and an F1 score of 6%.
- For Low Risk, the precision rate is 100%, the recall rate is 87% and an F1 score of 93%.
- The feature that has the most importance is the "total_rec_prncp" which weighted a total of 7.9%. 

![balanced_random_forest_classifier.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/balanced_random_forest_classifier.png)
![balanced_random_forest_classifier_rank.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/balanced_random_forest_classifier_rank.png)


### Easy Ensemble Classifier
- The balanced accuracy score for **`EasyEnsembleClassifier`** is 93.2%.

![easy_ensemble_classifier_accuracy.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/easy_ensemble_classifier_accuracy.png)

- For High Risk, the precision rate is 9%, the recall rate is 92% and an F1 score of 16%.
- For Low Risk, the precision rate is 100%, the recall rate is 94% and an F1 score of 97%.

![easy_ensemble_classifier.png](https://github.com/kntln/Credit_Risk_Analysis/blob/main/figures/easy_ensemble_classifier.png)


## Summary
In summary, out of all the six machine learning models, **`EasyEnsembleClassifier`** had the most promising results in terms of identifying high risk loans. The second was **`BalancedRandomForestClassifier`**, the third, was **`SMOTE`**, fourth was **`SMOTEENN`**, fifth was **`RandomOverSampler`** and lastly **`ClusterCentroids`**. For this type of credit risk analysis, **`EasyEnsembleClassifier`** machine learning model is recommended due to its high accuracy, precision, recall, and F1 score. However, please keep in mind that  **`EasyEnsembleClassifier`** may not always work for different type of analysis and other machine learning models may fare better. 
