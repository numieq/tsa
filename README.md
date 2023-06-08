# Numerical Integral Equations for Random Fields Estimations and Simulations

## Motivation

Random fields refer to stochastic models that describe the variation of a random quantity over a multidimensional space. In fact, a random field is a generalization of a stochastic process where the underlying parameter need no longer be real or integer valued "time" but can instead take values that are multidimensional vectors or points on some manifold.

Random fields applies in various fields, including finance, image processing, environmental modeling, and geostatistics, aning others. It can be used to perform data assimilation, model uncertainties, estimate the impact of various factors on the data, and identify anomalies or outliers in the data.

Random field estimation involves specifying a suitable model and estimating its parameters based on observed data. It is an essential step in analyzing and understanding spatial or spatiotemporal data and allows for making predictions and inferences about the underlying random field.

The common statistical techniques for performing estimations over random fields rely on the assumption of some form of ergodicity or stationarity combined with either Gaussian noise or Markovian randomness. Hence, are limited to these constraints.

The goal of this project is to provide practical methods and tools, which are based on numerical integral equations techniques, for analysis and estimation of non-stationary random fields, that are driven by non-Gaussian, possibly, heavy tailed noise.

## Why Integral Equations?

The commonly used techniques for random field estimation are maximum likelihood, method of moments, Bayesian estimation and Monte Carlo, among others. These methods are either oversimplifeid or require substantial computational effort both in preprocessing the data and solving a, typically, complex optimization problem.

[//]: <The most general paradigm addressing the prediction and forecasting problem is the nonlinear filtering framework. In this framework the particle filter technique is considered the most general method for tackling the problem due to its inherent ability for capturing complex nonlinear relationships between variables and handling non-Gaussian noise.>

Integral equations based techniques are, on the other hand, less general than the computationally demanding methods detailed above. However, these techniques can handle nonlinear complexities and non-Gaussian noise with controled stability and moderate computational resources.

In this sense, integral equations techniques bridge the gap between the over simplified and over complicated methods for nonlinear and non Gaussian random fields esimations and simulations.

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
