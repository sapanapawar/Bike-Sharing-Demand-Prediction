# Bike-Sharing-Demand-Prediction

Predicting the bike count required at each hour for the stable supply of rental bikes.

**Problem Statement:**

Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

**Aim of project:**

The goal of the company Seoul Bike is providing the city with a stable supply of rental bikes. It becomes a major concern to keep users satisfied. The crucial part is the prediction of bike count rents at each hour for a stable supply of rental bikes. We can suppose that this study could be reported to the company 'Seoul Bikes'. We think it could help them knowing if yes or not they have to supply bike stations in the city, in order to keep the customers.

**Attribute Information:**

●	Date : The day of the day, during 365 days, type : str

●	Rented Bike Count : Number of rented bikes per hour which is the target, type : int

●	Hour: The hour of the day, type : int

●	Temperature(°C): Temperature per hour, type : Float

●	Humidity(%): Humidity in the air in %, type : int

●	Wind speed (m/s) : Speed of the wind in m/s, type : Float

●	Visibility (10m): Visibility in m, type : int

●	Dew point temperature(°C): Temperature at the beginning of the day, type : Float

●	Solar Radiation (MJ/m2): Sun contribution, type : Float

●	Rainfall(mm): Amount of rain in mm, type : Float

●	Snowfall (cm): Amount of snow in cm, type : Float

●	Seasons: Season of the year, type : str

●	Holiday: If it is holiday period, type: str

●	Functioning Day: If it is a Functioning Day, type : str


**Model Implementation and Evaluation:**

Model Name                           | R2 Score | MAE       | MSE        | RMSE     | 
----------                           |----------|-----------|------------|----------|
Logistic Regression                  | 0.56     | 308.72    | 159536.57  | 399.42   | 
Lasso Regression                     | 0.56     | 308.71    | 159539.52  | 399.42   | 
Ridge Regression                     | 0.56     | 308.72    | 159535.60  | 399.41   | 
Elastic Net Regression               | 0.53     | 315.45    | 171410.07  | 414.01   | 
Decision Tree Regression             | 0.67     | 247.30    | 118143.64  | 343.72   |
XGBoost Regressor                    | 0.83     | 165.26    | 60720.72   | 246.41   |
Random Forest Regressor              | 0.86     | 139.89    | 50467.60   | 224.64   |


**Conclusion:**

**Hperparameter Tuning:**

After Hyperparameter tuning on Random Forest model using Random Search CV we can see the slight change in the accuracy i. e.

MAE is increased from 139.89 to 142.25

MSE is reduced from 50467.60 to 50153.49

RMSE is reduced from 224.64 to 223.94

R2-Score is increased from 0.8617 to 0.8626

This results can said to be good for this dataset.

**Feature Importance:**


![image](https://user-images.githubusercontent.com/89305804/202852112-25d4c18e-ad43-467c-ba1f-39ac69e38a21.png)



Based on this analysis, we choose to built a Random Forest model to predict the number of bike rents. We achieved an R2 accuracy of 86.26% based on 3-folds CV. Finally, it was found that hour and temperature are the most determining feature predictors.
