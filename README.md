# Problem Statement
Given the data for a hospital which contains information about the age, gender, blood group, the blood component requested, date and time when the component was requested, Quantity of blood requested. We have to predict total demand for a particular blood group x component, say the demand for B+ve Plasma, in the next 3 weeks. The time 3 weeks is important as the blood older than 3 weeks was less likely to deliver oxygen. 

# EDA  
We did EDA to find out the relation of the blood quantity requested with the age, gender, week of the day. Some of the insights we found out were:-
Males require more blood than females
Children and teenagers require significantly higher levels of blood than adults
There are small variations in average quantity of blood demanded with the day of the week, like on Sundays the average quantity of blood required is about half the blood quantity required on mondays.

# Feature Engineering:-   
We introduced some new features to the data, which include, 
 Average QTY for the last 7 days
 Average QTY for the last 30 days
 Ratio of above two (7d/30d)
P_qty_fem_l1d Number of female patients on the last day.
Number of patients of age >= 50
Number of patients of age <= 10
Label = Quantity of blood required in the next 1 day, a week and a month.

# Approaches:- 

Prediction for each blood component scaled by the % prevalence of corresponding blood group
Prediction for each unique blood component & blood group combination


# Model :-
We used Xgboost Regressor for making predictions because there may be gaps in the time series while making predictions for some combinations.

# Results:-   
R-squared comes close to about 0.66 for one of the most common blood (group x component) combination

