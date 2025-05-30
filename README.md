# Rainfall-Prediction-Classifier
This project builds a machine learning model to predict whether it will rain tomorrow based on weather data from multiple locations in Australia.

## Overview

The goal is to classify whether it will rain ("Yes") or not ("No") the next day using historical weather features like temperature, humidity, wind speed, and season.

## Project Steps

1. **Data Loading and Cleaning**

   * Loaded weather data from an online CSV file.
   * Removed missing values to ensure data quality.

2. **Feature Engineering**

   * Converted the "Date" column to seasons (Summer, Autumn, Winter, Spring) to capture seasonal effects on rainfall.
   * Filtered data for specific locations to focus the model.

3. **Prepare Features and Target**

   * Separated features (`X`) from the target label (`RainToday`).
   * Split data into training and testing sets to evaluate model performance.

4. **Preprocessing Pipeline**

   * Standardized numeric features (e.g., temperature, humidity).
   * One-hot encoded categorical features (e.g., location, wind direction, season).

5. **Model Building**

   * Used a Random Forest classifier to predict rainfall.
   * Combined preprocessing and model into a pipeline for smooth training.

6. **Hyperparameter Tuning**

   * Applied Grid Search with cross-validation to find the best model parameters (number of trees, max depth, etc.).

7. **Model Evaluation**

   * Evaluated accuracy on the test set.
   * Generated a classification report showing precision, recall, and F1-scores.
   * Plotted a confusion matrix to visualize true vs. predicted labels.

8. **Feature Importance Analysis**

   * Extracted and visualized the most important features the model uses to make predictions.
   * Found that features like humidity, wind speed, and season greatly influence rainfall prediction.

---

## How to Use

* Run the notebook/script to train the model on the weather dataset.
* Evaluate the model with your own data or visualize feature importance.
* Use the trained model to predict rain probability for new weather inputs.

---

## Dependencies

* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn

---
