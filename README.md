# Stock-Price-Predictions

- [Overview](#overview)
- [The problem](#the-problem)
- [Technical Details](#technical-details)
- [Credits](#credits)

## Overview

We look at a time-series analysis problem here with respect to stocks. It leverages a curated dataset that was provided as part of an in-depth course in Udemy on
[machine learning in Finance](https://www.udemy.com/course/ml-and-python-in-finance-real-cases-and-practical-solutions/). The datasets not only contains the daily stock price but also the traded stock volumes.


## The problem

- To predict stock prices based on a daily stock price and traded stock volume time series.
- Here, we specifically look at a few popular stocks and also the popular 'SP500' index. The stocks analyzed here are that of Google, Apple, AT&T, Tesla, MGM, Amazon, IBM and Boeing.

## Technical Details

- The details are in the [notebook](https://github.com/jyotisman-ds/Stock-Price-Predictions/blob/main/Stock_Price_Predictions.ipynb).
- Preprocessing included sorting with respect to the date variable. The idea here is to analyze the stock price increase since its inception (or in our case the beginning of 2012). So, we normalize the stock prices with respect to the initial trading value.  
- Another excellent way of visualizing time series is using the interactive plotting options provided by plotly. This also provides tools to zoom into specific time periods to visualize interesting variations.
- On the training side, I created a custom window function to choose any length of time-window one wants wants to feed into the model. Depending on the amount of fluctuations in the time series, one could find the optimal window size that best suits the model.
- We first use a Lasso regression model and optimize alpha to find the best fit.
- Given that its a time series, we ultimately trained a sequence model with LSTMs along with experimenting several different layers with it.


_Tools : python, sklearn, TensorFlow, Keras, pandas, plotly_

## Credits

I am deeply thankful to Udemy and all the instructors for hosting this wonderful course for [machine learning in Finance](https://www.udemy.com/course/ml-and-python-in-finance-real-cases-and-practical-solutions/). My curiosity to learn Machine Learning/deep learning applications led me to this course and I am glad not only to have learnt some useful techniques but also a great deal about the world of finance in general.
