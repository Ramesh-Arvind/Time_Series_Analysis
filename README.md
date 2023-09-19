# Time Series Analysis with Python

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
11. [Conclusion](#conclusion)

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

The powerful Holoviews library is utilized to create interactive visualizations, allowing us to effectively explore and visualize the demand trends within the dataset.


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

## Conclusion

This repository provides a comprehensive guide and codebase for conducting time series analysis and anomaly detection on the New York City taxi demand dataset. The code can be customized and extended for similar time series analysis tasks.
