# pso318-spectral-fit

Chi-square fitting of the PSO318-22 spectrum against the SM08 model grid across Teff, log g and fsed (Python, Jupyter).

Undergraduate project. Code for viewing only. Exploratory: there is no report or published result.

## What the notebook does

1. Loads the observed spectrum (wavelength, flux, flux error) and drops rows with missing values.
2. Loads a grid of model spectra (8 Teff x 4 log g x 4 fsed values, read from the model filenames).
3. Bins each model to R = 100 over 0.6-20 um with the `coronagraph` package, then interpolates it onto the observed wavelengths.
4. For each model, solves for the best-fit scale factor and computes the chi-square against the data.
5. Picks the model with the lowest chi-square and plots it against the data.

## Data

The data are not included in this repo, so the notebook can't be run as-is. The code is here to show the method.

- Spectrum: `PSO318-22.csv` (columns: `wavelength`, `flux`, `flux_err`). Provided as part of the project; original source not recorded.
- Models: SM08 grid files named like `sp_t1500g3000f2`. Provided as part of the project; original source not recorded.
