I fit glmnet models using all the variables except week\_start\_date, which is the unique identifier. They include the engineered feature year.season and also the new data about number of hotel guests.

I fit glmnet models with the missing values imputed two different ways: by median value, and by k nearest neighbor. Imputation by k nearest neighbor gave the better result, which makes sense to me because of the strong seasonal component to the data.

I resampled with 25 bootstrapped repetitions and nine different combinations of the parameters alpha and lambda. The best model had the values alpha = 0.1 and lambda = 0.5350029.

This model, with knn imputation, yields a Mean Absolute Error (MAE) of 9.74.

In order to meet the required model performance level established in the FPS, a future model must reduce the MAE by 5.74.