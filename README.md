# Dynamic Multiplier Estimation for VAR-X / Reduced Form SVAR-X Models

<p align="center">
  <img src="https://noodle.digitalfutures.com/studentuploads/DMS.png" alt="DMS Image" />
</p>

This Python function estimates **dynamic multipliers** (impulse response functions) from a Vector Autoregression with exogenous variables (VAR-X) or reduced-form SVAR-X using ordinary least squares (OLS). It captures how shocks to exogenous variables affect endogenous variables over a user-defined horizon.

---

## Features

- Computes dynamic multipliers.
- Calculates confidence intervals using the delta method with a customizable significance level.
- Supports flexible lag lengths for endogenous and exogenous variables.
- Offers plotting options: individual response plots or grid layout.
- Returns results as a Pandas DataFrame and NumPy arrays for further analysis.

---

## Documentation

- The file named `dynamic_multiplier.py` contains the main function.
- The file named `example_usage.py` demonstrates how to use the function.

---

## Parameters

- **df** (`pandas.DataFrame`, *required*)  
  Input dataset containing all endogenous and exogenous variables.

- **endog_vars** (`list` of `str`, *required*)  
  Names of the endogenous variables to analyse.

- **exog_vars** (`list` of `str`, *required*)  
  Names of the exogenous variables (shocks) whose effects are to be estimated.

- **endog_lags** (`int`, *required*)  
  Number of lags to include for the endogenous variables (starting from lag 1).

- **exog_lags** (`int`, *required*)  
  Number of lags for exogenous variables (including lag 0).

- **horizons** (`int`, *required*)  
  Number of time periods (horizons) over which to compute dynamic multipliers.

- **constant** (`bool`, default `True`)  
  Whether to include a constant term in the OLS regressions.

- **alpha** (`float`, default `0.05`)  
  Significance level for confidence intervals (e.g., 0.05 for 95% CI).

- **round_digits** (`int`, default `4`)  
  Number of decimal places to round the output results.

- **plot_style** (`str`, default `'individual'`)  
  Plotting style: `'individual'` to plot separate charts per response, `'grid'` for a matrix layout.

- **color** (`str`, default `'blue'`)  
  Colour of the impulse response function lines in the plots.

---

## Installation

Requires the following Python packages:

- `numpy`
- `pandas`
- `matplotlib`
- `statsmodels`
- `scipy`

Install via pip if needed:

```bash
pip install numpy pandas matplotlib statsmodels scipy

