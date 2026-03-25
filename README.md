# smart-home-energy-management
📌 Overview
As smart homes become increasingly common, the demand for smart energy management systems has grown significantly. These systems leverage IoT sensors and connected appliances to monitor and optimize energy use. By forecasting short-term consumption trends, homeowners and energy providers can make informed decisions that reduce costs, improve efficiency, and support sustainability.
This project develops a predictive model for estimating short-term energy usage based on environmental data and appliance activity. It combines ensemble learning (Random Forest Regressor) with explainable AI (SHAP) to provide accurate forecasts and transparent insights into the factors influencing energy consumption.

⚡ Key Features
- IoT Sensor Data: Time-stamped measurements of temperature, humidity, pressure, wind speed, and appliance activity.
- Time Series Preprocessing: Sliding window technique to preserve temporal relationships.
- Feature Engineering: Lag features, time-based inputs (hour, day, season), and polynomial features to capture nonlinear patterns.
- Model Development: Random Forest Regressor trained with time-aware splits to maintain chronological order.
- Model Interpretability: SHAP analysis to identify the most impactful features on energy consumption.
- Use Case: Real-time monitoring and adaptive control strategies for smart homes.

🛠 Methodology
1. Data Collection
- IoT sensors record environmental conditions and appliance-level energy usage.
- Data is highly time-sensitive, making it suitable for short-term forecasting.
2. Data Cleaning
- Removal of duplicate timestamps.
- Filtering out invalid values (e.g., negative energy usage).
3. Anomaly Detection
- Rolling window comparisons to detect abrupt variations.
- Outliers are corrected or removed to improve reliability.
4. Data Smoothening
- Moving average filters and exponential smoothing applied to reduce noise.
5. Feature Engineering
- Lag Features: Capture temporal dependencies.
- Time-Based Inputs: Hour of day, day of week, seasonality.
- Polynomial Features: Capture nonlinear interactions.
6. Model Development
- Algorithm: Random Forest Regressor.
- Validation: TimeSeriesSplit to preserve chronological order.
7. Model Evaluation
- Metric: Mean Squared Error (MSE).
- Visualization: Actual vs. predicted energy consumption plots.
8. Model Interpretability
- SHAP Analysis: Explains feature importance.
- Helps refine the model by removing low-impact variables.

📊 Results
- The model successfully predicts short-term energy consumption patterns.
- SHAP analysis revealed temperature (t1) and pressure (p1) as the most influential features.
- Time-based features (e.g., evening spikes between 6–8 pm due to kitchen appliance usage) improved accuracy.
- The system provides dependable forecasts and transparent explanations, making it suitable for real-time monitoring and adaptive control in smart homes.

🚀 Future Scope
- Integration with real-time dashboards for homeowners.
- Expansion to multi-home datasets for broader applicability.
- Deployment in edge devices for on-site energy management.

📂 Repository Structure
├── data/                # Raw and cleaned datasets
├── notebooks/           # Jupyter notebooks for preprocessing & modeling
├── src/                 # Source code for feature engineering & model training
├── results/             # Evaluation metrics and SHAP visualizations
├── README.md            # Project documentation



