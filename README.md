# Mar-a-Aranguren
# Spanish electricity market analysis
This repository contains a small, end-to-end analysis of Spanish day-ahead electricity prices using publicly available OMIE data.
The goal is not to build complex models, but to show how market data can be:
- analysed,
- turned into operational signals,
- and queried efficiently for decision support.

## Structure

### Forecasting and market context
The first notebook focuses on understanding recent price behaviour and producing a simple, explainable short-term forecast.
It covers:
- historical price patterns,
- weekday vs weekend effects,
- intraday behaviour,
- a lightweight daily forecast with basic validation.

### Operational monitoring
The second notebook adds an operational layer on top of the same data.
It implements simple alert rules to flag:
- unusually expensive days,
- high intraday volatility,
- extreme hourly price peaks.
The output is designed to support routine monitoring rather than replace human judgement.

### SQL-based market views
The final notebook answers common market questions using SQL only.
It focuses on:
- ranking expensive and cheap days,
- isolating evening price exposure,
- identifying unstable days,
- and tracking short-term trends.
This mirrors real-world workflows where SQL is used for fast, reproducible analysis on structured data.

## Data
The analysis uses OMIE Spain day-ahead price data, stored as a CSV file in the `data/` folder.
The dataset is included to keep the notebooks fully reproducible.

## Tools
- Python (pandas, matplotlib)
- Jupyter notebooks
- SQLite for SQL analysis

## Notes
The emphasis throughout the project is on clarity, explainability, and practical use cases, rather than model complexity.
