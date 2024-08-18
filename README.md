# Bike-Sharing-Demand-with-AutoGluon

This project focuses on creating and analyzing features, training a tabular prediction model using AutoGluon, and evaluating its performance through Kaggle submissions. The following sections outline the key steps involved in feature creation, model training, and evaluation.

## 1. Feature Creation and Data Analysis

### Feature Engineering
- **New Feature Creation:** A new feature was engineered by extracting and transforming data from an existing feature column. This new feature was then added to both the training and testing datasets to potentially improve model performance.

### Data Visualization
- **Feature Histograms:** Histograms for each feature column in the training dataset were created using `matplotlib`. These visualizations helped in understanding the distribution and characteristics of each feature, guiding further feature engineering and preprocessing.

### Data Type Conversion
- **Data Type Adjustment:** The data types of certain feature columns were changed from numeric to categorical where appropriate. This step was essential for ensuring that the AutoGluon model treated these features correctly during training.

## 2. Model Training with AutoGluon

### Model Training
- **Initial Model Training:** The `TabularPredictor` class from AutoGluon was used to create and train a predictor by calling the `.fit()` method on the training dataset. This model forms the baseline for further tuning and optimization.

### Hyperparameter Tuning
- **Hyperparameter Adjustment:** During model training, additional arguments were provided in the `.fit()` function to modify the hyperparameters. This step was crucial for exploring different model configurations and optimizing performance.

### Model Prediction
- **Making Predictions:** The trained `TabularPredictor` was used to make predictions on the test dataset. These predictions were then prepared for submission to Kaggle for scoring.

## 3. Model Performance Evaluation

### Kaggle Submission
- **Submission to Kaggle:** Predictions from the trained AutoGluon model were submitted to Kaggle using the `kaggle` CLI tool. The public score received from Kaggle provided immediate feedback on model performance.

### Performance Tracking
- **Model Performance Charting:** The project includes a line chart tracking changes in the model evaluation metric (e.g., accuracy, F1 score) after each iteration of model training. The chart was generated using `matplotlib` or spreadsheet software, with the X-axis representing model iterations and the Y-axis representing the evaluation metric.

- **Kaggle Score Tracking:** A similar line chart was created to track the changes in Kaggle competition scores after each model iteration. This visualization helped in identifying trends and assessing the impact of different model configurations.

## 4. Competition Report

### Best Model Identification
- **Model Selection:** The report identifies the best-performing model based on the `fit_summary()` or `leaderboard()` results from AutoGluon. This model was selected as it had the highest evaluation metric on the leaderboard.

### Impact of EDA on Model Performance
- **EDA Findings:** The report discusses how exploratory data analysis (EDA) and feature engineering led to significant discoveries that positively impacted model performance. Specifically, it highlights the role of newly created features and data type adjustments in improving the Kaggle score.

### Hyperparameter Tuning Analysis
- **Hyperparameter Impact:** The report contains a detailed table outlining the different hyperparameters used in each model iteration along with the corresponding Kaggle scores. It also includes an explanation of why certain hyperparameter changes led to improved or diminished performance, providing insights into the model's behavior.
