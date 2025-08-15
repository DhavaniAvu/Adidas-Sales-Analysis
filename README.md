# 🏷️ Adidas US Sales Analysis & Inventory Control Analysis 📊

## 📌 Overview
This project is a comprehensive data analysis and forecasting study using Adidas US retail sales data. It combines data cleaning, exploratory analysis, profit efficiency measurement, and advanced time series forecasting models including ARIMA and SARIMAX.

The objective is to understand sales patterns across geography, product, and channel — and then use historical trends to predict future operating profits.

---

## 🎯 Goals
- Identify high-performing regions and product lines
- Evaluate seasonality in sales trends
- Compare retailer strategies and margins
- Predict future sales using time series techniques

---

## 📁 Files Included

| File                     | Description                                                |
|--------------------------|------------------------------------------------------------|
| `adidas sales.ipynb`     | Jupyter Notebook with full pipeline and model implementations |
| `Addidas dashboard.pbix` | Power BI dashboard file visualizing sales KPIs             |
| `Addidas dashboard.twbx` | Tableau dashboard file visualizing sales KPIs              |
| `Adidas US Sales Datasets.csv` | The dataset used for this analysis                        |

---

## 🧪 Technologies Used

- **Languages**: Python
- **Libraries**: pandas, numpy, seaborn, matplotlib, statsmodels, pmdarima
- **ML Models**: ARIMA, SARIMAX, Auto ARIMA, Linear Regression, Logistic Regression
- **BI Tools**: Power BI, Tableau
- **Notebook Interface**: Jupyter

---

## 🧼 Data Cleaning & Preprocessing

- Removed NA/null values
- Removed `$`, `%`, and `,` from monetary fields and converted to float
- Converted `Invoice Date` to datetime format
- Aggregated records to **weekly profit trends** using `resample('W')`
- Extracted Gender and Product Type from item names
- Dropped unused fields like `Retailer ID`
- Created dummy variables for `Product`, `Retailer`, `Region`, and more
- Engineered new metric: `Sales Efficiency = Total Sales / Frequency`

---

## 🔍 Exploratory Data Analysis (EDA)

### 📊 Key KPIs & Business Insights

- **Top Regions**: Southeast and New York led in overall profit and efficiency
- **Product Trends**: Men’s products consistently outsold women’s across categories
- **Retail Channels**: In-store Retailers were more efficient despite growing online sales

### 📈 Visualizations Used

- Histograms for disrtibutions and skewness checks 
- Boxplots for outlier detection in Profit and Sales
- Bar plots for comparisons by Region, State, City
- Correlation heatmaps to identify key drivers of operating profit
- Weekly time series plots to visualize sales trend seasonality

---

## 📉 Time Series Forecasting

### ➤ Objective
Forecast Operating Profit using statistical and machine learning models.

### ⚙️ Stationarity & Transformation

- Conducted Augmented Dickey-Fuller (ADF) test — confirmed **non-stationarity**
- Applied **Box-Cox**, log, and square root transformations (Box-Cox yielded best results)
- Seasonal decomposition into **trend, seasonality, and residual**
- Detected significant **weekly seasonality** via ACF and PACF

### 🧠 Models Used

| Model             | Description |
|------------------|-------------|
| ARIMA(2,3,2)      | Manual tuning after differencing |
| Auto ARIMA        | Automatically optimized `p,d,q` values |
| SARIMAX           | ARIMA with seasonal and exogenous regressors |
| Linear Regression | Baseline with encoded features |
| Logistic Regression | For comparison and classification-type scenarios |

---

## 📊 Model Evaluation & Metrics

- Evaluated using **MAE**, **MSE**, and **R²**
- Used **TimeSeriesSplit (5-fold CV)** to validate consistency
- SARIMAX consistently outperformed other models in cross-validation

---

## 📈 ACF & PACF Interpretation

- **ACF** identifies moving average (MA) components (q)
- **PACF** identifies autoregressive (AR) components (p)
- Both were used to optimize ARIMA and SARIMAX parameters

---

## 🔮 Forecast Visualization

- Plotted **forecast vs. original** values with confidence intervals
- Included **fitted value overlays** to inspect residual patterns
- Forecast curve closely tracks historical trends with minor variance

---

## 🔍 Residual Analysis

- Residuals from SARIMAX model showed **no autocorrelation** and **random scatter**, indicating a good fit
- Residual plots helped validate model assumptions post-prediction

---

## 📌 Strategic Business Insights

- Focus expansion in **high-efficiency cities**: New York, Miami, Nashville
- Despite rising online sales, **Retail stores outperformed** — improve in-store experience and marketing
- Specialty retailers performed well — consider **exclusive product launches**
- Use time series models to **automate inventory planning**, marketing timing, and promotions

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
