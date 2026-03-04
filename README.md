# NIFTY ATM OI–IV Backtest (15‑min)

This project studies how 15‑minute changes in **Open Interest (OI)** and **Implied Volatility (IV)** of NIFTY ATM options relate to market direction, and how the **volatility smile/skew** evolves over time.

## Data
- Underlying: NIFTY index options (ATM strikes)
- Timeframe: 15‑minute data
- Format: One CSV per month in `data/` (OHLC, OI, IV, etc.)

## Main Components
- `notebooks/01_clean_oi_iv_15min.csv` – Load and clean monthly option CSVs, build continuous 15‑min dataset.
- `notebooks/03_oi_iv_signal_backtest.ipynb` – Test rules like “if OI↑ and IV↓ in ATM options, what happens to NIFTY next N bars?”.

## Goals
- Quantify how often specific OI+IV patterns precede up/down moves.
- Analyse volatility smile and skew behaviour during different market regimes.
- Build intuition for using OI/IV and skew as signal inputs.

## Tech Stack
- Python, Pandas, NumPy, Matplotlib/Plotly
- Jupyter Notebooks for research

> Note: CSVs in `data/` can be replaced with any NIFTY options 15‑min dataset using the same columns.
