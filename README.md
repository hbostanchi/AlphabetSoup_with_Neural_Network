# AlphabetSoup_with_Neural_Network
## Overview
In this module, we explore and implement neural networks using the TensorFlow platform in Python. We discuss the background and history of computational neurons as well as current implementations of neural networks as they apply to deep learning. We discuss the major costs and benefits of different neural networks and compare these costs to traditional machine learning classification and regression models. Additionally, we practice implementing neural networks and deep neural networks across a number of different datasets, including image, natural language, and numerical datasets. Finally, we learn how to store and retrieve trained models for more robust uses.

## Objectives
-	Compare the differences between the traditional machine learning classification and regression models and the neural network models.
-	Describe the perceptron model and its components.
-	Implement neural network models using TensorFlow.
- Explain how different neural network structures change algorithm performance.
-	Preprocess and construct datasets for neural network models.
-	Compare the differences between neural network models and deep neural networks.
-	Implement deep neural network models using TensorFlow.
-	Save trained TensorFlow models for later use.




## Project Overview
In this challenge, you’ll have to build your own machine learning model that will be able to predict the success of a venture paid by Alphabet soup. Your trained model will be used to determine the future decisions of the company.

The goals of this challenge are for you to:

- Import, analyze, clean, and preprocess a “real-world” classification dataset.
- Select, design, and train a binary classification model of your choosing.
- Optimize model training and input data to achieve desired model performance.
- [Click here](https://github.com/hbostanchi/AlphabetSoup_with_Neural_Network/blob/master/challenge/AlphabetSoupChallenge.ipynb) to access challenge files.


## Challenge Overview
We received a CSV containing more than 34,000 organizations that have received various amounts of funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization such as the following:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry 
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Resources
Software: Visual Studio Code 1.39.0, Jupyter Notebook 6.0.3
Languages: Python 3.7
Libraries: scikit-learn 0.22.1, TensorFlow 2.0 r2.1
Data Sources:
[Charity data](https://raw.githubusercontent.com/hbostanchi/AlphabetSoup_with_Neural_Network/master/challenge/charity_data.csv)


## Challenge Summary
Using our knowledge of machine learning and neural network model building, we created a binary classifier that is capable of predicting whether or not an applicant will be successful if funded by Alphabet Soup using the features collected in the provided dataset.

#### How many neurons and layers did you select for your neural network model? Why?

Observing the data, I decided that the columns EIN and Name were neither features nor targets. 
Also came up with the target variable column "Is_Successful".
For my first model, I chose 8 neurons in the first hidden layer and 4 neurons in the second. This model only achieved about 58.6% accuracy after 100 epochs.

#### Were you able to achieve the target model performance? What steps did you take to try and increase model performance? 

To optimize, I tried the following to add one neurons  on hidden layer. This model with 8 neurons in the first layer, 5 neurons in the second layer and reached the accuracy 0f %75.5 after 100 epoches.

#### If you were to implement a different model to solve this classification problem, which would you choose? Why?

Random forest classifiers are what I choose to use for classification into a more robust and accurate model. 
Random forest models have been popular in machine learning algorithms for many years due to their robustness and scalability. 











