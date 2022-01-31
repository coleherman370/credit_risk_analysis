# Overview

The purpose of this project is to explore variopus machine learning modules for the use of assessing credit application approvals. Various machine learning models were produced and assessed for which one made the most accurate predictions.

## Results

### Oversampling Techniques

#### Naive Random Oversampling

- From sklearn.metrics; the balanced accuracy score: 62.9%
- high risk f1 score: 2%
- high risk precision: 1%
- recall 57%

<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/naiveOversamplingCM.png"/>
</p>
<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/naiveOversamplingCR.png"/>
</p>

#### SMOTE Oversampling

- From sklearn.metrics; the balanced accuracy score: 62.7%
- high risk f1 score: 2%

<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/naiveOversamplingSmoteCM.png"/>
</p>
<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/naiveOversamplingSmoteCR.png"/>
</p>

### Undersampling Techniques

#### Cluster Centroids

- From sklearn.metrics; the balanced accuracy score: 51.7%
- high risk f1 score: 1%

<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/undersamplingClusterCentroidsCM.png"/>
</p>
<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/undersamplingClusterCentroidsCR.png"/>
</p>

### Combination (Over & Under) Sampling

#### SMOTEEN

- From sklearn.metrics; the balanced accuracy score: 64.1%
- high risk f1 score: 2%

<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/combinationSMOTEENCM.png"/>
</p>
<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/combinationSMOTEENCR.png"/>
</p>

### Ensemble Learners

#### Balanced Random Forest

- From sklearn.metrics, the balanced_accuracy_score = 78.7%.
- high_risk precision is 3%, recall is 70%
- May be overfitting; high accuracy but lowish recall

<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/ensembleRandomForestCM.png"/>
</p>
<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/combinationSMOTEENCR.png"/>
</p>

#### Easy Ensemble AdaBoost

- From sklearn.metrics, the balanced_accuracy_score = 93.2%.
- high_risk precision is 3%, recall is 87%

<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/ensembleAdaBoostCM.png"/>
</p>
<p align="left">
  <img src="https://github.com/coleherman370/credit_risk_analysis/blob/main/Resources/ensembleAdaBoostCR.png"/>
</p>

## Summary

When using unbalanced data sets, understanding the fundemental task in which we want the model to be used for is a key factor in measuring its performance. Since we are trying to find a model that most accurately flags high_risk customers, we want to make sure we capture as many of those accounts as possible. Of all six machine learning models, the easy ensemble adaboost model performed the best with the highest balanced accuracy score, lowest number of false negatives in the confusion matrix, and the highest high_risk recall and precision scores. While the random forest model performed fairly well, there is some evidence of overfitting with lower recall scores when validating the model.

