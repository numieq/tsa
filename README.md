# Numerical Integral Equations for Time Series Analysis
## Motivation
Time series analysis is used in many fields, including finance, economics, engineering, social sciences, and natural sciences. It can be used to forecast future values of the data, estimate the impact of various factors on the data, and identify anomalies or outliers in the data.

The common statistical techniques which are employed for performing the analysis, are, among others, moving averages, autoregressive models and their extensions (e.g., ARIMA, SARIMA), exponential smoothing, and noise filtering . These methods rely on the assumption of some form of ergodicity or stationarity combined with either Gaussian noise or Markovian randomness. Hence, are limited to these constraints. 

The goal of this project is to provied theory and methods from integral equations point of view for handling non-stationary time series, which are driven by non-Gaussian, possibly heavy tailed, noise. 

## Topics
Not all topics of time series analysis are treated here. The focus of this work is on the following topics:
  * Elements of Covariance theory.
  * Generalized Linear estimation.
  * Non-linear estimation techniques.

Our derivation of estimation methods is done in the framework of covariance theory, with minimal a-priori assumptions. The underlying distribution laws are, however, depicted by the properties of the chosen approximation for the covariance matrix.

## Background
Let us cosider a multivariate time series,

$$\\left\\{{\bf X}_t\\right\\}=\\left\\{...,{\bf X}_{t-1},{\bf X}_{t},{\bf X}_{t+1},...\\right\\}$$

where ${\bf X}_t$ is an $m$-dimensionalrandom vector for each $t\in T$ with well defined first and second order statistics.
