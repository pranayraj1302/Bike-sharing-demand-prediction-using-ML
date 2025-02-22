 # Overview:

This project aims to predict the demand for shared bikes using a dataset provided by a US bike-sharing provider, BoomBikes. The dataset contains daily rental bike counts along with various environmental and seasonal factors. The goal is to identify significant variables affecting bike demand and build a predictive model using multiple linear regression.

# **Table of Contents**
Problem Statement

Data Understanding and Exploration

Data Visualization

Data Preparation

Model Building and Evaluation

Results

Conclusion

Requirements

Usage

# **Problem Statement**

BoomBikes wants to understand the factors affecting the demand for shared bikes in the American market. The objectives are to:

Identify significant variables in predicting bike demand.
Evaluate how well these variables describe bike demand.
Data Understanding and Exploration
The dataset consists of 730 rows and 16 columns, with no missing values. 

# The key features include:

- season: Season of the year (spring, summer, fall, winter)
- yr: Year (0: 2018, 1: 2019)
- mnth: Month of the year
- holiday: Whether the day is a holiday
- weekday: Day of the week
- workingday: Whether the day is a working day
- temp: Normalized temperature in Celsius
- atemp: Normalized feeling temperature in Celsius
- hum: Normalized humidity
- windspeed: Normalized wind speed
- cnt: Count of total rental bikes (target variable)

# Data Visualization
Data visualization is performed using matplotlib and seaborn to understand the distribution of numeric variables and the relationships between categorical variables and the target variable. 

Key visualizations include:

- Distribution plots for numeric variables (temperature, humidity, wind speed, and bike count).
- Box plots for categorical variables against bike count.
- Pair plots to visualize relationships between numeric variables.
- Correlation heatmap to identify multicollinearity.

# Data Preparation

Data preparation involves:

- Converting categorical variables into string representations for better readability.
- Creating dummy variables for categorical features.
- Dropping unnecessary columns (instant, dteday) that do not contribute to the analysis.
- Splitting the dataset into training and testing sets (70% train, 30% test).
- Scaling numeric variables using MinMaxScaler.

# Model Building and Evaluation

The model is built using multiple linear regression. 

The steps include:

- Fitting a linear regression model with all features.
- Using Recursive Feature Elimination (RFE) to select significant features.
- Evaluating the model's performance using metrics such as R-squared and Adjusted R-squared.
- Checking for multicollinearity using Variance Inflation Factor (VIF).
- The final model is built using 6 significant features, achieving an Adjusted **R-squared value of approximately 79.1%.**
