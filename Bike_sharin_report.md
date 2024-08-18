# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Initially, I faced a problem connecting to Kaggle for submissions, so I had to install Kaggle to let me upload data directly. Later, when I tried to submit after incorporating new features, some submissions showed negative values. I addressed this by adjusting them to zero before submitting.

### What was the top ranked model that performed?
The highest-ranked model, named "New_feature model," achieved a Kaggle score of 0.51625. This improvement was the result of adding several features, including datetime, humidity, and temperature. Remarkably, this score was attained without any hyperparameter tuning.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The exploratory analysis helped in examining the distribution of the dataset and in determining the best additional features to use. I derived features such as day, hour, and year from the datetime data. Additionally, I transformed the temperature into a categorical feature that indicates temperature levels. Similarly, I converted the humidity data into a categorical feature to represent different humidity levels.

### How much better did your model preform after adding additional features and why do you think that is?
The model showed significant improvement, with its score improving from 1.80839 to 0.51625 after incorporating additional features. This substantial enhancement indicates that adding features can greatly improve the accuracy of our model.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
After tuning the hyperparameters, there was a modest improvement in the model's performance, with the score moving from 0.51625 to 0.46639. This indicates that while hyperparameter tuning did result in better performance, the improvement was relatively small.

### If you were given more time with this dataset, where do you think you would spend more time?
The exploratory data analysis (EDA) part of the dataset will require more time, as we need to carefully assess the importance of each feature. This thorough analysis will provide valuable insights that will inform further improvements to our models.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model| presets|time_limit|hyperparameters|score|
|--|--|--|--|--|
|initial|best_quality|600|default|1.80839|
|add_features|best_quality|600|default|0.51625|
|hpo|best_quality|800|GBM, NN_Torch, CAT|0.46639|
 
### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)


### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
