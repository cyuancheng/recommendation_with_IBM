# Recommendations with IBM

### Chiyuan Cheng 07/09/2019

## Table of Contents

- [Project Overview](#overview)

- [Project Description](#run)
  - [Exploratory Data Analysis](#2.1)
  - [Rank Based Recommendations](#2.2)
  - [User-user Based Collaborative Filtering](#2.3)
  - [Content Based Recommendations](#2.4)
  - [Matrix Factorization](#2.5)
- [Conclusion](#conclusion)
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

<a id='2.2'></a>
### 2.2. Rank Based Recommendations

Find the most popular articles based on the most interactions with users. Since there is no rating for any of the articles, it is easy to assume the articles with the most interactions are the most popular. 

<a id='2.3'></a>
### 2.3. User-user Based Collaborative Filtering

To provide better recommendations to the users, we could look at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. 

<a id='2.4'></a>
### 2.4. Content Based Recommendations

We might be able to use NLP to to develop a content based recommendation system. ( This is not required to complete this project.)


<a id='2.5'></a>
### 2.5. Matrix Factorization

Finally, we can use machine learning approach to building recommendation system. we can build a matrix decomposition using the user-item interactions. Using this decomposition, we can get an idea of how well we can predict new articles an individual might interact with. 


<a id='conclusion'></a>
## 3. Conclusion

To improve the model, we can use A/B test to verify the effect of training vs testing data. Firstly, we can randomly divided the users into two groups, where the articles that the users see are recommended by recommendation system. In the other group, the articles that the users see are randomly selected from all the articles. Then, we can evaluate how much experiment size should be collected. Finally, we can use these experimental data to make a hypothesis test. The null hypothesis is that the recommendations with any of the recommendation system do not raise the proportion of article which users interact with. We can then use a parametric test or non-parametric test to estimate p vale. If the p value is less than 0.05, it means the hypothesis is rejected and the recommendation systems are an improvement to how users currently find articles.

<a id='sw'></a>

## 5. Software Requirements

The code contained in this repository was written in Python 3, and requires the following Python packages: pandas, numpy, matplotlib, seaborn.

<a id='credits'></a>

## 6. Acknowledgements

This app was developed as part of the Udacity Data Scientist Nanodegree.