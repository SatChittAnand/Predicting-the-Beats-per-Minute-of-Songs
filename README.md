# Predicting the Beats Per Minute of Songs

This notebook explores a dataset of song features and aims to predict the beats per minute (BPM) of a song based on these features.

## Dataset

The dataset used in this notebook is from the Kaggle Playground Series - S5E9 competition. It contains various audio features for a large collection of songs, including:

- RhythmScore
- AudioLoudness
- VocalContent
- AcousticQuality
- InstrumentalScore
- LivePerformanceLikelihood
- MoodScore
- TrackDurationMs
- Energy
- BeatsPerMinute (Target variable)

## Notebook Structure

1.  *Data Loading and Initial Exploration*: The notebook starts by loading the training and testing datasets and performing some initial exploration, including displaying the first few rows of the training data and generating descriptive statistics.
2.  *Data Visualization*: Visualizations are used to understand the distribution of each feature and their relationship with the target variable (BeatsPerMinute). This includes:
    - Heatmap of feature correlations.
    - Histograms of individual feature distributions.
    - Scatter plots of each feature against BeatsPerMinute.
    - Box plots of individual feature distributions to identify outliers.
3.  *Feature Selection*: Mutual information regression is used to assess the relationship between each feature and the target variable to identify potentially useful features for modeling.
4.  *Model Training and Evaluation*: Several regression models are trained and evaluated to predict BeatsPerMinute. The models used include:
    - Linear Regression
    - CatBoost Regressor
    - XGBoost Regressor
    The models are evaluated using R-squared, Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE) on training, development, and test sets.
5.  *Submission File Generation*: Finally, predictions are made on the test dataset using the trained XGBoost model, and a submission file is generated in the specified format.

## Dependencies

The following libraries are required to run this notebook:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- catboost
- xgboost
- kagglehub

These dependencies can be installed using ```bash pip    ``` :
