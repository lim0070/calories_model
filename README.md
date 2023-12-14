
# Predict_Calories-Model
Made by Brighton Chan and Lincoln Ma


## Problem Identification
When we were given a random meal,we do not know how much calories that we were
comsuming. In our data frame, we were given (cols) which can used to predict
the calories for receipes in our data set so we can tell how much calories are
we comsuming if the food item dont have the calories label.

It could be useful for the majority of the people who cares about health since
food items in resteraunts were not forced to include a calories messurement and 
people may consuming too much calories so that it may lead to some health 
issues like diabetes. Some medical company could use this data to create a 
calories checking app so it can reduce unintention calories comsumption.

---

For the accuracy of the model, we will use root mean squre(RMSE) and also R^2 to test the performance of our model. RMSE is a good messure of accuracy on models and R^2 would tell us how many variation of the calories did our data explained.

RMSE could helps our model to avoid extreme errors in the data frame, we also set a boundary on certains variables like n_minutes and n_steps because some of the data in our dataset is large outlier like a cooking receipe require 10 year s would be removed

We aim to have a lower RMSE in our model so that it will reflects good performance on our model and also the trustworthy and individauls could apply our model on food items to get nutrition informations as they desires

Since we aim for an accurate model, a high R^2 means that our model predict large variability of the model so that we can confirm that we have the correct sets of features to predict the calories

# Baseline Model
For the baseline model, we used the linear regression model from sklearn and we used the columns "n_ingredients" and "minutes" to predict the "calories" of the food. The reason why we used linear regression is because it is relatively basic so we think it would set the basline for our final model which should have a better result. We chose to use "n_ingredients" and "minutes" as the columns to predict "calories" because we think the number of ingredients used has a correlation with the calories of the food as the more ingredients there are, the more calories the food has. For minutes, we also think it has a similar correlation as the longer it takes to make the dish, there should be more ingredients and steps to take which means there should be more calories.


## Preprocessing the Data
Both of the columns that we are using are quantitative variables, so we don't have to conduct preprocessing that transforms categorical variables. However, we realized that the data in the minutes and n_ingredients columns have a huge variance. Therefore, we used StandardScaler to standardize both of the columns, which would lower the variance between the datapoints.


## Model Performance
After fitting and predicting the data, the R^2 value that we got is 0.01948289259781144, which is pretty low. This suggests that "n_ingredients" and "minutes" aren't really the main contributing factors to predict calories. There is also a possiblity that a linear regression model isn't the best model to predict calories using n_ingredients and minutes. Moreover, we obtained the RMSE for the model which is 23.11474264203012. This suggests that there is some deviation between the predicted values and the actual values. We believe that we could do better to train a model that predicts data with a lower RMSE.




We also obtained a residual plot from the which illustrates the RMSE of the model. As you can see, the deviation is heavily skewed towards the positive side. This implies that the baseline model can be further improved.
*residual plot*

