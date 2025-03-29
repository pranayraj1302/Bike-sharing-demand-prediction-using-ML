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


# Output Images

![Bike Sharing - 5](https://github.com/user-attachments/assets/bf98d480-adde-43e8-b4cf-42183add3c07)
![Bike Sharing - 4](https://github.com/user-attachments/assets/d887b65a-06b0-4947-8863-305e4fc1a8ec)
![Bike Sharing - 3](https://github.com/user-attachments/assets/bb3ef4fc-c0ea-49a8-8720-234145a0316e)
![Bike Sharing - 1](https://github.com/user-attachments/assets/9dc3d4e4-72a6-4354-bf70-aa739fcc640a)
![Bike Sharing   Corelation](https://github.com/user-attachments/assets/29394e4d-9c65-4f05-bb98-c74dd10823f9)
![Bike Sharing -2](https://github.com/user-attachments/assets/90dede05-2168-443c-88e5-c9b31a08b6e9)
![Bike Sharing - 8](https://github.com/user-attachments/assets/0c4c7ac7-0003-4c8d-8ee3-4adb543d08b2)
![Bike Sharing - 7](https://github.com/user-attachments/assets/06f1d079-6f91-4634-89eb-50297479711a)
![Bike Sharing - 6](https://github.com/user-attachments/assets/45b68268-aeee-424d-9ca4-133e1d8e30ac)

