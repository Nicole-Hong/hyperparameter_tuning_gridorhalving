[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)

# Hyperparameter Tuning - GridSearch vs Halving GridSearch

Hyperparameter tuning helps improve the performance of machine learning models in predictive modeling, but for certain machine learning models, especially the suppurt vector machine (SVM), the processing time can be a buttleneck, and using the GridSearchCV for the classification algorithms, SVM can run for 2 hours to 48 hours, or even longer. 

HalvingGridSearchCV is an experimental optimizer by sklearn and alternative method to GridSearchCV, and it helps reduce the processing time significantly, almost by 80%, with the same accuracy and improvement in the performance that GridSearchCV provides.

The objective of this project is to experiment the efficiency of HalvingGridSearchCV in comparison to GridSearchCV, by measuring both, the model performance and processing time. Tests are conducted for both, classification and regression models, where for classification models, GridSearchCV and HalvingGridSearchCV are compared and for regression models, RandomizedSearchCV and HalvingRandomizedSearchCV are compared against each other.

#### Links:

__Comparison for Classification Models:__
* [sklearn: GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
* [sklearn: HalvingGridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.HalvingGridSearchCV.html)

__Comparison for Regression Models:__
* [sklearn: RandomizedSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.RandomizedSearchCV.html)
* [sklearn: HalvingRandomizedSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.HalvingRandomSearchCV.html)


## How to use this repository

This repository has the following main directories:

* __data:__ train/test datasets for classification and regression
* __figures:__ visualizations generated from EDA
* __src:__ code for hyperparameter tuning experiments

### Workflow Overview

Hyperparameter tuning using the standard GridSearch for classification and regressions are processed first. Then, Halving methods are applied to the same datasets with the same grid parameters. In both runs, in addition to measuring the processing time and performance effectiveness, the following is measured, compared and analyzed:

__For Regression Models:__
* MSE, MAE and RMSE

__For Classification Models:__
* Accuracy
* F1 Scores
* Confusion Metrics

### System Requirements

This project has been developed using Python, Jupyter Notebook and Google CoLab, which are run on a Windows system. 

### Data Requirements

Data for Classification and Regression is obtained from sklearn datasets.

### Key Outputs

Best model parameters are produced from each hyperparameter tuning process, along with the results of the performance metrics being used in each test. The performance of best parameters identified by each Grid Search and Halving Grid Search is then compared and analyzed.


