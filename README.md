# Analysis Overview

In this project, we use machine learning to build and evaluate models to predict credit risk.

We used the following methods:

•	Oversample the data using the RandomOverSampler and SMOTE algorithms.

•	Undersample the data using the ClusterCentroids algorithm.

•	Use a combinatorial approach of over-and undersampling using the SMOTEENN algorithm.

•	Compare two machine learning models that reduce bias, BalancedRandomForestClassifier , and EasyEnsembleClassifier.

We will evaluate the performance of these models and make recommendations on whether they should be used to predict credit risk.

# Resources

•	Data Source: LoanStats_2019Q1.csv

•	Software: Python, Anaconda Navigator, Jupyter Notebook 


# Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)


## RandomOverSampler model


![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/RandomOverSampler%20model_balanced_accuracy_score.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/RandomOverSampler%20model_conf_Mat.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/RandomOverSampler%20model_Classification_report.png)


The balanced accuracy score is 64.7%.

The high_risk precision is about 1% only with 69% sensitivity which makes a F1 of 2% only.

Due to the high number of the low_risk population, its precision is 100% with a sensitivity of 60%.


## SMOTE model


![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/SMOT%20model_balanced_accuracy_score.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/SMOT_model_conf_Mat.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/SMOT%20model_Classification_report.png)


The balanced accuracy score is 66%.

The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.

Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 69%.




## SMOTEENN model

![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Undersampling_Smoteenn_model_balanced_accuracy_score.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Undersampling_Smoteenn_model_conf_Mat.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Undersampling_Smoteenn_model_Classification_report.png)

Here the balanced accuracy score is 64%.

The high_risk precision is still 1% only with 72% sensitivity which makes a F1 of 2%.

Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 57%.

## BalancedRandomForestClassifier model

![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Balanced%20Random%20Forest%20Classifier%20model_balanced_accuracy_score.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Balanced%20Random%20Forest%20Classifier%20model_conf_Mat.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Balanced%20Random%20Forest%20Classifier%20model_Classification_report.png)

The balanced accuracy score improved to about 79%.

The high_risk precision is still low at 3% only with 70% sensitivity which makes a F1 of only 6%.

Due to a lower number of false positives, the low_risk sensitivity is now 87% with 100% presicion.


## EasyEnsembleClassifier model


![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Easy%20Ensemble%20AdaBoost%20Classifier%20model_balanced_accuracy_score.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Easy%20Ensemble%20AdaBoost%20Classifier%20model_conf_Mat.png)
![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Easy%20Ensemble%20AdaBoost%20Classifier%20model_Classification_report.png)

The balanced accuracy score is about 93%.

The high_risk precision is still low at 9% only with 92% sensitivity which makes a F1 of only 16%.

Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.


# Summary

We can see the summary of all the models used for this analysis in the table below:

![](https://github.com/ALEIN3/Credit_Risk_Analysis/blob/main/Images/Summary.png)


After checking all the used modules to perform the credit risk analysis, we can see weak precision in determining if credit risk is high.
The Ensemble models showed more improvement, especially on the sensitivity of the high risk credits. The EasyEnsembleClassifier model delivered the best prediction in every measure. It shows a recall of 92% that means that it detected 92% of the cases of the high risk credit. On the other hand, with a low precision, a lot of the cases that actualy  low risk credits are still falsely detected as high risk, which will let the bank miss many business opportunities in the future.
For the above reasons, I would not recommend the bank to use any of these models to predict credit risk.
In the end, the financial organization strategy defines the priorities in determining the lending policy


