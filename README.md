# ElectricityBillPrediction

This project predicts the monthly electricity bill using traditional machine learning models, based on household appliance usage, location, tariff, and estimated energy consumption.

---

##  Objective

To develop a supervised regression model that accurately predicts electricity bills using input features such as:

- Appliance counts (Fan, Refrigerator, AC, etc.)
- Monthly usage hours
- Tariff rate
- City and energy company

---

##  Approach

1. **Data Preprocessing**:   
     Categorical features like `City` and `Company` were label encoded.    
     Feature engineering was done to estimate total power usage and cost.
   
2. **Feature Engineering with Real-World Power Ratings**
      
      To improve interpretability and model performance, we used **estimated power consumption values** for each appliance type:
      
      | Appliance       | Estimated Power (Watts) |
      |----------------|--------------------------|
      | Fan            | 75 W                     |
      | Refrigerator   | 250 W                    |
      | Air Conditioner| 1500 W                   |
      | Television     | 120 W                    |
      | Monitor        | 50 W                     |
      | Motor Pump     | 1000 W                   |
      
      From this, we calculated:
      
      - `EstimatedEnergyKWh` = `(Total Power × Monthly Usage Hours) / 1000`
      - `EstimatedCost` = `EstimatedEnergyKWh × TariffRate`
      
      These features added meaningful energy-related context to raw appliance counts and helped bridge the gap between input features and actual bill amounts.
      
      ---
3. **Model Training**:
   - Baseline model: Linear Regression
   - Final model: RandomForestRegressor
4. **Evaluation Metrics**:
   - RMSE (Root Mean Squared Error)
   - R² Score

---

##  Results

| Model                | RMSE   | R² Score |     
| Linear Regression    | ~30    | 0.9992   |       
| Random Forest        | ~17.83 | 0.999720 |      


##  Key Takeaways

- `EstimatedCost`, `TariffRate`, and `MonthlyHours` were top important features.
- Random Forest provided the best performance without overfitting.
- The model is interpretable and works well for real-world energy forecasting.

---

##

---

