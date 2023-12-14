
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


