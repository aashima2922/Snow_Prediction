**ARIMA Model for Snow Prediction**

This repository contains code to predict snow occurrence using an ARIMA model on historical weather data. 
The steps involve data preparation, model fitting, forecasting, and snow prediction based on temperature thresholds.
The data is the public data available on bigquery.

**Description**
The code performs the following tasks:

*Data Preparation:*

Load and filter relevant features from the dataset.
Convert the date column to datetime format and set it as the index.
Drop columns with any null values.


*Forecast Date Calculation:*
Calculated the specific date 15 years ago from today to use for forecasting.


*Split Data into Training and Test Sets:*

Create a training dataset with data before the forecast date.
Create a test dataset with data for the forecast date.


*Fit ARIMA Model:*
Fit an ARIMA model to the 'mean_temp' column of the training data.


*Calculate the average temperature on days when it snowed.*
Set a threshold temperature slightly below this average for snow prediction.

*Forecast Future Values:*

Forecast the mean temperature for the day before and the day of the forecast date.
Print the forecasted values and their confidence intervals.

*Predict Snow:*

Predict snow occurrence based on the forecasted temperatures and the set threshold.
Print the snow predictions for the forecast dates.
