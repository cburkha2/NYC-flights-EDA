# Project Proposal

I will be using a dataset that contains information for every domestic flight departing from one of New York City’s three major airports during the year 2013. The data were provided by the Federal Aviation Administration (FAA) and organized into an R package by Hadley Wickham, leader of the Tidyverse (collection of R packages/libraries for data science) team. I am using this dataset because of my interest in aviation. I also like this dataset because it has a relatively small number of features but a large number of observations. My goal in this project is to find out which features have the greatest effect on arrival delay. 

 
This dataset has a relatively small number of features, so I plan to start by finding summary statistics and creating simple visualizations for each of the relevant features. Then, I plan to examine correlations to potentially create new features and determine which features to use as predictors. Feature engineering may also be necessary to convert some of the features to more appropriate data types. 
	Because the response (arrival delay) is numerical, my first model will be a simple linear regression model. For more advanced models, I would like to try random forests and XGBoost because both models have performed very well in high-profile Kaggle competitions. I do not intend to use an artificial neural network because I don’t believe it will be necessary to create an accurate model. 

 
I will be using R throughout the project. I am choosing R over Python because I am much more familiar with it, I think the syntax is more intuitive, and its capabilities for most data science tasks are comparable to those of Python. The most important library I will be using is “dplyr”, which will allow me to do any required preprocessing/feature engineering (similarly to Pandas for Python). I will be using “ggplot2” for all visualizations. I will use “caret” to fit the machine learning models, and I plan to use “corrr” for correlations and “yardstick” for evaluation. 

# Summary

The linear regression model had an R-squared of 0.84 (84% of variance in arrival delay can be explained by the model) and a mean absolute error of 13 (on average, the model's prediction for arrival delay was 13 minutes off the actual arrival delay). Both of these values were better than I anticipated, because I ended up using 21 predictor variables. As mentioned in the model notebook, I unfortunately did not plan my time very well, and so I was unable to try other models (I was curious about both random forest and XGBoost). 

The exploratory data analysis part revealed some interesting trends. On average, flights were least likely to arrive late in late September or early October. Flights in the early morning were more likely to arrive on-time or early, while flights departing between 5PM and 7PM had the greatest arrival delay. Longer distances between the origin and destination airports were correlated with lower arrival delays. Flights operated by Alaskan and Hawaiian airlines arrived earliest on average, while flights operated by AirTran and Frontier had an average arrival delay of over 20 minutes. On average, flights from Newark arrived 9 minutes late, while flights from JFK and LaGuardia arrived 5.5-5.75 minutes late. The best predictor of arrival delay, by far, was departure delay. 

The main thing I would change about this experience is to give myself more time. I would have loved to use multiple ML models and compare their performance. The exploratory data analysis I did was not very deep, and I suspect there are more meaningful insights to draw from more thorough analysis. In particular, the data package also includes hourly weather data for each airport, which would have been excellent to investigate. I chose not to for this project because the weather data has some missing observations which are as so straightforward to deal with. 
