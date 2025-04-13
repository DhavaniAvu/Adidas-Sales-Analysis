# 🏷️ Adidas US Sales Analysis & Time Series Forecasting 📊

## 📌 Overview

This project is a comprehensive **data analysis and forecasting study** using Adidas US retail sales data. It combines **data cleaning**, **exploratory analysis**, **profit efficiency measurement**, and **advanced time series forecasting models** including **ARIMA** and **SARIMAX**.

The objective is to understand sales patterns across geography, product, and channel — and then use historical trends to **predict future operating profits**.

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

## 📁 Files Included

| File | Description |
|------|-------------|
| `AdidasSalesAnalysis_TimeSeries.py` | Main Python script for data cleaning, analysis, and time series modeling |
| `AdidasSalesAnalysis.ipynb` / `adidas sales.ipynb` | Jupyter Notebooks with full EDA and modeling |
| `Addidas dashboard.pbix` | Power BI dashboard file visualizing sales KPIs |
| `adidasSales.html` / `AdidasSalesAnalysis_TimeSeries.html` | HTML exports of notebooks for browser viewing |

---

## 🧪 Technologies Used

- **Languages**: Python
- **Libraries**: pandas, numpy, seaborn, matplotlib, statsmodels, pmdarima
- **ML Models**: ARIMA, SARIMAX, Auto ARIMA, Linear Regression
- **BI Tool**: Power BI
- **Notebook Interface**: Jupyter

---

## 🧼 Data Cleaning & Preprocessing

- Removed `$`, `%`, and `,` from monetary values and converted to `float`
- Converted `Invoice Date` to datetime type
- Extracted `Gender` from product names
- Dropped unused columns like `Retailer ID`
- Created dummies for categorical columns (`Product`, `Retailer`, `Region`, etc.)
- Created new metrics like `Sales Efficiency = Total Sales / Frequency`

---

## 🔍 Exploratory Data Analysis (EDA)

### 📊 KPIs & Comparisons

- **Top Regions**: Southeast had the highest sales efficiency
- **Best Retailer**: Walmart was top in both sales volume and efficiency
- **Product Trends**: Men’s categories outsold Women’s
- **Online vs Retail**: Retail was more efficient despite online growth

### 📈 Visualizations

- Boxplots for outlier detection
- Bar plots for region/state/city performance
- Correlation matrix to identify profit drivers
- Time series plot of weekly aggregated profit

---

## 📉 Time Series Modeling

### ➤ Goal: Forecast Operating Profit

### ⚙️ Stationarity & Transformation

- Conducted **Augmented Dickey-Fuller (ADF)** test (non-stationary)
- Applied **Box-Cox** and **log/square root** transformations
- Performed **seasonal decomposition** (trend, seasonal, residual)
- Detected seasonality using **ACF/PACF** plots

### 🧠 Models Used

| Model | Description |
|-------|-------------|
| `ARIMA(2,3,2)` | Manually tuned model after differencing |
| `Auto ARIMA` | Automatically selected parameters (p,d,q) |
| `SARIMAX` | Seasonal ARIMA with external regressors |
| `Linear Regression` | As baseline comparison with encoded features |

---

## 🧪 Model Evaluation & Metrics

| Metric | Model 1 | Model 2 (Better) |
|--------|---------|------------------|
| MAE    | 0.214   | **0.193**        |
| MSE    | 0.114   | **0.098**        |
| R²     | -14.39  | **-9.35**        |

- Used **TimeSeriesSplit (5-fold)** cross-validation
- Computed evaluation metrics on each fold
- **Second model (SARIMAX/Auto ARIMA)** consistently outperformed

> Note: Negative R² values in some folds suggest more improvement is needed. External factors and holidays could be modeled better in future versions.

---

## 🧠 Interpretation of ACF & PACF

- **ACF** helps identify the **MA (q)** term
- **PACF** helps identify the **AR (p)** term
- Used both plots to tune ARIMA and SARIMAX models effectively

---

## 📉 Forecast Visualization

- Plotted forecast vs. original values with confidence intervals
- Forecast curve closely tracks actual profit trend
- Used `fittedvalues` overlay to inspect residual patterns

---

## 📌 Strategic Business Insights

- Focus on **high-efficiency states/cities** like New York, Miami, Nashville
- **Retail stores** outperform online in many metrics — enhance in-store UX
- Expand product lines that perform well in **specialty retailers**
- Use models to plan **inventory, marketing, and discounting strategies**

---

## 🧑‍💻 Author

**Dhavani Avu**  
🎓 Master’s in Data Analytics Engineering – George Mason University  
📫 Email: [dhavaniavu08@gmail.com](mailto:dhavaniavu08@gmail.com)  

---

## 🙌 Acknowledgements

- Dataset simulated for academic research
- Special thanks to professors and peers who reviewed early drafts
- Inspired by real-world business forecasting use cases

---
