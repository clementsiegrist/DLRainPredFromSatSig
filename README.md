# Rain-Prediction-with-LSTM

# Real-Time Rain Monitoring using Communication Satellites

![Project Image](insert_link_to_context_photo_here)

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.md)
[![Python Version](https://img.shields.io/badge/python-3.7%20%7C%203.8%20%7C%203.9-blue)](https://www.python.org/downloads/)

## Introduction and Context

In communication satellite systems, satellite operators monitor the connection to each of their satellite dishes (internet users everywhere on Earth) in real-time. This parameter is the carrier-to-noise (C/N) ratio, which can be understood as the signal-to-noise ratio and is measured in dB. In case of rain above the terminal, the signal drops, and there is a clear correlation between the amount of signal drops and the rain intensity. As the signal is almost only impacted by rain, it can be used as a virtual rain sensor. More precisely, it can be seen as a point measurement of rain at the location of the satellite dish. Combining many of these rain point measurements allows for creating rain maps for a full region with, for example, 1km x 1km spatial resolution.

## Data Visualization Process using RainDataPlotter

The `RainDataPlotter` class provides a convenient way to visualize rain data from one or multiple DataFrames. The class allows you to plot line, scatter, and histogram plots for selected variables with customizable options such as the sampling rate.
