# Numerical Integral Equations for Time Series Analysis
## Motivation
Time series analysis is used in many fields, including finance, economics, engineering, social sciences, and natural sciences. It can be used to forecast future values of the data, estimate the impact of various factors on the data, and identify anomalies or outliers in the data.

The common statistical techniques which are employed for performing the analysis, are, among others, moving averages, autoregressive models (e.g., ARMA, ARIMA, SARIMA), exponential smoothing, and noise filtering . These methods rely on the assumption of some form of ergodicity or stationarity combined with either Gaussian noise or Markovian randomness. Hence, are limited to these constraints.

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

where ${\bf X}_t$ is an $m$-dimensional random vector for each $t\in T$ with well defined first and second order statistics, and $T$ is a discrete set of values representing succesive sampling points in time.

Let us assume that,

$$ {\bf X}_t = {\bf s}(t) + {\bf n}(t) $$

where ${\bf s}(t)$ is the useful random signal and ${\bf n}(t)$ is an additive noise,
whose mean values are zeros,

$$ \left<{\bf s}(t)\right> = {\bf 0} = \left<{\bf n}(t)\right> $$

and assume the availability of the covariace functions,

 $$ R(t,\tau)=\left<{\bf X}_t^*\cdot{\bf X}_{\tau}\right> $$

and

 $$ f(t,\tau)=\left<{\bf X}_t^*\cdot{\bf s}(\tau)\right> $$

where the star stands for complex conjugate.

Let $D$ denote the observed domain of the signal. It can be shown, that any linear estimate for the signal,

$$ {\bf s}(t) = \int_Dh(t,\tau){\bf X}_{\tau}{\rm d}\tau $$

minimizing the variance, also satisfies the integral equation

$$ \int_DR(t,\tau)h(s,\tau){\rm d}\tau = f(t,s) \\,,\\quad t,s\in\overline{D}=D\cup\Gamma $$

where $\Gamma$ denotes the boundary of the doamin, $D$. Thus, unique solvability of the integral equation, ensures the existence and uniqueness of the minimizer.
