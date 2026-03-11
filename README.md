# ESG Analytics: Digital Twin for Solar-Powered Data Center Efficiency
A Predictive Modeling & Optimization Framework for Real-Time Carbon-Free Energy Matching

Malaysia has emerged as a premier regional hub for digital infrastructure. Despite this economic growth, data centers contribute 1–2% of global greenhouse gas emissions, surpassing the commercial airline industry (IEA, 2024). 
This project introduces a Digital Twin framework—a virtualized model of a solar-integrated data center. By leveraging:
- Random Forest Regressor (Scikit-Learn)
- LSTM (PyTorch, Deep Learning)

## Objectives
- Predicts Solar Supply: Analyzes real-time weather and irradiance data (via NREL/Data.gov) to forecast energy generation.
- Optimizes Demand Side Management: Dynamically aligns non-critical computing tasks with peak solar hours to minimize reliance on the carbon-heavy national grid.
- Measure ESG Impact

## Scope of Study
- Location: Kulai, Johor
- Data period: 2018 - 2024
- Frequency: Mixed (Hourly Weather, Monthly Solar Capacity)
- Forecast Horizon: 24-Hour Day-Ahead Solar Yield

## Datasets
1. Electricity consumption
   - data source: data.gov.my
   - data type: .json
2. Capacity and generation
   - data source: SEDA Malaysia SEIP
   - data type: .csv
3. Weather 
   - data source: kaggle
   - data type: .csv.zip

## Tools and Technologies
- Language: Python
- Environment: Jupyter Notebook
- Libraries:
  - Data: pandas, numpy, requests
  - ML/ DL: scikit-learn, pytorch
  - Visualization: matplotlib, seaborn

## ETL/ Data Pipelines
1. Data extraction
2. Data Transformation:
   - Standardize data types and formats
      - Electricity : date, object dtype to datetime
      - Capacity : Year, int dtype to datetime
      - Weather : date_time, object dtype to datetime
   - Change column name
      - Electricity : date to Date
      - Capacity : Year to Date
      - Weather : date_time to Date
   - Set Data range
      - Date : 2018 - 2024
      - City : Kulai
4. Reset index
5. Drop column
6. Handle missing value
7. Create relevant columns
3. Data Load
