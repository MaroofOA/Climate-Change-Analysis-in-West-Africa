# Climate Change Analysis in West Africa: Forecasting Temperature Trends for Enhanced Resilience

## Overview
This project aims to analyze historical temperature data for 15 West African countries over the period 1980–2022 to study climate change trends and assess their broader implications. Given the growing impact of climate change on key sectors such as agriculture, water resources, and public health in Africa, this project compares three different time series forecasting models (ARIMA, Prophet, and VAR) to predict temperature trends. By comparing the models, the project seeks to determine which one is most effective for accurate climate forecasting in this region.

## Problem Statement
Africa faces significant challenges due to climate change, especially in areas such as agriculture, water resources, and public health. This project aims to analyze historical temperature data (1980-2022) from West African countries to understand climate change patterns and their implications, with a focus on temperature trends and their broader effects.

## Data Source
The data was sourced from the National Centers for Environmental Information (National Oceanic and Atmospheric Administration) through the Global Historical Climatology Network Daily (GHCNd) dataset. It includes temperature records from 72 weather stations across the 15 West African countries.

- [Access the dataset here](https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND)

## Objectives
1. Investigate long-term temperature trends across West Africa, identifying variations and patterns.
2. Develop location-specific forecasting models to predict extreme temperatures using historical data.
3. Compare ARIMA, Prophet, and VAR time series models and analyze their prediction accuracy.

## Data Description
The dataset consists of daily temperature records (minimum, maximum, and average) from January 1st, 1980 to December 31st, 2022 across 15 West African countries. The stations are identified by latitude, longitude, elevation, and country. 

- Mean Temperature: 24.63°C 
- Standard Deviation: 2.73°C
- Temperature Range: 15.56°C to 32.22°C

The dataset provides a comprehensive view of long-term temperature patterns in the region.

## Data Preparation
- Data from 15 countries was consolidated into a single dataset.
- Missing values exceeding 30% were removed, and smaller gaps were filled using forward-fill methods.
- Temperature readings were converted from Fahrenheit to Celsius for standardization.
- Station metadata, including latitude, longitude, elevation, and country, was merged with the temperature data.
- The resulting processed dataset is saved as `West_Africa_temperature_1980_2022.csv` and station-specific metadata as `Station_metadata.csv`.

## Models and Forecasting
The project compares three forecasting models for temperature trend prediction:
1. **ARIMA (AutoRegressive Integrated Moving Average)**
   - Training Time: 73.27 seconds
   - Mean Absolute Error (MAE): 1.05
   - Root Mean Squared Error (RMSE): 1.4

2. **Facebook Prophet**
   - Training Time: 13.28 seconds
   - Mean Absolute Error (MAE): 1.53
   - Root Mean Squared Error (RMSE): 1.96

3. **Vector AutoRegressive Model (VAR)**
   - Training Time: 0.51 seconds
   - Mean Absolute Error (MAE): 2.88
   - Root Mean Squared Error (RMSE): 3.54

## Results
- **ARIMA** performed the best, achieving the lowest MAE and RMSE.
- **Prophet** was faster to train but had slightly higher error rates.
- **VAR** performed the worst among the three, with the highest error rates but was the fastest to test.

## Conclusions
The analysis revealed that ARIMA offers the most accurate forecasts for temperature trends in West Africa. Prophet also performed well, especially in terms of speed, while VAR's performance was suboptimal. These models can be useful for policymakers and researchers working on climate resilience, helping them plan for future temperature changes in the region.

## Files
- `West_Africa_temperature_1980_2022.csv`: Contains the processed temperature data for West African countries from 1980 to 2022.
- `Station_metadata.csv`: Contains metadata for the temperature stations, including station ID, latitude, longitude, elevation, and country.
- `climate_change_analysis.ipynb`: Jupyter Notebook that includes the code for data processing, model training, and evaluation.
- `README.md`: This documentation file.
