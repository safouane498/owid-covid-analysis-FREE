# OWID COVID-19 Analysis

This project explores the evolution of the COVID-19 pandemic using data from **Our World in Data (OWID)**.

It combines exploratory data analysis, global trend visualization, geographic mapping, and time-series forecasting to study the progression of reported COVID-19 cases and deaths across countries.

The public version focuses on clear visual exploration and a simple forecasting example. More in-depth statistical, mathematical, and time-series analysis is available separately in the private repository.

---

## 🚀 Features

- Cleaning and preparation of OWID COVID-19 data
- Analysis of global COVID-19 cases and deaths
- Visualization of smoothed daily cases and deaths over time
- Country-level and worldwide trend analysis
- Geographic visualization of cumulative cases per million
- Geographic visualization of cumulative deaths per million
- Animated world maps showing the evolution of:
  - new cases per million
  - new deaths per million
- Time-series forecasting of COVID-19 cases
- SARIMA-based forecasting for France
- 365-day forecast horizon
- 95% forecast confidence intervals

---

## 🌍 Geographic Analysis

The project uses interactive choropleth maps to visualize the geographic distribution of COVID-19 indicators across the world.

The available maps include:

- Cumulative COVID-19 cases per million inhabitants
- Cumulative COVID-19 deaths per million inhabitants
- Animated evolution of new cases per million
- Animated evolution of new deaths per million

These visualizations make it possible to compare the progression of the pandemic across countries and observe how its geographic distribution changed over time.

---

## 📈 Global Pandemic Evolution

Daily COVID-19 observations are aggregated to study worldwide trends.

Smoothed indicators are used to reduce short-term fluctuations and make the main pandemic waves easier to identify.

The analysis includes:

- Global evolution of new COVID-19 cases
- Global evolution of new COVID-19 deaths
- Identification of major waves and peaks
- Visualization of long-term pandemic dynamics

The dataset used in this analysis covers the period from **February 2020 to October 2022**.

---

## 🔮 Time-Series Forecasting

The project also contains a forecasting example based on a **Seasonal ARIMA (SARIMA)** model.

For France, the model analyzes the smoothed number of new COVID-19 cases using:

```text
SARIMA(2,1,2) × (1,1,1,7)
```

The seasonal period of **7 days** is used to represent weekly patterns in the reported data.

The model produces:

- Historical time-series visualization
- 365-day forecast
- Expected future number of smoothed cases
- 95% confidence intervals around the forecasts

This forecasting component is intended as a simple introduction to statistical time-series modeling rather than a complete epidemiological forecasting system.

---

## 🧠 Analysis Workflow

1. **Data Loading** — COVID-19 data is imported using Pandas.
2. **Data Cleaning** — Unnecessary mobility variables are removed and dates are standardized.
3. **Global Aggregation** — Cases and deaths are aggregated by date.
4. **Trend Analysis** — Smoothed indicators are visualized to study pandemic waves.
5. **Geographic Analysis** — Plotly choropleth maps are generated for country-level comparisons.
6. **Animated Mapping** — The geographical evolution of cases and deaths is visualized over time.
7. **Country Selection** — France is selected for the forecasting example.
8. **SARIMA Modeling** — A seasonal time-series model is fitted to smoothed new cases.
9. **Forecast Generation** — Future values and 95% confidence intervals are generated.

---

## 🛠️ Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Plotly
- Statsmodels
- SARIMA / SARIMAX
- Jupyter Notebook

---

## 📊 Dataset

The project is based on COVID-19 data from **Our World in Data (OWID)**.

The analysis uses variables such as:

```text
total_cases
new_cases
new_cases_smoothed
total_deaths
new_deaths
new_deaths_smoothed
total_cases_per_million
new_cases_per_million
total_deaths_per_million
new_deaths_per_million
population
population_density
life_expectancy
diabetes_prevalence
```

Official OWID COVID-19 data repository:

https://github.com/owid/covid-19-data

---

## 🔒 Extended Analysis

This public repository is intended for **commercial presentation and demonstration** of the project.

A separate private version contains more in-depth work, including additional:

- Statistical analysis
- Mathematical analysis
- Time-series modeling
- Forecast evaluation
- Model diagnostics
- Advanced forecasting experiments

The private repository contains the **extended version** of the project.

---

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/safouane498/owid-covid-analysis.git

# Move into the project directory
cd owid-covid-analysis

# Install the dependencies
pip install -r requirements.txt
```

Then launch Jupyter Notebook:

```bash
jupyter notebook
```

---

## 📌 Disclaimer

This project is intended for **data analysis, visualization, demonstration, and educational purposes**.

The statistical forecasts should not be interpreted as medical or epidemiological predictions.
