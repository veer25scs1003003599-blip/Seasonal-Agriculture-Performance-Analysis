# 🌾 Seasonal Agriculture Performance Analysis

A data analytics project exploring how **agricultural performance varies across seasons** — analyzing 4,000 farm-level records across 8 Indian states to uncover seasonal patterns in yield, water efficiency, and profitability, using **Google Colab, Pandas, NumPy, Matplotlib, and Seaborn**.

<p align="left">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white">
  <img alt="Pandas" src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white">
  <img alt="NumPy" src="https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?logo=numpy&logoColor=white">
  <img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-Visualization-11557C">
  <img alt="Seaborn" src="https://img.shields.io/badge/Seaborn-Statistical%20Viz-4C72B0">
  <img alt="Colab" src="https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?logo=googlecolab&logoColor=white">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-green">
</p>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/veer25scs1003003599-blip/Seasonal-Agriculture-Performance-Analysis/blob/main/Seasonal_Agriculture_Performance_Data_Analytics.ipynb)

---

## 📌 Problem Statement

Agricultural activities are influenced by seasonal variations in environmental conditions, farming practices, resource availability, and economic conditions — as a result, agricultural performance can differ significantly from one season to another.

This project analyzes a seasonal agriculture dataset to identify meaningful **patterns, trends, relationships, and variations** in performance across seasons, and to turn those findings into evidence-based recommendations.

> This is a pure **data analytics** project — exploratory analysis and visualization only, no machine learning modeling or dashboard development.

## 🎯 Project Objectives

- Understand the structure and quality of the agricultural dataset
- Clean and prepare the data for analysis
- Explore seasonal patterns across environmental and economic variables
- Compare agricultural performance across seasons
- Investigate relationships among key variables (yield, water use, profit, etc.)
- Apply univariate, bivariate, and multivariate visualization techniques
- Derive evidence-based insights and recommendations

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| [Google Colab](https://colab.research.google.com/) | Notebook environment for running the analysis |
| [Pandas](https://pandas.pydata.org/) | Data loading, cleaning, and manipulation |
| [NumPy](https://numpy.org/) | Numerical operations |
| [Matplotlib](https://matplotlib.org/) | Core plotting and charting |
| [Seaborn](https://seaborn.pydata.org/) | Statistical data visualization |

## 📊 Dataset

**File:** [`seasonal_agriculture_performance_dataset.csv`](./seasonal_agriculture_performance_dataset.csv)
**Size:** 4,000 farm-level records × 28 columns

The dataset contains farm-level agricultural records covering seasons, locations, environmental conditions, farming practices, production costs, revenues, profits, and resource usage.

| Category | Details |
|---|---|
| **Seasons** | Kharif, Rabi, Zaid |
| **Crops** | Chilli, Cotton, Groundnut, Maize, Pulses, Rice, Sugarcane, Wheat |
| **States** | Andhra Pradesh, Gujarat, Karnataka, Madhya Pradesh, Maharashtra, Punjab, Tamil Nadu, Telangana |
| **Irrigation methods** | Drip, Flood, Rainfed, Sprinkler |

<details>
<summary><b>Full column reference</b></summary>

| Column | Description |
|---|---|
| `Farm_ID` | Unique identifier for each farm record |
| `State`, `District` | Location of the farm |
| `Crop` | Crop grown |
| `Season` | Growing season (Kharif / Rabi / Zaid) |
| `Farm_Area_Hectares` | Total cultivated area |
| `Rainfall_mm` | Rainfall received during the season |
| `Avg_Temperature_C` | Average temperature |
| `Humidity_pct` | Average relative humidity |
| `Sunlight_Hours_Day` | Average daily sunlight hours |
| `Soil_pH` | Soil pH level |
| `Soil_Moisture_pct` | Soil moisture percentage |
| `Nitrogen_kg_ha`, `Phosphorus_kg_ha`, `Potassium_kg_ha` | Soil nutrient levels (NPK) |
| `Irrigation_Method` | Irrigation technique used |
| `Fertilizer_kg_ha` | Fertilizer applied per hectare |
| `Pesticide_Litre_ha` | Pesticide applied per hectare |
| `Seed_Quality_Score` | Seed quality rating |
| `Yield_Tonnes_Ha` | Crop yield per hectare |
| `Production_Tonnes` | Total production volume |
| `Market_Price_INR_Tonne` | Market price per tonne (INR) |
| `Total_Cost_INR`, `Revenue_INR`, `Profit_INR` | Financial performance (INR) |
| `Water_Used_m3` | Total water consumption |
| `Water_Efficiency_t_per_1000m3` | Yield per 1000m³ of water used |
| `Disease_Pest_Risk_pct` | Disease/pest risk score |

</details>

## 🔬 Analysis Workflow

The notebook follows a complete EDA pipeline:

1. **Data Understanding** — shape, structure, data types, sample records
2. **Data Quality & Cleaning** — missing value detection and group-wise (season-based) median imputation for `Rainfall_mm`, `Soil_Moisture_pct`, and `Yield_Tonnes_Ha`; duplicate checks
3. **Descriptive Statistics** — mean, median, std, IQR across numerical features, and seasonal KPI summaries
4. **Univariate Analysis** — distribution plots, histograms with KDE, count plots, pie charts
5. **Outlier Analysis** — IQR-based outlier detection across all numeric columns
6. **Bivariate Analysis** — boxplots and scatter plots (e.g., water usage by season, yield vs. rainfall)
7. **Multivariate Analysis** — pairplots and a full correlation heatmap across environmental and performance variables
8. **Key Findings & Recommendations** — insights translated into actionable, evidence-based recommendations

## 📈 Key Findings

1. **Seasonal yield & production disparities** — Yield varies significantly by season: **Kharif** drives the highest total production due to abundant rainfall (>600 mm on average), while **Rabi** shows superior water efficiency and crop stability, especially for wheat and pulses.
2. **Resource consumption & water efficiency** — **Zaid** (summer) season demands the highest irrigation volume per hectare due to low rainfall and high temperatures (>30°C). Drip irrigation shows notably higher water efficiency than flood irrigation.
3. **Economic & profitability patterns** — Production costs peak in high-input seasons, but profit is heavily constrained by market price fluctuations and fertilizer/pesticide spend. Higher pest/disease risk scores correlate with higher input costs and lower margins.

## ✅ Evidence-Based Recommendations

1. **Precision water management** — shift Zaid and Rabi crops from flood to drip/micro-irrigation to cut water usage and reduce thermal stress.
2. **Seasonal crop selection strategy** — align high-water-demand crops (e.g., Sugarcane, Rice) with high-rainfall Kharif periods to optimize yield and lower cost per ton.
3. **Integrated Pest Management (IPM)** — proactive pest-risk monitoring during humid transitional weather to reduce pesticide use and improve profitability.

## ⚠️ Limitations

- **No time-series continuity** — the dataset is cross-sectional, not multi-year sequential farm tracking.
- **Uncaptured macroeconomic factors** — regional supply-demand shocks, fuel price changes, and state subsidies are not included.

## 🚀 Getting Started

### Option 1: Run in Google Colab (recommended)

Click the badge above, or open directly:
[Seasonal_Agriculture_Performance_Data_Analytics.ipynb](https://colab.research.google.com/github/veer25scs1003003599-blip/Seasonal-Agriculture-Performance-Analysis/blob/main/Seasonal_Agriculture_Performance_Data_Analytics.ipynb)

The notebook prompts you to upload `seasonal_agriculture_performance_dataset.csv` directly — no extra setup needed.

### Option 2: Run locally

```bash
# 1. Clone the repository
git clone https://github.com/veer25scs1003003599-blip/Seasonal-Agriculture-Performance-Analysis.git
cd Seasonal-Agriculture-Performance-Analysis

# 2. (Optional) Create a virtual environment
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 4. Launch the notebook
jupyter notebook Seasonal_Agriculture_Performance_Data_Analytics.ipynb
```

> Note: the notebook uses `google.colab.files.upload()` to load the CSV — if running locally, replace that cell with `df = pd.read_csv('seasonal_agriculture_performance_dataset.csv')`.

## 🗺️ Roadmap

- [ ] Add exported chart images to a `visuals/` folder for quick preview in this README
- [ ] Extend analysis with multi-year time-series data
- [ ] Incorporate macroeconomic and subsidy data
- [ ] Explore predictive modeling on top of the EDA

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the [MIT License](LICENSE). *(Add a `LICENSE` file to the repo if one doesn't exist yet.)*

## 👤 Author

**Veer** — [@veer25scs1003003599-blip](https://github.com/veer25scs1003003599-blip)

---

<p align="center"><i>If you found this project useful, consider giving it a ⭐!</i></p>
