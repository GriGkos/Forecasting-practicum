# Forecasting and Statistical Modeling Practicum

A series of Jupyter notebooks on regression diagnostics and classical time-series modeling. The work moves from least-squares model construction and statistical significance tests to residual diagnostics, autoregressive and moving-average processes.

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

### `4.ipynb` — continuation of the forecasting practicum

This notebook is kept in its original executed form as part of the practicum sequence. It is larger than the other notebooks because it contains extensive output and visualizations.

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

## Why this repository is in the portfolio

This is primarily a statistical-modeling repository rather than an end-to-end production forecasting service. Its value is that it shows the mathematical side behind common modeling tools: **least squares, statistical tests, uncertainty intervals, residual diagnostics, ACF/PACF and AR/MA model assumptions**.

That foundation is useful when a forecasting or regression problem requires more than calling a library model and comparing a single metric.
