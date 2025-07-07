![](UTA-DataScience-Logo.png)

# Spotify Song Popularity Prediction

This repository outlines my attempt to use track features to predict track popularity using "Spotify Tracks Dataset" from Kaggle, found [here](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset/data)

## Overview

The task, as defined by the Kaggle challenge is to use a dataset with Spotify track information containing 21 features, to predict the popularity of each track. The approach in this repository follows a polynomial regression model and a few iterations of this model with feature adjustments. This model achieved a mean-squared error (MSE) score of 341 after 5 attempts, which is higher than the best performance on Kaggle of 227 using XGBoost models.

## Summary of Workdone

### Data

* Data:
  * Type: CSV file of tabular data consisting of numerical and categorical features
  * Size: 114,000 unique entires
  * Instances (Train, Test, Validation Split): 91,200 tracks for training, 22,800 tracks for testing, none for validation

#### Preprocessing / Clean up

* Missing values and redundant features were removed, categorical features were one-hot encoded, and data was standardized for normalization purposes. 

#### Data Visualization

![](feature_histograms.png)

### Problem Formulation

* Define:
  * Input: Features in dataset
  * Output Track popularity prediction
  * Models
    * Linear regression: To establish a baseline set of evaluation metrics
    * Polynomial regression: To build on baseline metrics using a more complex model, with the goal of finding more complex relationships between features
    * Decision Tree: Attempted to compare against baseline and determine which model to move forward with
  * I attempted to adjust the degree hyperparameter, but was unsucessful in running the model

### Training

* Describe the training:
  * Software: I trained the model using Python within a Jupyter Notebook environment. Libraries used include:
    * pandas and numpy to manipulate data
    * sci-kit learn to build models
    * matplotlib to create visualizations
  * Hardware: All training and testing was done on a personal device (Macbook Air)
  * Difficulties include working with a dataset with many unique identifiers and determining which were useful, alongside hardware issues and inability to run models on my device

### Performance Comparison

* Clearly define the key performance metric(s).
* Show/compare results in one table.
* Show one (or few) visualization(s) of results, for example ROC curves.

### Conclusions

* State any conclusions you can infer from your work. Example: LSTM work better than GRU.

### Future Work

* What would be the next thing that you would try.
* What are some other studies that can be done starting from here.

## How to reproduce results

* In this section, provide instructions at least one of the following:
   * Reproduce your results fully, including training.
   * Apply this package to other data. For example, how to use the model you trained.
   * Use this package to perform their own study.
* Also describe what resources to use for this package, if appropirate. For example, point them to Collab and TPUs.

### Overview of files in repository

* Describe the directory structure, if any.
* List all relavent files and describe their role in the package.
* An example:
  * utils.py: various functions that are used in cleaning and visualizing data.
  * preprocess.ipynb: Takes input data in CSV and writes out data frame after cleanup.
  * visualization.ipynb: Creates various visualizations of the data.
  * models.py: Contains functions that build the various models.
  * training-model-1.ipynb: Trains the first model and saves model during training.
  * training-model-2.ipynb: Trains the second model and saves model during training.
  * training-model-3.ipynb: Trains the third model and saves model during training.
  * performance.ipynb: loads multiple trained models and compares results.
  * inference.ipynb: loads a trained model and applies it to test data to create kaggle submission.

* Note that all of these notebooks should contain enough text for someone to understand what is happening.

### Software Setup
* List all of the required packages.
* If not standard, provide or point to instruction for installing the packages.
* Describe how to install your package.

### Data

* Point to where they can download the data.
* Lead them through preprocessing steps, if necessary.

### Training

* Describe how to train the model

#### Performance Evaluation

* Describe how to run the performance evaluation.


## Citations

* Provide any references.







