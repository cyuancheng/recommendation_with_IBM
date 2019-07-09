# Recommendations with IBM

### Chiyuan Cheng 07/09/2019

## Table of Contents

- [Project Overview](#overview)

- [Project Description](#run)
  - [Exploratory Data Analysis](#2.1)
  - [Rank Based Recommendations](#2.2)
  - [User Based Collaborative Filtering](#2.3)
  - [Content Based Recommendations](#2.4)
  - [Matrix Factorization](#2.5)
- [Conclusion](#conclusion)
- [Files](#files)
- [Software Requirements](#sw)
- [Acknowledgements](#credits)


<a id='overview'></a>

## 1. Overview

In this project I analyzed the interactions that users have with articles on the IBM Watson Studio platform, and made recommendations of articles they will like.

<a id='run'></a>

## 2. Description

Five steps for this project:

<a id='2.1'></a>

### 2.1. Exploratory Data Analysis

Before we dive into the details of recommendation system, we explore the data and ask questions about the data we are working with.

<a id=2.2'></a>

### 2.2. Rank Based Recommendations

Find the most popular articles based on the most interactions with users. Since there is no rating for any of the articles, it is easy to assume the articles with the most interactions are the most popular. 

<a id='2.3'></a>

### 2.3. User Based Collaborative Filtering

To provide better recommendations to the users, we could look at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. 

<a id='2.4></a>

### 2.4. Content Based Recommendations

We might be able to use NLP to to develop a content based recommendation system. ( This is not required to complete this project.)


<a id='2.5'></a>

### 2.5. Matrix Factorization

Finally, we can use machine learning approach to building recommendation system. we can build a matrix decomposition using the user-item interactions. Using this decomposition, we can get an idea of how well we can predict new articles an individual might interact with. 

<a id='files'></a>

## 3. Files

<pre>
.
├── app
│   ├── run.py------------------------# flask file to run app
│   ├── imag_webapp_1		# screenshot of web app
│   ├── imag_webapp_2 		# screenshot of web app
│   └── templates
│       ├── go.html-------------------# classification result page of web app
│       └── master.html---------------# main page of web app
├── data
│   ├── DisasterResponse.db-----------# database to save cleaned data
│   ├── categories.csv-------# raw data to process
│   ├── messages.csv---------# raw data to process
│   └── process_data.py---------------# perform ETL pipline
├── model
│   ├── train_classifier.py-----------# perform classification pipeline
│   └── classifier.pkl		-----------# classifier result
├── notebook
     ├── ETL Pipeline Preparation.ipynb----------# Jupyter notebook for ETL 
     └── ML Pipeline Preparation.ipynb-----------# Jupyter notebook for ML

</pre>

<a id='conclusion'></a>
## 4. Conclusion

The dataset used in this project is highly unbalanced, with very few positive examples for some message categories. This results in a low recall despite having high accuracy.

Therefore, more data is needed in order to improve the prediction accuracy and use this app for actual prediction

<a id='sw'></a>

## 5. Software Requirements

The code contained in this repository was written in Python 3, and requires the following Python packages: pandas, numpy, matplotlib, seaborn.

<a id='credits'></a>

## 6. Acknowledgements

This app was developed as part of the Udacity Data Scientist Nanodegree.