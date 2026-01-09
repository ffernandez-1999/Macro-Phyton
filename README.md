# BCRA FX Bands Tracker

Python project that reconstructs and visualizes the Argentine FX bands scheme.

The script combines the wholesale exchange rate (A3500) with a daily FX bands system, following the rules applied by the BCRA during 2025 and 2026.

## What the project does

- Downloads the official A3500 exchange rate from the BCRA.
- Builds daily FX bands using two different regimes:
  - **2025:** fixed ±1% monthly bands, converted to daily rates.
  - **2026:** inflation-based bands, updated monthly with a **t−2 lag**, using:
    - official CPI when available,
    - REM inflation expectations as a fallback.
- Merges daily bands with observed FX data (business days only).
- Produces a final chart showing the exchange rate and FX bands.

## Data sources

- BCRA – Wholesale exchange rate (A3500)
- BCRA – REM inflation expectations
- INDEC / datos.gob.ar – Monthly CPI (headline)

## Output

- Daily dataset with:
  - lower FX band
  - upper FX band
  - observed A3500 exchange rate
- High-resolution chart for analysis and reporting.

## Technologies

- Python
- pandas
- numpy
- matplotlib
- numpy
- matplotlib
