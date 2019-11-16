# Model Comparisons for Predicting Titanic Survivors
Final Project for the Spring 2019 Statistical Methods and Applications course. All code written in R.

This project compares the performance of different models for predicting survival rates of Titanic passengers. Models selected include:

* Logistic Regression
* Random Forests
* Generalized Additive Models (GAMs)
* Naive Bayes
* Linear Support Vector Machines
* K-Nearest Neighbor
* Neural Net

For each of these models, I tested on the full dataset and a subset of features, selected by finding maximum AIC score on the regression model.
Both the full and reduced models were measured on their accuracy, precision and recall to determine which model performed the best at the 
classification task. According to a final F-score, the Reduced Naive Bayes model performed the best (f_score=0.9467) and the full GAM
model performed second best (f_score=0.9367).

Data Cleaning Tasks included:
* I had to replace missing data with most likely estimates and used predictive imputation. This was mostly with fares using the passenger's class.
* There was a large amount of missing data in the Age feature (263 nan values), so I utilized predictive imputation with the mice package to fill those values.

Feature Engineering included:
* Re-classifying Titles from many types into 4 distinct types (Mr, Mrs, Miss, Rare_Title).
* Adding a count for amount of family on the boat and a categorical variable for singleton, small family, or large family.
* A boolean of whether someone was a mother.
