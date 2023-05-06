# Numerical Integral Equations for Time Series Analysis

## Motivation

Time series analysis is used in many fields, including finance, economics, engineering, social sciences, and natural sciences. It can be used to forecast future values of the data, estimate the impact of various factors on the data, and identify anomalies or outliers in the data.

The common statistical techniques which are employed for performing the analysis, are, among others, moving averages, autoregressive models (e.g., ARMA, ARIMA, SARIMA), exponential smoothing, and noise filtering . These methods rely on the assumption of some form of ergodicity or stationarity combined with either Gaussian noise or Markovian randomness. Hence, are limited to these constraints.

The goal of this project is to provide practical merhods and tools, which are based on numerical integral equations techniques, for prediction and forecasting of non-stationary time series, that are driven by non-Gaussian, possibly, heavy tailed noise.

## Why Integral Equations?

The most general paradign addressing the prediction and forecasting problem is the nonlinear filtering framework. In this framework the particle filter technique is considered the most general method for tackling the problem due to its inherent ability for capturing complex nonlinear relationships between variables and handling non-Gaussian noise.

However, particle filters can be computationally expensive and become unstable, particularly for high-dimensional or complex systems, which can limit their practical use. Simpler techniques, e.g. Extended Kalman Filter or Unscented Kalman Filter, are, typically, attempted in this case with limited success.

Integral equations based techniques are, on the other hand, less general than the particle filter method. However, these techniques alleviate some of the difficulties associated with the particle filter: they can handle nonlinear time series and non-Gaussian noise with controled stability and moderate computational resources.

In this sense, integral equations techniques bridge the gap between the two celebrated mehods, the particle and Kalman filtering techniques, for nonlinear time series prediction and forecasting.

## Background

Let us cosider a multivariate time series,

$$  ...,{\bf X}[t_{-1}],{\bf X}[t_0],{\bf X}[t_1],...  $$

where ${\bf X}[t]$ is an $m$-dimensional random vector for each $t\in T$ with well defined first and second order statistics, and $T$ is a discrete set of values representing succesive sampling points in time.

Let us assume that,

$$ {\bf X}[t] = {\bf s}(t) + {\bf N}[t] $$

where ${\bf s}(t)$ is a useful signal and ${\bf N}[t]$ is an additive noise,
whose mean values are zeros,

$$ \left<{\bf s}(t)\right> = {\bf 0} = \left<{\bf N}[t] \right> $$

and assume the availability of the covariace functions,

 $$ R(t,\tau)=\left<{\bf X}[t]^*\cdot{\bf X}[\tau]\right> $$

and

 $$ f(t,\tau)=\left<{\bf X}[t]^*\cdot{\bf s}(\tau)\right> $$

where the star stands for complex conjugate.

Let $D$ denote the observed domain of the signal. It can be shown, that any linear estimate for the signal,

$$ {\bf s}(t) = \int_Dh(t,\tau){\bf X}_[\tau]{\rm d}\tau $$

minimizing the variance, also satisfies the integral equation

$$ \int_DR(t,\tau)h(s,\tau){\rm d}\tau = f(t,s) \,,\quad t,s\in\overline{D}=D\cup\Gamma $$

where $\Gamma$ denotes the boundary of the doamin, $D$. Thus, unique solvability of the integral equation, ensures the existence and uniqueness of the minimizer.

For handling nonlinear time series, we can replace ${\bf s}(t)$ $\rightarrow$ $A{\bf s}(t)$, where $A$ is a suitable nonlinear operator.

## Topics

Not all topics of time series analysis are treated here. The focus of this work is on the following elements:

* Principles of Covariance theory.
* Generalized Linear estimation.
* Nonlinear estimation techniques.

Our derivation of estimation methods is done in the framework of covariance theory, with minimal a-priori assumptions. The underlying distribution laws are, however, rendered by the properties of the chosen model and construction for the covariance functions, $R(t,\tau)$ and $f(t,s)$.
