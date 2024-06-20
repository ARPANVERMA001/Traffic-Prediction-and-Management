# Traffic Flow Prediction & Management

## Project Overview

This project aims to predict traffic flow at road intersections using various AI/ML models and to devise an efficient traffic management plan by adjusting the timers of traffic signals. 

### Presented By
- Arpan Verma
- Aditya Upadhyay

### Date
14th May 2024

### Course
Statistical Machine Learning (SML) CSE-342

## Table of Contents
1. [Background of the Study](#background-of-the-study)
2. [Problem Statement](#problem-statement)
3. [Introduction](#introduction)
4. [Dataset](#dataset)
5. [Feature Engineering](#feature-engineering)
6. [Algorithms/Methodology](#algorithms-methodology)
    - [Linear Regression](#linear-regression)
    - [Random Forest](#random-forest)
    - [Gradient Boosting](#gradient-boosting)
    - [XGBoost](#xgboost)
    - [LSTM](#lstm)
7. [Findings](#findings)
8. [Testing](#testing)
9. [Analysis](#analysis)
10. [Traffic Management](#traffic-management)
11. [Conclusion](#conclusion)
12. [Next Steps](#next-steps)
13. [References](#references)

## Background of the Study
Traffic congestion is a significant issue in urban areas, leading to wasted time, increased pollution, and economic losses.

## Problem Statement
- Predict traffic at intersections.
- Devise a traffic management plan by adjusting traffic signal timers.

## Introduction
In this project, we have utilized and compared various AI/ML models to predict traffic at road intersections and devised an efficient plan to manage signal timers.

## Dataset
The dataset used for this project is sourced from Kaggle, containing 48,120 observations of the number of vehicles each hour in four different lanes:
- DateTime
- Junction/Lane
- Vehicles
- ID

[Link to Dataset](https://www.kaggle.com/datasets/fedesoriano/traffic-prediction-dataset)

### Preprocessing
- The initial dataset is split into two separate datasets.
- Normalization is performed by subtracting the mean and dividing by the square root of variance.
- Data is plotted to determine its distribution and relevance.

## Feature Engineering
Relevant features are extracted and new features are created:
1. **DateTime features**: Hour, DayOfWeek, Month, Year, Date
2. **Interaction Feature**: HourDayOfWeek
3. **Junction Feature**: Overall Traffic
4. **Temporal Feature**: Trend

## Algorithms/Methodology

### Linear Regression
Implemented from scratch to model the relationship between independent variables and the target variable.

### Random Forest
An ensemble learning method used for regression tasks, achieving an MSE of 0.2403.

### Gradient Boosting
Builds models sequentially to correct errors made by previous models. Utilized decision trees as base learners.

### XGBoost
An optimized implementation of gradient boosting, improving performance with regularization techniques and parallel processing.

### LSTM
A type of recurrent neural network designed to capture long-term dependencies in sequential data. Implemented for time series prediction involving vehicle traffic data.

## Findings
- Models were evaluated and compared based on their performance.
- LSTM and Random Forest models provided the best predictions without overfitting the data.

## Testing
- Models were tested on each junction.
- Evaluation metrics such as MSE were used to measure performance.

## Analysis
- Models were tested on hidden datasets to assess their real-life prediction capabilities.
- Inference showed that LSTM and Random Forest models performed well without overfitting.

## Traffic Management
An algorithm was devised to calculate the green time for signals at each lane, optimizing traffic flow based on various assumptions and real-life constraints.

## Conclusion
The models, especially LSTM and Random Forest, provided reliable predictions and can be utilized for real-life traffic management by adjusting traffic signal timers.

## Next Steps
Future work includes extending the traffic prediction model to real-life scenarios and implementing the approach on a directed weighted graph to optimize traffic signal timing.

## References
- [Kaggle Dataset](https://www.kaggle.com/code/puneetgupta24/traffic-prediction)
- [Linear Regression Implementation](https://www.geeksforgeeks.org/linear-regression-implementation-fromscratch-using-python)
- [Traffic Signal Timing](https://ops.fhwa.dot.gov/publications/signal\ timing/03.htm#:∼:text=Phase%20Time%20%3D%203.8%20%2B%202.1%)

For more detailed information, please refer to the full project report.

---

This README provides a summary of the project, detailing the background, methodologies, findings, and future directions. For implementation details and code, please refer to the respective sections in the repository.
