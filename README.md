# Blood-Demand-Forecasting
This repo contains my work on Blood Demand Prediction under the company That Wise Advice.
# Objective 
• To build a model to predict demand of various blood components across blood groups over a period of 3 weeks
# Approach 
• Used pandasql with XGBRegressor for Time Series Forecasting and introduced Feature Engineering  
• Tried the following two ways to estimate the demand of each blood component x blood group  
Option 1: Prediction for each blood component scaled by the % prevalence of corresponding blood group  
Option 2: Prediction for each unique blood component & blood group combination  
# Results   
• Option 2 gives better predictions than option 1 for most of the combinations  
• R-squared comes close to about 0.66 for one of the most common blood (group x component) combination
