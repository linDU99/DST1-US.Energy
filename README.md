## U.S. Energy Consumptions

by Lin Ma and Vamsi Vundela 

### Purposes: 
- Visualize patterns of U.S. total energy consumptions over time, 1949-2024
    + Total end-use energy consumption
    + Total electricity consumption (end-use)
    + Energy consumptions by sector: Residential, Commercial, Industrial, and Transportation 

- Forecast future end-use energy and electricity consumptions through 2025-2030
- State level: 2000-2023
    + Track energy loss rate (%) and delivered electricity trends, identify key drivers (GDP, population, prices/spending, heating/cooling degree days (CDD/HDD), pinpoint the sector driving change, and produce 2024–2030 baseline forecasts with uncertainty.

### Datasets:
- Sources:  API of U.S. Energy Information Administration (EIA)
- U.S.-level data: 1949 - 2024
    + EIA Open Data, Total Energy & indicators: www.eia.gov/opendata/
- State-level data: 2000 - 2023
    + State Energy Data System (SEDS): www.eia.gov/opendata/browser/seds

### Directory Structure:
- data: Include the raw data files extracted and the cleaned data files for analysis
- notebooks: The Jupyter Notebook files for data cleaning, EDA exploration, and analysis
- visuals: The analysis outputs

### Main Findings:
- U.S. total end-use energy consumption and electricity use have increased as rising in GDP and population from 1949 to 2024.
- Intensity indicators: 'Energy use per GDP' and 'energy use per capita', which indicate energy efficiency has improved substantially, especially since 1980. However, per-capita electricity use increased consistently from 1949 to 2007, and although it has declined slightly since 2008, it has remained at a high level.
- Accuracy: Gradient Boosting (time-aware CV) predicts state energy loss rate with MAE 2.38, RMSE 3.30, R² 0.93, MAPE 4.54% on 2022–2023.
- Insights & forecasts: Since 2000, energy loss rates show state-specific, gradual shifts; delivered electricity varies widely.

  Within-state drivers: lag-1 energy loss rate, CDD/HDD, and prices/spending (GDP & population weaker). 2024–2030 baseline forecasts (Ridge time-trend) are stable → gently drifting and kept within [0,100]%; detailed sector attribution needs a separate decomposition.
