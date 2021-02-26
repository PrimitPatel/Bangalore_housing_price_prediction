# Banglore-housing-price-Prediction

## Overview
* Designed a tool that estimates house prices to help people when they looking for new house/Appartment.
 * Applied Different Data cleaning strategies to handle null values and outliers.
* Applied various machine learning models with Hyperparameter tuning techniques to get the best results with minimum errors.
* Built a client-facing API using flask.
## Resources Used
**Python Version:** 3.8.2

**Packages:**  pandas, numpy, sklearn, matplotlib, seaborn, xgboost, flask, json, pickle
  
**Datasets:** [https://www.kaggle.com/amitabhajoy/bengaluru-house-price-data/kernels](https://www.kaggle.com/amitabhajoy/bengaluru-house-price-data/kernels)

**Project Reference:** [https://www.youtube.com/playlist?list=PLeo1K3hjS3uu7clOTtwsp94PcHbzqpAdg](https://www.youtube.com/playlist?list=PLeo1K3hjS3uu7clOTtwsp94PcHbzqpAdg)

## Data Preprocessing
* Parsing total_sqft column:
  * Many rows contain a range instead of single values. this can be resolved by taking an average of range.  
  * some of rows have different measure unit like 'Sq. Meter', 'Sq. Yards', 'Perch' so convert them in 'sq. Foot' to make uniform 
* Removed Society feature as it has more than 40% missing values
* Parsed no_of_bedroom feature from Size column
* Handling Bathroom feature:
  * Filled null values with mode value as it's count was more than 50%
  * Removed rows which has 2 or more bathrooms than no of bedrooms in a home.
* Filled null values with a median in Balcony feature
* Put locations in a new group called 'other' which has less than 10 counts
* There was huge variation in price per sqft for the same location so removed outliers by using mean and std.
## Model Building
First, I transformed the categorical variables into dummy variables. I also split the data into train and test sets with a test size of 20%.

I tried different models:
* Multiple Linear Regressor 
* Gradient Boosting Regressor 
* XGBoost regressor 
* Random Forest Regressor
* Extra-trees regressor


   
