# Real-Time Rain Monitoring using Communication Satellites

![Project Image](https://github.com/clementsiegrist/Rain-Prediction-with-LSTM/blob/main/DALL%C2%B7E%202023-11-03%2019.11.33%20-%20Photo%20of%20a%20large%20satellite%20dish%20positioned%20prominently%20in%20the%20foreground%2C%20with%20droplets%20of%20rain%20visibly%20falling%20around%20it.%20The%20sky%20is%20overcast%20with%20da.png)

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.md)
[![Python Version](https://img.shields.io/badge/python-3.7%20%7C%203.8%20%7C%203.9-blue)](https://www.python.org/downloads/)

## Introduction and Context

This project focuses on real-time rain monitoring using communication satellites. By analyzing the carrier-to-noise (C/N) ratio, which correlates with rain intensity, it's possible to create rain maps for regions with high spatial resolution.

## Exploratory Data Analysis

The project utilizes the `ydata-profiling` library for automated Exploratory Data Analysis (EDA) to understand the dataset better.

## Data Preprocessing and Cleaning

Data preprocessing involves converting timestamps, handling missing values, normalizing data, and feature engineering. External geophysical and geographical features can also be incorporated for better predictions.

## Deep Learning for Time Series Regression

The project considers various machine learning algorithms, including polynomial linear regression and random forests for explainability. Deep learning models such as RNNs, LSTMs, Bi-LSTMs, Long-Long-Memory, ConvLSTM, and Transformers are explored for capturing temporal dependencies.

## Subtask Splitting

The project suggests splitting the task into two subtasks: classifying timestamps into rain/dry events and estimating rain intensity for rainy timestamps, with potential benefits in handling imbalances and filtering data based on classification confidence.

## Handling Missing Data

Missing data is handled through imputation methods like rolling mean interpolation and forward/backward fill.

## Creating Features

Feature engineering includes datetime features, time series derivatives, and potentially external/geophysical, geographical features to enhance model performance.

## External/Geophysical, Geographical Features

Consideration is given to incorporating external and geographical features to improve rain intensity predictions by accounting for factors like wind speed, temperature, atmospheric conditions, and more.

## Data Ingestion and Pipeline

- Data Ingestion: Tools like Apache NiFi, Cloudera miNifi, or Fluentd are used to monitor the directory where new CSV files with C/N data are pushed by satellite operators every five minutes. These tools ingest the data in real-time and forward it to the pipeline.

- Data Processing: Data preprocessing involves optimizing data processing with libraries like Numba or Dask, or using distributed processing frameworks like Apache Spark or Apache FLink. It may also involve optimizing deep learning models for speed using techniques like quantization or custom hardware accelerators.

- ML/DL Inference: The trained LSTM model is deployed for real-time inference, potentially using TensorFlow Serving, ONNX Runtime, or cloud compute services with optimized hardware like TPUs.

- Data Storage: Processed data and model predictions are stored in databases like InfluxDB, TimescaledDB, QuestDB, or cloud-based time series databases like AWS Timestream, depending on factors like ingestion rate and query performance.

- API Layer: An API layer is created using web frameworks like Flask, Django, or FastAPI to provide customers with access to rain map results.

- Monitoring and Alerting: Tools like Prometheus and Grafana are used for monitoring pipeline health, and alerts are set up for detecting issues.

- Orchestration: Kubernetes is used for managing components like scaling, failover, and operational concerns.

- CI/CD: Continuous Integration and Continuous Deployment pipelines (e.g., Jenkins, GitLab CI/CD) are used for maintaining the codebase, automating tests, and deploying changes to the pipeline.

## Multi-Terminal Algorithm

A multi-terminal algorithm is proposed for rain intensity estimation using data from multiple satellite dishes. It involves data collection, preprocessing, dataset formatting, complex real-time inference, on-terminal data acquisition synchronization, and considering geographical dependencies and relations. Advantages and disadvantages of multi-terminal algorithms are discussed.

## Code Snippets

Code snippets are provided for simulating data from multiple terminals, normalizing data, and building a multi-terminal LSTM model for rain intensity prediction.
