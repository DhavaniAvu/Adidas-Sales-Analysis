# 🏷️ Adidas US Sales Analysis & Forecasting

## 📌 Project Description

Explore the dynamic landscape of Adidas sales from 2021 to 2022 through a comprehensive sales analysis. This analysis assists Adidas in dissecting critical factors influencing sales, such as **retailer performance**, **gender-based insights**, and **regional variations**. Each visual is crafted to clearly highlight trends across diverse business dimensions.

---

## 🧾 About the Dataset

- **Source:** [Kaggle – Adidas Sales Dataset](https://www.kaggle.com/datasets/heemalichaudhari/adidas-sales-dataset?resource=download)
- **Contents:** The dataset includes:
  - Product types
  - Sales revenue
  - Units sold
  - Operating profit & margin
  - Sales locations (region/state/city)
  - Retailer & sales method
  - Time-series information (invoice dates)

The dataset supports:
- Sales trend analysis
- Market performance comparisons
- Strategy formulation for future campaigns
- Channel evaluation (retail vs online)

---

## 📚 Project Overview

This project aims to **analyze, visualize, and forecast** Adidas' U.S. sales performance. Using Python and Power BI, we derive business intelligence from structured sales records.

### 🎯 Goals

- Identify high-performing regions and product lines
- Evaluate seasonality in sales trends
- Compare retailer strategies and margins
- Predict future sales using time series techniques

---

## ❓ Research Questions

- 📈 What are the overall sales trends of Adidas products over time?
- 🏷️ Which product categories and regions contribute most to revenue?
- ⏳ How do sales vary across months and seasons?
- 🔮 What factors influence performance, and how can we forecast future sales?

---

## 🧹 Data Cleaning & Preprocessing

- **Data Import:** Loaded data using pandas and validated schema
- **Missing Values:** Checked for NA/nulls and treated them appropriately
- **Monetary Formatting:** Cleaned dollar signs and commas for numeric conversion
- **Datetime Handling:** Parsed `Invoice Date` to datetime format
- **Feature Engineering:** Extracted gender, encoded categories (e.g., one-hot encoding)
- **Outlier Inspection:** Used boxplots to assess outliers while retaining business-relevant extremes

---

## 🔍 Exploratory Data Analysis (EDA)

### 📊 Descriptive Statistics

- Mean, median, standard deviation, and frequency computed
- Insights generated for each categorical dimension (region, state, city, retailer, product)

### 📈 Visualizations

- Line plots for time-series sales
- Bar charts for regional & product sales
- Box plots for price and profit variance
- Correlation matrix to study profit-driving features

---

## 🔬 Time Series Analysis

- **Decomposition:** Split sales into trend, seasonal, and residual components
- **Moving Averages:** Smoothed fluctuations to reveal overall direction
- **Stationarity Check:** Applied Augmented Dickey-Fuller (ADF) test
- **ARIMA Modeling:** Tuned ARIMA(p,d,q) to best fit historical sales
- **Forecasting:** Predicted future trends with confidence intervals

---

## 💡 Key Findings & Insights

- 📌 **Top Regions & Retailers:** Southeast region and Walmart exhibited highest sales efficiency
- 🛍️ **Product Category Leaders:** Men’s footwear and specific seasonal products dominated
- ❄️ **Seasonal Peaks:** Spikes observed during summer and holiday periods
- 📉 **Low Efficiency Areas:** Some states and cities underperformed, signaling growth opportunities
- 🔮 **Forecast Accuracy:** ARIMA model delivered reliable short-term sales forecasts

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `AdidasSalesAnalysis_TimeSeries.py` | Python script with EDA and forecasting code |
| `AdidasSalesAnalysis_TimeSeries.html` | Exported notebook view with visuals |
| `adidas sales.ipynb` | Jupyter Notebook version of detailed analysis |
| `Addidas dashboard.pbix` | Power BI dashboard (regional heatmaps, KPIs, filters) |
| `adidasSales.html` | Clean HTML report for project showcasing |

---

## 🧪 Tools & Technologies

- **Python Libraries**: `pandas`, `numpy`, `seaborn`, `matplotlib`, `statsmodels`
- **Time Series Modeling**: ADF Test, ARIMA
- **Visualization**: Matplotlib, Seaborn, Power BI
- **Notebook Platforms**: JupyterLab, VS Code

---

## 📎 Folder Structure

