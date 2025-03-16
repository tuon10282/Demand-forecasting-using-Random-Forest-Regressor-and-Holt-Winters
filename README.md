**Demand Forecasting Using Random Forest Regressor and Holt-Winters**

**1. Overview**
To tackle inventory management challenges, this study applies Holt-Winters and Random Forest for demand forecasting. Holt-Winters, a time series method, captures trends and seasonality using exponentially weighted smoothing. Random Forest, a machine learning algorithm, leverages multiple decision trees to model non-linear relationships.

**2. Dataset Selection and Preprocessing**
This study utilizes the "Retail Store Inventory Forecasting in the United States" dataset from Kaggle, covering January 2022 to January 2024. A five-step preprocessing approach ensures data quality:
- Data Cleaning – Handling missing values and verifying completeness.
- Data Reduction – Aggregating daily orders into monthly totals.
- Feature Engineering – Incorporating historical sales trends and lag variables.
- Data Splitting – Using 80% for training (Jan 2022–Jul 2023) and 20% for testing (Aug 2023–Dec 2023).
  
**3. Model Construction**
  
**Holt-Winters Exponential Smoothing**: Models trend and seasonality with exponentially decreasing weights.
The Multiplicative Model was selected after evaluating variance stability.
Optimized smoothing parameters:
- Alpha (α): 0.0050
- Beta (β): 0.0001
- Gamma (γ): 0.0001
**Random Forest Regressor**: Utilizes lag variables (1-month, 2-month, and 3-month sales) and dummy variables for months.
**Evaluation Metrics**: To ensure an objective assessment, the study employs:
- Mean Absolute Percentage Error (MAPE) – Measures percentage deviation from actual values.
- Root Mean Squared Error (RMSE) – Measures the absolute error in original units.
  
**4. Results & Comparison**

While Holt-Winters remains useful for structured seasonal data, Random Forest provides superior accuracy and adaptability in handling real-world demand fluctuations. The results demonstrate that machine learning methods outperform traditional time series models when external influencing factors are involved.

