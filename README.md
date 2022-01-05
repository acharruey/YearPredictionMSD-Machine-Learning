# YearPredictionMSD-Machine-Learning
This is the final project of the course "Python for Data Analysis".

Our data set is the YearPredictionMSD Data Set from the UCI Machine Learning Repository.
Link : https://archive.ics.uci.edu/ml/datasets/YearPredictionMSD
This data set is composed of 515 345 songs released between 1922 and 2011. These songs are mostly western, commercial tracks. There are 91 variables, the first variable is the release year, ranging from 1922 to 2011. The 12 following variables are timbre averages, and the 78 last variables are timbre covariances. They take real values.

We wish to predict the release year of a given song, from 90 of its audio features (the 12 timbre averages and the 78 timbre covariances).
Therefore, the target variable is the release year, and the features are the 12 timbre averages and the 78 timbre covariances.

We tried the combination of 6 different models, and 4 different data sets (10 features and not downsampled, 20 features and not downsampled, 10 features and downsampled, 20 features and downsampled).
We found that the model with the best Root Mean Squared Error is the ExtraTreesRegressor, with the sets of 20 features, and the training set not downsampled. But to have a model small enough to load in a reasonnable time, and not to many features for the user to enter in the API, we decided to keep the best model with data sets of 10 features. It was the ExtraTreesRegressor, with the sets of 10 features, and the training set not downsampled. Unfortunately we got a memory error, so we kept the second best model with data sets of 10 features, which was the GradientBoostingRegressor, with the sets of 10 features, and the training set not downsampled. It has a RMSE of 9,38.


For further explanation, see the pdf of the PowerPoint that is in this repository.
