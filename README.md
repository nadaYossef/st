# Starbucks Capstone Project

![image](https://github.com/user-attachments/assets/eab00f51-2f2a-46f9-964c-dd2b6715f65f)

blog post: https://medium.com/@nadaayoussef.202/brewing-insights-unleashing-data-science-to-transform-starbucks-customer-experience-4ba62926c48a

## Table of Contents
- [Overview](#overview)
- [Motivation](#motivation)
- [Libraries Used](#libraries-used)
- [Files](#files)
  - [portfolio.json](#portfoliojson)
  - [profile.json](#profilejson)
  - [transcript.json](#transcriptjson)
- [Techniques and Algorithms](#techniques-and-algorithms)
- [Summary of Results](#summary-of-results)
- [Challenges](#challenges)
- [How to Deploy](#how-to-deploy)
- [Acknowledgements](#acknowledgements)

## Overview

This project is a part of the Udacity Data Science Nanodegree program. The goal is to analyze customer behavior and spending patterns related to offers and memberships at Starbucks. The insights derived from this analysis aim to help optimize marketing strategies and enhance customer engagement.

## Motivation

Understanding customer preferences is crucial in the competitive landscape of the coffee shop industry. This project seeks to provide valuable insights that can improve marketing efforts and increase customer satisfaction through targeted promotions and offers.

## Libraries Used

This project utilizes several Python libraries for data analysis, visualization, and machine learning, including:

- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `math`: For mathematical functions.
- `json`: For parsing JSON data.
- `matplotlib`: For creating static visualizations.
- `seaborn`: For enhanced visualizations.
- `plotly.express`: For interactive visualizations.
- `sklearn`:
  - `preprocessing.MultiLabelBinarizer`: For transforming multiple label columns into binary format.
  - `model_selection.train_test_split`: For splitting datasets into training and testing sets.
  - `ensemble.RandomForestClassifier`: For implementing the Random Forest classification algorithm.
  - `ensemble.HistGradientBoostingClassifier`: For using the Histogram-based Gradient Boosting classifier.
  - `metrics.accuracy_score`: For evaluating the accuracy of the model.
  - `metrics.classification_report`: For generating a classification report.
  - `metrics.confusion_matrix`: For generating a confusion matrix.
  - `metrics.ConfusionMatrixDisplay`: For visualizing the confusion matrix.
  - `model_selection.cross_val_score`: For performing cross-validation.
  - `model_selection.RandomizedSearchCV`: For hyperparameter tuning using randomized search.
- `scipy.stats`: For statistical distributions, including uniform and random integers.

## Files

### portfolio.json
- **Description**: Contains information about offers.
  - **Offer ID**: Unique identifier for each offer.
  - **Offer Type**: The category of the offer (e.g., BOGO, discount, informational).
  - **Difficulty**: Minimum required spending to complete an offer.
  - **Reward**: Incentive provided for completing an offer.
  - **Duration**: Time period during which the offer is valid (in days).
  - **Channels**: Platforms through which the offer is communicated (e.g., mobile, email).

### profile.json
- **Description**: Contains customer demographic information.
  - **Customer ID**: Unique identifier for each customer.
  - **Age**: The age of the customer.
  - **Gender**: The gender of the customer (with some entries marked as 'O' for other).
  - **Income**: The income level of the customer.
  - **Became Member On**: The date when the customer registered on the app.

### transcript.json
- **Description**: Contains interaction events between customers and the app.
  - **Event**: Type of interaction (transaction, offer received, offer viewed, offer completed).
  - **Person**: Customer ID associated with the event.
  - **Time**: Time (in hours) since the start of the test.
  - **Value**: Either the offer ID or transaction amount, depending on the event.

*Note: The data was too large to upload on GitHub but can be downloaded from [this link](https://drive.google.com/file/d/1Kd1a6oG_p2JBTn66_4a4kIIt8Tz-0sk6/view?usp=sharing).*

## Techniques and Algorithms

- **Mapping Encoding**: Used to prepare categorical data for analysis.
- **MultiLabelBinarizer Encoder**: Applied for transforming multiple label columns into binary format.
- **Model Selection**: The `HistGradientBoostingClassifier` outperformed the Random Forest due to its ability to handle complex relationships within the data effectively, indicated by its higher accuracy and better handling of classes.
- **Hyperparameter Tuning**: Tuning parameters improved the model's performance without drastically altering its characteristics, reinforcing the importance of optimizing models for better accuracy and generalization.
- **Validation Techniques**: Cross-validation provided assurance against overfitting, confirming that the model’s performance was not merely a result of random chance.

## Summary of Results

For detailed results of the analysis, refer to the [Starbucks Capstone Notebook](https://github.com/nadaYossef/starbucks_capstone_project/blob/main/Starbucks_Capstone_notebook.ipynb).

## Challenges

- Handling a lot of missing values while merging the dataframes into one without losing significant data. 
- Imputing some values and dropping others posed challenges in maintaining data integrity.

## How to Deploy

Just copy the data files and run all the cells in your local device.

## Acknowledgements

The data was taken directly from the workspace of the project from the Data Science Capstone section course Jupyter directory.
