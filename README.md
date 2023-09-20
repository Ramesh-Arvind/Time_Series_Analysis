# Time Series Analysis with Statistical methods and ML Forecasting for Anomaly Detection

This repository contains Python code and data for performing time series analysis on New York City taxi demand data.

## Table of Contents

1. [Introduction](#introduction)
2. [Setup](#setup)
3. [Loading and Preparing the Dataset](#loading-and-preparing-the-dataset)
4. [Data Quality Check](#data-quality-check)
5. [Resampling and Visualization](#resampling-and-visualization)
6. [Time Series Decomposition](#time-series-decomposition)
7. [Stationarity Check](#stationarity-check)
8. [Outlier Detection](#outlier-detection)
9. [Visualization of Outliers](#visualization-of-outliers)
10. [QQ Plot for Normality Testing](#qq-plot-for-normality-testing)
11. [Machine Learning and Anomaly techniques](#machine-learning-unsupervised-techniques-and-anamoly-detection)
12. [Conclusion](#conclusion)

## Introduction

In this project, we perform time series analysis on New York City taxi demand data to gain insights into demand patterns, seasonality, and outliers.

## Setup

To run the code in this repository, you'll need to set up a Python environment with the required libraries. You can use the provided `requirements.txt` file to install the dependencies.
pip install -r requirements.txt

## Loading and Preparing the Dataset

The dataset used in this analysis is the New York City taxi demand dataset, which is part of the Numenta Anomaly Benchmark (NAB). You can download the dataset from [here](https://www.kaggle.com/datasets/boltzmannbrain/nab). 

In this section, we load and prepare the dataset for analysis.

## Data Quality Check

Before diving into the analysis, it's essential to ensure data quality. We perform a thorough data quality check by examining the dataset for missing values and reviewing the data types. The `blank_data_check` function is used to provide a summary of the data's quality, including the date range.

## Resampling and Visualization

To gain deeper insights from the time series data, we employ resampling techniques to convert the data into different time intervals, such as hourly, daily, and weekly. 

The powerful Holoviews library is utilized to create interactive visualizations, allowing us to effectively explore and visualize the demand trends within the dataset [here](images)

## Time Series Decomposition

We perform a seasonal decomposition of the time series data to extract key components, including trends, seasonality, and residuals. This decomposition helps us understand the underlying patterns in the data.

## Stationarity Check

We check for stationarity in the time series data using Augmented Dickey-Fuller (ADF) and Kwiatkowski-Phillips-Schmidt-Shin (KPSS) tests. Stationarity is essential for accurate time series modeling.

## Outlier Detection

Detecting outliers is crucial in time series analysis. We employ various methods, including the modified Z-score and interquartile range (IQR), to identify unusual data points that might indicate anomalies or errors..

## Visualization of Outliers

We visualize the identified outliers using different plots, such as box plots, violin plots, and lag plots. These visualizations help us understand when and where anomalies occur in the time series.

## QQ Plot for Normality Testing

We employ quantile-quantile (QQ) plots to test if the data follows a normal distribution. This is important for selecting appropriate statistical models.

## Machine Learning Unsupervised techniques and Anamoly Detection
### Scenario 1: Outlier Detection with K-Nearest Neighbors (KNN)
**Note**: In this scenario, we applied the K-Nearest Neighbors (KNN) algorithm to detect outliers in the taxi demand data. KNN is a robust method for identifying unusual data points by measuring their proximity to neighboring data points. We chose KNN for its simplicity and effectiveness in handling multi-dimensional data.

### Scenario 2: Copula-Based Outlier Detection
**Note**: Copula-based outlier detection is a powerful technique that captures complex dependencies between variables. We utilized this method to uncover anomalies in our time series data. Copulas provide a flexible framework for modeling dependencies and offer a deeper understanding of extreme events in the data.

### Scenario 3: One-Class SVM (OCSVM) with Multiple Kernels
**Note**: Our exploration of One-Class SVM (OCSVM) involved testing multiple kernels, including linear, polynomial, radial basis function (RBF), and sigmoid. By experimenting with various kernels, we aimed to find the one that best suited the underlying data distribution. OCSVM with the RBF kernel, for example, effectively captured non-linear relationships in the data, demonstrating the importance of kernel selection in anomaly detection.

### Scenario 4: Anomaly Detection with PyCaret
**Note**: PyCaret's low-code machine learning capabilities allowed us to easily experiment with different anomaly detection models. By leveraging PyCaret, we streamlined the model selection and evaluation process. The library's user-friendly interface and comprehensive model comparison enabled efficient identification of anomalies in our time series data.

### Scenario 5: Time Series Forecasting with ARIMA
**Note**: AutoRegressive Integrated Moving Average (ARIMA) modeling played a crucial role in forecasting taxi demand. By fitting an ARIMA model to historical data, we captured temporal dependencies and seasonal patterns. This forecasting technique provides valuable insights into future demand trends, aiding in decision-making and resource allocation.

### Scenario 6: Time Series Forecasting with Facebook Prophet
**Note**: Facebook Prophet emerged as a powerful tool for forecasting time series data with seasonality and holidays. Prophet's ability to handle these factors makes it an ideal choice for modeling and predicting taxi demand. Its flexibility and intuitive parameter tuning made it a valuable addition to our forecasting toolkit.


## Conclusion
In this analysis, we applied the Prophet time series forecasting model to predict future demand for New York City taxi services. After adapting the dataset and fitting the Prophet model, we extended the forecasting horizon to provide forecasts for an additional 7 days.

The forecasted demand, represented by the red line in the plot, appears to capture the underlying patterns and trends in the data effectively. The shaded region between the lower and upper bounds of the forecast provides a measure of uncertainty.

Key Findings:
- The Prophet model demonstrates the ability to capture daily and weekly seasonality in the demand for taxi services.
- The forecasted values align well with the observed data, indicating that the model can be useful for predicting future demand.

## Acknowledgments

Special thanks to the New York City Taxi and Limousine Commission for providing the dataset.
For holoviews visualization : Josh from kaggle
