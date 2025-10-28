## Classification of Waze Data for User Churn Prediction

## Project Overview 
Waze is a free, community-based navigation app that uses crowdsourced data from users to provide real-time traffic information and optimized routes directions. The goal of this project was to create a model to predict Waze's monthly user churn and accurately identify who, when, and why users churn. The models tested included a binomial linear regression model, XGBoost, and random forest model, at which the XGBoost model performed the best with an 81% accuracy, 16% recall, and 43% precision. Despite its higher performance, the XGBoost model's low recall score implies it is not a strong model. Thus, it is recommended more features of user data be collected to iterate this project to identify and build a stronger user churn predictive model.

## Business Problem
Waze aims to increase user base growth by reducing monthly churn — the rate at which users uninstall or stop using the app. High retention rates are key indicators of user satisfaction and long-term engagement, making churn prevention an essential part of Waze’s broader business strategy. This project focuses on developing a predictive machine learning model to identify users at risk of churning and uncover the behavioral and usage patterns that contribute to their disengagement. By understanding these drivers, Waze can take proactive measures to retain users through personalized recommendations, feature improvements, and targeted outreach.

Key business questions guiding this analysis include:

- Which users are most likely to churn each month?

- What specific behaviors or app usage patterns predict churn?

- How can Waze strategically intervene to improve user retention?


## Data Description
This project utilized a synthetic data set provided by Waze that included 15,000 uniqe navigations and 14 features. Features included in the data set include information such as:
- user's total navigations
- total duration driving time during the month
- total distance driven during the month
- days since onboarding onto the app, device type
- wether a user churned or not
  
Engineered features include: 
- distance driven per day
- total sessions per day
- distance driven per hour
- distance per navigation
- categorization of "professional drivers"

The pie chart below shows the breakdown of churned (17.7%) and retained (82.3%) users in the data set.


[INSERT PIC]


## Modeling and Evaluation
1. Hypothesis Testing to identify statistical significance of user characteristics and device type
3. Binomial Linear Regression Model
4. Random Forest Model
5. XGBoost Model

Hypothesis testing explored potential differences in user behavior between iPhone and Android drivers; however, no statistically significant relationships were found between device type and any other variables. Of the preditive models above, the XGBoost model was the highest performing with an 81% accuracy, 16% recall, and 43% precision. The top three most important factors in determining user churn included kilometers driven per hour, number of days after onbaording, and total navigations to a user's favorite destination, all of which were engineered features. 

[INSERT PIC]

## Business Recommendations:
Recommendations derived from the XGBoost Model include: 
- Incentivize Driving Frequency: Users with less kilometers driven per hour appear most likely to churn. Thus, Waze could promote challenges such as “drive streaks,” to encourage users to log frequent drives
- Personalize New User Engagement: The number of days after a user onbards to the app is the second strongest predictors of churn. Targeted engagement campaigns for new users during the onboarding period such as app tutorials or milestone rewards can be implemented to build early habits and prevent early drop-off
- Create Route Dependency: Waze can leverage the predictive power of total navigations to favorite locations by increasing user dependence for routine trips by sending push notifications that suggest a favorite destination when the user is detected in a new or atypical location
  
## Next Steps
Despite the XGBoost model's higher performance to other predictive models, its low recall score implies that it is not a strong predictor of user churn. Thus, it is recommended that more user feature data be collected to improve predicitve power and integrity of the model. Addiitional data could include: 
- User location attributes (e.g., urban vs. non-urban)
- Deeper metrics on user app interactions and feature usage


