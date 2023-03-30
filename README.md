# SC1015 DSAI Mini Project
## About
This is our mini project for NTU-SC1015 (Introduction to Data Science and Artificial Intelligence).

Our mini project uses a dataset that contains the personal stats and attributes of NBA players between the 1996 - 2021 seasons. The dataset can be obtained from above or click [here](https://www.kaggle.com/datasets/justinas/nba-players-data) to go to source directly.
Our code and analysis can be obtained from the notebook 'NBA_DataAnalysis_Final.ipynb' above.

## Problem Statement
To find out the relation between a player's personal stats and attributes and their team performance.
As a measure of team performance, our response variable will be the net_rating of the individual players.

## Analysis Walkthrough
__Bolded points are new things we have implemented__
1. Data Preparation & Cleaning
  - Remove rows that we feel is irrelevant to our analysis (E.g. name, college, season, etc.)
  - __Data Binning__
    - Split personal attributes into ranges to simplify the data and make it easier to understand and analyze
  - Removal of 'NaN' values, for our data we are interested in how drafting may affect net_rating hence we removed undrafted players
2. Exploratory Data Analysis
  - Visualisation of Repsonse Variables
    - Removal of outliers due to obvious skewness
  - Visualisation of Predictor Variables
  - Calculation of linear correlation using Pearson's correlation coefficient
  - __Calculation of non-linear correlation using Kendall's Rank coefficient__
3. Model Training Attempt
  - __Use of mutual information regression to measure the statistical dependence of predicotrs with response__
  - __Use of Seleck K best to select the features with the highest mutual information scores (k = 5 for our model)__
  - Split dataset into 80-20 train-test datasets
  - Use of decision tree regressor as our machine learning model
  - Calculation of MSE, MAS, and R^2 to measure accuracy of model
  
## Conclusion
From our exploratory analysis, we have discovered that personal stats and attributes have little to no linear correlation with team performance. Hence, we took a non-linear approach to the relationship but through our analysis, there seems to be little to no non-linear correlation as well.

For our attempt at model training to predict team performance of a player based on their personal stats and attributes, we used a decision tree regressor due to the complex correlation of the predictors and the continuous nature of our response variable. Unfortunately
  
## Contributors
- Randall Chiang Tian Cong U2222099A
- Gary
- Trisha

## References
Dataset: https://www.kaggle.com/datasets/justinas/nba-players-data