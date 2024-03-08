# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Oreoluwa Alade

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: When I submitted the first prediction, everything went smoothly as it was successful. However, when I submitted the second one, Kaggle rejected it because it contained negative values. To address this issue, I had to modify the predictions and set the negative values to zero.

### What was the top ranked model that performed?
TODO: For me, the model that peformed best was KNeighborsDist with a score of 1.86412 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: As suggested, I ensured that the 'datetime' column was parsed as datetime objects when reading the CSV files. Following the first training, I converted the datetime columns in both the train and test DataFrames to datetime format. Then, I extracted the hour, day, and month from these datetime columns and created new columns for them. Subsequently, I dropped the original datetime column from both the training and test datasets. 

There was an improvement because I did the things written above and this improved the model by 60%. 

### How much better did your model preform after adding additional features and why do you think that is?
TODO: I was unable to improve the performance of the model after trying different hyper parameters. Rather I obtained models slightly lower in performance (0.73217 and 0.67163 as Kaggle Score) to the previous model.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: For some reason, when I tried different hyper parameters, it wasn't working for me and that's why O settled for a preset of "medium_quality_faster_train".

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: On the Hyper parameter optimization

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model       |timelimit|presets              |eval_metric            |score  |
|------------|---|---------------------------|-----------------------|-------|
|initial     |600|medium_quality_faster_train|root_mean_squared_error|1.86412|
|add_features|600|medium_quality_faster_train|root_mean_squared_error|0.73217|
|hpo         |600|medium_quality_faster_train|root_mean_squared_error|0.67163|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: The greatest benefits are derived from feature engineering, coupled with thorough Exploratory Data Analysis (EDA). Moving forward, my primary objective is to enhance the model's performance by integrating variables such as working hours, which significantly influence bike demand, and capturing seasonal patterns, both in terms of peak demand and off-peak periods.
