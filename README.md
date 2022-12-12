# CS 6120 Semester Project

This repo represents the semester project work, Development and Evaluation of Models for Coding Injury Cause Description for CS 6120.

**Name:** Lillith Chute, Vitaliy Shkolnik, Adithya Abhishek Chenthilkannan

**Email:** chute.l@northeastern.edu, Shkolnik.v@northeastern.edu, chenthilkannan.a@northeastern.edu

**Preferred Name:** Lillith

**Updated:** December 11, 2022


### About/Overview

The worker’s compensation industry contains a lot of challenges. One such challenge is finding an effective way to classify various forms of unstructured data. 
One such form deals with injury description classification. This project is designed to see if a model can be produced to effectively categorize injury 
cause descriptions using real world worker’s compensation injury description claims. Frequently these descriptions are brief, and categories are non-standardized. 
As such, analyses were done around the length of text and its nature and examination of the categories. Based on this work, it was determined that there 
is a lot of overlap in categories. Further, that the descriptions were extremely short, frequently less than the size of a tweet. Given this, we chose to 
explore three different models. Naïve Bayes was chosen as a baseline. Second, that baseline was compared against Support Vector Machine and Random Forest/XGBoost. 
It was determined that XGBoost outperformed the others. However, there was not a statistically significant difference in the performance. Based on the findings, 
a major factor in the model’s ability to predict is that the data needs to be significantly improved. Ideally, the data ingestion process could be changed such 
that overlapping categories would be combined. Several categories that have little to no data could be removed. Furthermore, descriptions would be constructed 
so that based on categories, key words would be included.



### List of Features

This repository was initially constructed as a python project.  However, it was converted into a series of notebooks instead for ease of separation of tasks 
and to make it a bit more portable.  The python files primarily consist of preprocessing functions, pickle file production, and the baseline Naive Bayes model.  
For purposes of the features, this list will cover the notebooks.

The program can perform the following:
1. Using the given properly formatted cause of injury data file (injury category, injury description) as a CSV the various notebooks can be run.  The data should be stored in the Data directory one level down from the notebook.
2. The NaiveBayesBaseline.ipynb notebook will generate a series of models from worst performing to the best performing.
3. The TSNE.ipynb notebook will create a T-SNE clustering graph on the injury cause categories to determine separation.
4. The SVM.ipynb notebook will generate a series of models from worst performing to the best performing.
5. The Random_forest_exp.ipynb notebook will generate a series of models from worst performing to the best performing.
6. The XGboost_exp.ipynb notebook will generate a series of models from worst performing to the best performing.


### How to Run

1. Open your favorite .ipynb/python notebook evironment
2. Pull the data set InjuryCauseTopThirteen.csv and place it in a folder called Data.
3. Pull the notebook you wish to run and place it in the main directory.
4. Run the notebook.

Version 1 changes:
1. N/A


### Assumptions

N/A

### Limitations

1. The preprocessing hasn't had a chance to be as refined as we would like given the limitations of the data set.
2. The was a time constraint on this project.  Therfore, there is considerable room for greater data analysis on the data. Preliminary investigation suggests a lot of room for improvement in the data ingestion process generally speaking.  
3. The models were reasonably close in evaluation.  Further hyperparameter exploration could be explored.  Additionally, model chaining or building a specialized vocabulary of keywords for injury cause description could be useful in improving accuracy.


### Citations

N/A
