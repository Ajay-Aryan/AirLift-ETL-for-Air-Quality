# Dynamic AirLift: Real-Time ETL for Air Quality Data

Dynamic AirLift is an end-to-end solution for extracting, transforming, and analyzing real-time air quality data. This project leverages OpenWeatherMap's API to fetch air pollution data for New York City and provides insights through interactive visualizations and analysis.

## Features

- **Real-Time Data Extraction**: Fetches air quality data for the past 10 hours dynamically.
- **Data Transformation and Storage**: Converts raw data into structured formats (CSV and Excel).
- **Visualizations**:
  - Bar charts of pollutant levels.
  - Correlation heatmaps to identify relationships between pollutants.
  - Interactive time-series analysis of air quality trends.
  - Pollutant threshold analysis with visual alerts for critical levels.
- **Combined Pollutant Graphs**: Displays trends for multiple pollutants simultaneously.

## Requirements

- Python 3.8 or higher
- Libraries:
  - `requests`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `plotly`
  - `openpyxl`

Install the required libraries with:
```bash
pip install -r requirements.txt
