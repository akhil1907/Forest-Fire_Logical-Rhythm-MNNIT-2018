## Predict The Burned Area Of Forest Fires


### Introduction to the problem

Our task is to use the twelve inputs (in the original data set) to predict the burned area of forest fires. The output "area" was first transformed with a ln(x+1) function. Then, several Data Mining methods were applied. After fitting the models, the outputs were post-processed with the inverse of the ln(x+1) transform. Four different input setups were used. The experiments were conducted using a 10-fold (cross-validation) x 30 runs. Two regression metrics were measured: MAD and RMSE. A Gaussian support vector machine (SVM) fed with only 4 direct weather conditions (temp, RH, wind and rain) obtained the best MAD value: . The best RMSE was attained by the naive mean predictor. An analysis to the regression error curve (REC) shows that the SVM model predicts more examples within a lower admitted error. In effect, the SVM model predicts better small fires, which are the majority.
The data set contains 699 instances and 12 inputs. They are:

    1. X - x-axis spatial coordinate within the Montesinho park map: 1 to 9
    2. Y - y-axis spatial coordinate within the Montesinho park map: 2 to 9
    3. month - month of the year: "jan" to "dec"
    4. day - day of the week: "mon" to "sun"
    5. FFMC - FFMC index from the FWI system: 18.7 to 96.20
    6. DMC - DMC index from the FWI system: 1.1 to 291.3
    7. DC - DC index from the FWI system: 7.9 to 860.6
    8. ISI - ISI index from the FWI system: 0.0 to 56.10
    9. temp - temperature in Celsius degrees: 2.2 to 33.30
    10. RH - relative humidity in %: 15.0 to 100
    11. wind - wind speed in km/h: 0.40 to 9.40
    12. rain - outside rain in mm/m2 : 0.0 to 6.4
    13. area - the burned area of the forest (in ha): 0.00 to 1090.84

.
