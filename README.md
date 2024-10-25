# BoomBikes Assignment


## Table of Contents
* [General Info](#general-information)
* [Approach](#approach)
* [Solution Found](#solution-found)
* [Key Insights](#key-insights)
* [Conclusion](#conclusion)
* [Technologies Used](#technologies-used)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
**Problem Statement**

BoomBikes, a US-based bike-sharing provider, has experienced significant revenue declines due to the COVID-19 pandemic. To recover and thrive post-lockdown, the company aims to understand the factors influencing the demand for shared bikes. This knowledge will help them prepare for increased demand and outperform competitors.


**Business Goal**

The objective is to model the demand for shared bikes using available independent variables. This model will help BoomBikes’ management understand how demand varies with different features, enabling them to adjust their business strategy to meet customer expectations and optimize revenue. Additionally, the model will provide insights into the demand dynamics of new markets.


**The company wants to know:**

1. Which variables are significant in predicting the demand for shared bikes.
2. How well those variables describe the bike demands>


**Data being used**
Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors.
Bike Sharing dataset [here](https://ml-course2-upgrad.s3.amazonaws.com/Linear+Regression+Assignment/Bike+Sharing+Assignment/day.csv) and Data dictionary [here](https://drive.google.com/file/d/1x4Vi_FF0DEmTN1Cf6BnPHUuQP9p0s0Pz/view?usp=sharing).


## Approach
The approach follows a structured path to address the problem of demand prediction:

- Data Collection and Understanding
  - The dataset consists of daily records of bike rentals, which includes features related to weather conditions, seasonality, holidays, working days, and the number of bikes rented per day.
  - The dataset is loaded, and a preliminary inspection is conducted to understand the types of variables available (e.g., categorical and continuous variables) and their distributions.

- Exploratory Data Analysis (EDA):
  - The EDA phase involves inspecting the relationships between bike demand (the dependent variable) and independent variables, such as temperature, humidity, and day types.
  - Visualization techniques like pair plots, histograms, and correlation heatmaps are used to examine patterns, trends, and outliers in the data.
  - This step identifies potential trends, such as higher demand on weekends, and the impact of favorable weather conditions.

- Data Preprocessing
  - Handling Missing Values: Missing values are treated appropriately if any exist.
  - Encoding Categorical Variables: Variables like seasons, months, or whether a day is a working day are encoded as dummy variables to make them suitable for the regression model.
  - Scaling Features: Numeric features are scaled to bring all variables onto a similar scale to ensure that the model coefficients are not biased by different feature ranges.


- Feature Selection
To avoid overfitting and reduce model complexity, only significant features are selected for the model. Methods such as correlation analysis and variance inflation factors (VIFs) are used to remove multicollinearity and ensure that independent variables provide distinct information.
Stepwise regression or backward elimination may be used to iteratively refine the list of significant predictors.

- Model Building:
  - A linear regression model is built using the selected features. The model attempts to establish a relationship between the dependent variable (bike demand) and the independent variables.
  - The model is trained on the dataset, and regression coefficients are calculated to understand the impact of each feature on bike demand.

- Model Evaluation:
  - The model is evaluated using performance metrics such as R-squared, adjusted R-squared, Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).
  - These metrics help assess how well the model fits the data and how accurately it predicts bike demand. A high R-squared value would indicate a good fit, while lower error terms would signify better predictive performance. it.


## Solution Found
After building the linear regression model and evaluating its performance, the following insights were uncovered:

- Significant Variables
  - This model captures the complex interplay between weather, seasons, and temporal factors affecting bike rides.
  - Positive influences like higher temperatures, the year variable (suggesting growth), and certain months like September increase ridership
  - While negative factors like windspeed, humidity, and adverse weather significantly decrease it.

- Model Performance
  - The model achieved a good R-squared value, indicating that a substantial proportion of the variance in bike demand was explained by the independent variables.
  - Error metrics like RMSE showed that the model was able to predict bike demand with a reasonable level of accuracy, making it useful for business forecasting.

## Key Insights
- Temperature and year-over-year growth are the strongest positive drivers of bike ridership.
- Adverse weather conditions like windspeed, humidity, and light snow have significant negative impacts on bike ridership.
- Seasonality and monthly trends show specific months (like September) driving more rides, while colder and holiday months (e.g., December and November) see declines.

![image](https://github.com/user-attachments/assets/de1a73b8-14d2-4dfc-886c-0a03e6fca6e1)

![image](https://github.com/user-attachments/assets/1c758c76-85c6-4248-934d-f797593ad61d)


## Conclusion:
The insights gained from this model can help BoomBikes optimize their operations by:

- Adjusting bike availability based on predicted demand during different seasons, weather conditions, and day types.
- Operational efficiency: The company can plan maintenance and fleet management activities during days with lower predicted demand, such as during unfavorable weather conditions.

The model will allow BoomBikes to proactively respond to changes in market conditions and customer behavior, positioning them to capture increased demand and enhance revenue in the post-pandemic era.


## Technologies Used
This project leverages the following technologies and libraries:

- NumPy: Provides support for multi-dimensional arrays and matrix operations, facilitating numerical computations.
  
- Pandas: Used for data manipulation and analysis, enabling data loading, cleaning, and structuring.

- Matplotlib: A plotting library used for creating static visualizations to understand data distributions and trends.

- Seaborn: Based on Matplotlib, Seaborn simplifies complex statistical plots and enhances visualizations.

- Plotly: An interactive graphing library used for dynamic and highly customizable visualizations.

- SciPy: Provides scientific and technical computing tools, including statistical methods for hypothesis testing.

- Scikit-Learn: Machine learning library used for feature selection, model building, and evaluation metrics.

- Statsmodels: Provides tools for statistical models and hypothesis testing, used here for linear regression and variance inflation factor (VIF) calculations to assess multicollinearity.

These technologies collectively enable data preparation, statistical analysis, predictive modeling, and insightful visualizations.

## Acknowledgements
- Live sessions by upGrad.
- Resposnes provided in Daily Doubt Resolution sessions conducted by upGrad.
- Cource content in upGrad Course 2 - Module 1 - Linear Regression.
- Learning Curves - Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 2nd Edition ISBN: 9781492032649 page 131



## Contact
Created by [@kk20krishna](https://github.com/kk20krishna)


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
