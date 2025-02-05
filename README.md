# Forecasting U-3 Labor Underutilization Rate 📊

## Project Overview
This project aims to predict the **U-3 Labor Underutilization Rate for December 2024**, providing insights for policymakers and economists. The analysis leverages **statistical modeling, time series forecasting, and machine learning techniques** to model unemployment trends based on labor market indicators.

## Problem Statement
The U-3 Labor Underutilization Rate is a key economic indicator representing the percentage of unemployed individuals within the civilian labor force. Accurate forecasting of this metric is crucial for:
- **Policymakers** to make informed economic decisions
- **Businesses** to plan workforce strategies
- **Investors** to assess labor market conditions

This project aims to build a **predictive model** for the **U-3 unemployment rate** using historical labor statistics and external economic indicators.

## 🔑 Key Objectives
- Analyze historical labor market trends from **January 2022 – September 2024**
- Identify the most influential variables impacting the U-3 rate
- Develop a robust predictive model using **Gamma Regression**
- Utilize **ARIMA models** to forecast economic indicators for missing months
- Validate model performance through cross-validation and statistical diagnostics

## 📊 Data Analyzed
**Primary Dataset:**
- Bureau of Labor Statistics (BLS) data covering **employment and labor force metrics**

**Key Variables:**
- **Labor Market Indicators:**
  - AWU (Average Weeks Unemployed)
  - CLF (Civilian Labor Force)
  - EPR (Employment-Population Ratio)
  - LFPR (Civilian Labor Force Participation Rate)
  - TNE (Total Nonfarm Employment)
  - U3 (U-3 Unemployment Rate, Target Variable)
- **Economic Indicators:**
  - UA (All Items CPI)
  - UFH (Food at Home CPI)
  - UG (Gasoline Prices)
  - USH (Housing Costs)
  - USM (Medical Care Costs)
  - UST (Transportation Costs)

## 📊 Data Processing & Model Development

### 1. **Exploratory Data Analysis (EDA)**
- Evaluated trends in unemployment and economic indicators
- Applied **log transformation** to smooth irregular features (e.g., gasoline prices)
- Conducted **multicollinearity tests** (Variance Inflation Factor - VIF) to remove highly correlated variables

### 2. **Model Selection & Training**
- Trained multiple regression models:
  - **Linear Regression**
  - **Gamma Regression** ✅ (Chosen due to lowest AIC score)
  - **Poisson, Tweedie, and Negative Binomial Models** (Benchmark comparisons)
- Selected **Gamma Regression** based on superior **Akaike Information Criterion (AIC)** and **Mean Squared Error (MSE)**

### 3. **Time Series Forecasting**
- Used **ARIMA models** to forecast missing values for key economic indicators (EPR, UG, USM)
- Implemented **5-Fold Cross-Validation** for model robustness
- Evaluated residuals to ensure unbiased predictions

## 📈 Key Findings
- **Gamma Regression** provided the best predictive performance for U-3 unemployment rate
- **Employment-Population Ratio (EPR)** and **Medical Costs (USM)** were significant predictors
- **Historical U-3 rates (U3_lag1)** played a crucial role in forecasting
- **Predicted U-3 rate for December 2024: 4.17% (± 0.12%)**

## 💡 Skills Demonstrated
- Time Series Analysis & Forecasting (ARIMA)
- Statistical Modeling & Regression Analysis
- Feature Engineering & Multicollinearity Reduction
- Data Cleaning & Standardization
- Python Programming for Economic Data Analysis

## 🎯 Methodology
1. **Data Preprocessing & Standardization**
   - Scaled numerical features using **StandardScaler**
   - Addressed multicollinearity with **VIF-based feature selection**
2. **Exploratory Data Analysis**
   - Visualized unemployment trends & economic correlations
   - Applied transformations to improve model interpretability
3. **Model Training & Evaluation**
   - Selected **Gamma Regression** based on lowest **AIC** and **MSE**
   - Validated using **5-Fold Cross-Validation**
4. **Forecasting Future U-3 Rates**
   - Predicted missing economic indicators using **ARIMA**
   - Forecasted U-3 Unemployment Rate for December 2024

## 🌟 Research Contributions
- Developed a **robust economic forecasting model** for unemployment prediction
- Demonstrated **ARIMA-driven forecasting** for economic variables
- Provided insights into **labor market trends & economic policy implications**

## 🎓 Learning Outcomes
- Hands-on experience with **econometric modeling & forecasting**
- Understanding of **labor market dynamics** through statistical analysis
- Practical application of **Python’s statsmodels & machine learning libraries**

## 🚀 Future Enhancements
- Extend forecasting model to incorporate **macro-economic shocks**
- Experiment with **deep learning-based time series models** (LSTMs, Transformers)
- Improve model interpretability with **Shapley values for feature importance**

