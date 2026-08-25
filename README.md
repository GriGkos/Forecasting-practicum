# Forecasting and Statistical Modeling Practicum

A series of Jupyter notebooks on regression diagnostics and classical time-series modeling. The work moves from least-squares model construction and statistical significance tests to trend/seasonality analysis, residual diagnostics, autoregressive and moving-average processes.

`Python` · `NumPy` · `pandas` · `SciPy` · `statsmodels` · `scikit-learn` · `Matplotlib`

## What is covered

The notebooks include:

- construction of regression design matrices;
- ordinary least squares implemented from matrix formulas;
- comparison of polynomial and nonlinear model forms;
- coefficient significance testing;
- confidence intervals for coefficients and predictions;
- Fisher and Student statistical tests;
- residual diagnostics and model-adequacy checks;
- trend removal and differencing;
- stationarity diagnostics with the Augmented Dickey–Fuller test;
- seasonal-pattern estimation with Fourier terms, time-slot indicators and seasonal differencing;
- autocorrelation analysis with ACF/PACF;
- stationarity and invertibility conditions;
- autoregressive `AR` models;
- moving-average `MA` models;
- classical `ARIMA` tooling from `statsmodels`.

## Notebook progression

### `1.ipynb` — model construction and least squares

The first notebook works with different functional model forms, builds the experiment/design matrix explicitly and implements least-squares estimation. It compares fitted relationships using numerical and visualization tools rather than relying only on a ready-made estimator.

### `2.ipynb` — significance and confidence intervals

The second notebook focuses on statistical inference around a fitted regression model:

- Student tests for coefficient significance;
- Fisher comparison of nested models;
- confidence intervals for coefficients;
- confidence and prediction intervals;
- a model containing polynomial and Fourier components.

### `3.ipynb` — model adequacy and residual diagnostics

The third notebook checks whether the regression assumptions are reasonable. The analysis includes residual behavior, tests related to constant expectation/variance and autocorrelation diagnostics using `statsmodels`.

### `4.ipynb` — trend, stationarity and seasonality

The fourth notebook studies two time series from `TimeSeries.xls` and separates deterministic trend from periodic behavior.

For the pressure series it covers:

- visual trend and ACF analysis;
- least-squares estimation of a linear trend;
- detrending and first differences;
- Augmented Dickey–Fuller tests under several deterministic specifications;
- comparison of the original and differenced series from a stationarity perspective.

For the flow series it identifies a daily seasonal period of **12 observations** at a two-hour sampling interval and compares several ways of removing that periodic component:

- a non-singular Fourier basis for period 12;
- time-of-day indicator variables;
- direct per-slot seasonal means;
- seasonal differencing with lag 12.

The notebook also compares residual ACF and variance across the seasonal-adjustment approaches. The indicator and per-slot-mean formulations are shown as equivalent representations of the same 12-slot seasonal profile.

### `5.ipynb` — autoregressive models

The AR section studies autoregressive processes analytically and numerically. Examples include:

- stationarity through characteristic roots;
- ACF recurrence using Yule–Walker relationships;
- ACF/PACF visualization;
- fitting/working with autoregressive models through `statsmodels`.

### `6.ipynb` — moving-average models

The final notebook covers MA processes, including:

- stationarity and invertibility;
- characteristic roots;
- analytical autocorrelation structure;
- ACF/PACF diagnostics;
- use of `ARIMA` tooling for classical time-series modeling.

## Data

The repository contains the original `.xls` datasets used by the notebooks:

```text
TimeSeries.xls
ls_variants.xls
```

The notebooks expect these files to be available in the repository root when run locally.

## Running locally

Install the dependencies:

```bash
pip install -r requirements.txt
```

Then start Jupyter and run the notebooks from the repository root so the relative paths to the `.xls` files remain valid.

## Why this repository is in the portfolio

This is primarily a statistical-modeling repository rather than an end-to-end production forecasting service. Its value is that it shows the mathematical side behind common modeling tools: **least squares, statistical tests, uncertainty intervals, trend and seasonality, residual diagnostics, ACF/PACF and AR/MA model assumptions**.

That foundation is useful when a forecasting or regression problem requires more than calling a library model and comparing a single metric.
