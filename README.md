Challenge 17 -- Supervised Machine Learning - Credit Risk Predictions

## Credit Risk Overview
Using a credit card credit dataset we implement an analysis of a sample of credit behavior to better understand and predict credit risk.  To do this we are wanting to reduce any bias.  To do this we will implement the use of imbalanced learn and scikit-learn to evaluate the database to understand credit risk.

## Here's what we found

The following are the findings from our research.  The Balanced Accuracy scores are included in the section headings.

The first analysis was the use of use of naive oversampling - BAS = .6413

https://github.com/JohnJohnson913/Credit_Risk_Analysis/blob/8e4bad3b508f7e11ca95d26b04a82cf82c2cc10f/Naive_Oversampling.png

The next would be the SMOTE oversampling = BAS = .6376

https://github.com/JohnJohnson913/Credit_Risk_Analysis/blob/8e4bad3b508f7e11ca95d26b04a82cf82c2cc10f/SMOTE_Oversampling.png

That moves us to the Cluster Centroid Undersampling - BAS = .6413

https://github.com/JohnJohnson913/Credit_Risk_Analysis/blob/8e4bad3b508f7e11ca95d26b04a82cf82c2cc10f/Cluster_Undersampling.png

Next is the SMOTEENN Combination Sampling = BAS = .5294

https://github.com/JohnJohnson913/Credit_Risk_Analysis/blob/8e4bad3b508f7e11ca95d26b04a82cf82c2cc10f/Combination_Sampling.png

Next is the Balanced Rnadom Forest Classifier - BAS = .7877

https://github.com/JohnJohnson913/Credit_Risk_Analysis/blob/8e4bad3b508f7e11ca95d26b04a82cf82c2cc10f/Balanced_Random_Forest.png

Finally we used the Easy Ensable Adaboost Classifier = BAS =  .9254

https://github.com/JohnJohnson913/Credit_Risk_Analysis/blob/8e4bad3b508f7e11ca95d26b04a82cf82c2cc10f/Ensable_AdaBoost_Classifier.png

## In Summary

Though it's important situations like this to have a precise model, but even more important to be able to know you are able to catch all high risk individuals that are interested in opening accounts.  Due to that, it's likely better to look at the sensitivity or recall of the data, ensureing as many relevant instances are retrieved.

However, speaking of precision it remained low in each model when evaluating high risk invdividuals.  This especially was relevant when reviewing the high risk individuals as they are often the focus of the inscreased scrutiny.  However, the low risk individuals remained very high in regards to sensitivity. It may be a better approach to run the model, remove all the individuals identified as low risk and anyone not meeting this criteria could move to an underwriter for further rewview.

In terms of the test models to use going forward, I would be mostly likely to recommend the Easy Ensambler AdaBoost Classifier as it has the best balanced accuracy score, and also has the higher sensitivity score.
