## US Energy consumptions

by Lin Ma and Vamsi Vundela 

### Research Questions:
- Visualize patterns of U.S. total energy consumptions (end-use energy and electricity) over time, 1949-2024
    + Total end-use energy consumption
    + Total electricity consumption (end-use)
    + Energy consumptions by sector: Residential, Commercial, Industrial, and Transportation 

- Forecasting future end-use energy and electricity consumptions through 2025-2030
- State level: 

#### Datasets:
- Sources:  API of U.S. Energy Information Administration (EIA)
##### U.S. level – data: 1949 - 2024
- EIA Open Data, Total Energy & indicators: www.eia.gov/opendata/
##### State level – data: 2000 - 2023
- State Energy Data System (SEDS): www.eia.gov/opendata/browser/seds




Directory Structure:
data: Include the downloaded data files – AQI and wildfires and the analysis data files
notebooks: the Jupyter Notebook files for data cleaning, exploration, and analysis
src: The python scripts and the json scripts for exploratory data analysis (EDA) and data analysis
visuals: All visual maps and analysis outputs
Files Included:
aqi_collector.py - Downloads yearly AQI data from EPA source. Not necessary to run since Github LFS is hosting the file used for this analysis.
aqi_wf_processor.py - Segments and processes both data sources (AQI and wildfire) to produce properly formatted dataframes containing dates and measurements.
geo_plots.py - Geographic data exploration of the datasets (state-wide stations, wildfires, etc.)
stat_plots.py - Statistical data exploration of the datasets (Time-series exploration)
visualizer_folium.py - Heatmap chart of the dataset, interactive
DataExploration.ipynb - Jupyter notebook stepping through the download, processing, and geo/temporal exploratory anaylsis.
DataAnalysis.ipynb - Jupyter notbeook containing the seasonal and trend analyses of the dataset
Main Findings:
