# HW2: Text Classification

## Overview

In this assignment you will experiment with classical ML models for categorizing social and news media posts as "fake" vs. "real". The models will be evaluated using Accuracy and F1 metrics, defined below. You may do additional tuning or feature engineering, based on only "train" split of the data. The highest performing model on the "test" split will receive +10pts extra credit.

## Experimental Setup

**Dataset:** Covid19 News dataset: [https://github.com/diptamath/covid_fake_news](https://github.com/diptamath/covid_fake_news).

Place data is all in one directory,  ./data , to make testing your code easier. Do not hardcode path to the data. Do not rename files.

**Metrics:**

- Accuracy: reported by SciKit Learn by default. [https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html).
- F1: [https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html).

## Problems/What to Do

### P1: Naive Bayes (15 pts)

Implement Multinomial NB with Lidstone smoothing (alpha=1, … , 1\|V|):
[https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html).

Hyperparameter to optimize: alpha

### P2: Random Forest and GDBT (20 pts)

- P2a: Random Forest: [https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html).
- P2b: Gradient Boosted Decision Tree: [https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html).

Hyperparameters to optimize: number of trees, learning rate, min_samples_leaf

### P3: SVM (15 pts)

SVM: [https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html).

Hyperparameters to optimize: Kernel: linear, polynomial, sigmoid; C (slack): 1, …

## What to submit:

One python file, containing 1 function for each model, with a single (shared) data loader function.

- For each model: Accuracy and F1 on test fold, range of hyperparameter values compared, final setting of hyperparameters
- Note: optimize hyperparameters on Validation fold only
