# **Dynamic AirLift: Real-Time ETL for Air Quality Data**

**Dynamic AirLift** is an end-to-end Python project that extracts, transforms, and analyzes real-time air pollution data. This project focuses on air quality in **New York City** (NYC) using OpenWeatherMap's API, providing actionable insights through visualizations.

---

## **Project Overview**

This project operates as a robust **ETL pipeline**:

1. **Extract**: Fetches real-time air quality data using OpenWeatherMap's API.
2. **Transform**:
   - Normalizes raw JSON responses into clean, structured formats.
   - Converts timestamps into **Eastern Time** for readability.
   - Computes derived values, such as CO in µg/m³.
3. **Load**: Saves transformed data into **CSV** and **Excel** files for persistence.
4. **Analyze**: Generates visualizations to identify air quality trends and correlations.

---

## **Features**

###  **Real-Time Data Extraction**
- Dynamically fetches air quality data for the **last 10 hours**.
- Pollutants included:
   - **PM2.5**: Fine particulate matter
   - **PM10**: Coarse particulate matter
   - **NO₂**: Nitrogen dioxide
   - **O₃**: Ozone
   - **SO₂**: Sulfur dioxide
   - **CO**: Carbon monoxide
   - **NH₃**: Ammonia

---

###  **Data Transformation and Storage**
- Converts raw API responses into clean **DataFrames**.
- Removes timezone offsets for easier analysis.
- Saves structured data as:
   - `air_quality_data_last_10_hours.csv`
   - `air_quality_data_last_10_hours.xlsx`

---

###  **Visualizations**

#### 1. **Last-Hour Pollutant Levels**  
A bar chart highlights pollutant concentrations in the most recent hour.

#### 2. **Correlation Heatmap**  
Displays correlations between pollutants using **Seaborn**.

#### 3. **Time-Series Trends**  
Interactive line graphs (via **Plotly**) visualize pollutant levels over time.

#### 4. **Threshold Analysis**  
Line charts compare pollutant levels against predefined thresholds (Good, Moderate, Unhealthy).

#### 5. **Combined Pollutant Visualization**  
A time-series graph shows trends for multiple pollutants, including derived CO levels.

---

## **Code Workflow**

The script is modular and divided into key sections:

1. **Data Extraction**  
   Fetches hourly air pollution data using OpenWeatherMap's API.

2. **Save Data**  
   Stores clean data into CSV and Excel files.

3. **Visualizations**  
   - Pollutant bar charts (last hour).  
   - Correlation heatmaps.  
   - Interactive time-series graphs.  
   - Threshold comparisons.  
   - Combined pollutant trends.

---

## **Installation**

### Prerequisites
- **Python 3.8+**
- OpenWeatherMap API Key (sign up [here](https://openweathermap.org/api)).

### Required Libraries
Install dependencies with pip:

```bash
pip install requests pandas matplotlib seaborn plotly openpyxl pytz
