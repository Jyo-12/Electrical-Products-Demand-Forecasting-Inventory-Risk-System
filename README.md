# Electrical-Products-Demand-Forecasting-Inventory-Risk-System
🧠 Problem Statement

A large electrical goods supplier faces frequent stockouts of fast-moving items and overstock of slow-moving SKUs. The objective is to build a demand forecasting model and translate predictions into actionable inventory decisions.

🎯 Objectives:

Forecast monthly demand for each SKU–Region–Channel combination
Capture seasonality, promotions, and demand variability
Optimize inventory planning using reorder points and safety stock

📊 Dataset:

The dataset includes:

Historical monthly sales (units_sold)
Product attributes (category, lead time, cost)
Business signals (price, promotion, project spikes, supply disruption)

⚙️ Approach:

🔹 Feature Engineering:

Time-based features: month, year, quarter
Lag features: previous 1–3 months demand
Rolling statistics: mean and standard deviation
Encoded categorical variables

🔹 Modeling:

Used LightGBM Regressor for demand prediction
Incorporated temporal dependencies using lag features

🔹 Forecast Enhancement:

Initialized test lag features using latest training observations
Captured recent trends for improved predictions

📦 Inventory Optimization:

Reorder Point = Forecasted Demand × Lead Time
Safety Stock = z × Demand Variability
Generated actionable recommendations for inventory planning

📈 Evaluation:

Metrics: SMAPE and RMSE
Achieved Top 4 rank on leaderboard 🏆

💡 Key Insights:

Demand exhibits strong temporal dependency and seasonality
Promotions and project spikes significantly impact demand
Lag-based features greatly improve forecasting accuracy.

🛠️ Tech Stack:

Python (Pandas, NumPy)
Scikit-learn
LightGBM
Matplotlib

🚀 Outcome:

Developed an end-to-end forecasting and inventory decision system combining machine learning with business logic, achieving high predictive accuracy and actionable insights.
