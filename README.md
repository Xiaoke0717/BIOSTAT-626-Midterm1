# BIOSTAT-626-Midterm1

## Using Software: 

Anaconda - Jupyter Notebook 6.4.11 (Python3)

## Introduction

The ipnyb file contains mainly two parts. The first part is binary classification problem, which built a binary classifier to classify the activity of each time window into static (0) and dynamic (1). The second part is multi-class classification problem, which built a refined multi-class classifier to classify walking (1), walking_upstairs (2), walking_downstairs (3), sitting (4), standing (5), lying (6), and static postural transition (7).

## Binary Classification Part

In this section, there are 6 main steps, which have been marked in great detail, just follow the code of each module and run it.

The first step is to load the data and mark the target variables of the data to construct 0-1 binary target variables. When running, note that the test data path is modified to the local storage path.

The second step is to observe the basic condition of the data, which mainly contains the target variable distribution and the kernel density curve of each feature. Because the data itself is processed, the distributions are basically normal and are not treated here.

The third step is to divide the data, standardize them and reduce the dimensionality of PCA. I chose a training set to test set ratio of 6:4, which can be modified by test_size. the PCA was reduced to 185 dimensions because the cumulative explained variance is 99% at this point (you can also modify it yourself).

The fourth step is model selection, which mainly contains six models: K- Neighbors classification, Decision Tree Classification, Gaussian Naive Bases Classification, and Support Vector Each model is predicted using all the data and the PCA dimensionality reduction data, and the prediction report is obtained.

The fifth step is to load the test set data and perform the PCA process.

The sixth step is to bring in the test set data based on the previously selected models to get the final model results and export them to a local Excel file.

## Multi-class Classification Part

The Multi-class Classification section is basically the same as Binary Classification. Only two steps are added at the end, one is parameter selection, and parameter tuning is performed using grid search. Finally, a data correction section is also added, which is mainly based on the data observation of the step2, and some distribution characteristics of the target variables are derived to correct the model prediction for possible bad results.
