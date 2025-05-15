# Rossmann Store Sales Forecasting

## Project Overview

Sales forecasting is the process of predicting future sales based on historical data and trends. Accurate sales forecasting helps businesses optimize inventory, marketing, staffing, and financial planning.

This project uses the **Rossmann Store Sales** dataset to predict future sales using machine learning. The dataset includes store information, past sales, promotions, and competition data.

---
🔗 **Notebook Link**: [Rossmann Store Sales - Marketing Effort](https://www.kaggle.com/code/krishnayadav456wrsty/rossmann-store-sales-marketing-effort)
---
## Dataset

The dataset contains:

| File               | Description                                           |
|--------------------|-------------------------------------------------------|
| `train.csv`        | Historical sales data including Store, Date, Sales, etc. |
| `test.csv`         | Test data to predict sales for future dates           |
| `store.csv`        | Store metadata such as store type and competition info |
| `sample_submission.csv` | Sample format for submission                         |

---

## Approach & Methodology

### Steps:
1. **Data Preprocessing:**  
   - Load datasets and merge `train.csv` with `store.csv` on Store ID  
   - Extract time features like Month, Day, Year from Date column  
   - Handle missing values and encode categorical variables  

2. **Exploratory Data Analysis (EDA):**  
   - Visualize monthly sales trends to understand seasonality  
   - Identify sales spikes and drops (e.g., December spike)  

3. **Feature Engineering:**  
   - Add features such as Month, Day of Week, Promotion, and Competition  
   - (Optional) Create lag features and rolling averages for future improvements  

4. **Modeling:**  
   - Use `XGBRegressor` (Extreme Gradient Boosting) for sales prediction  
   - Train model on historical data and evaluate performance  

5. **Evaluation:**  
   - Metrics used:  
     - Mean Absolute Percentage Error (MAPE)  
     - Root Mean Squared Error (RMSE)  
   - Compare predicted sales with actual sales  

---
![Screenshot 2025-05-15 204628](https://github.com/user-attachments/assets/93616675-ee11-4f90-b940-e70ebf5b51a8)

## Code 

![Screenshot 2025-05-15 220144](https://github.com/user-attachments/assets/5208e446-7cd1-4326-9571-b7cf2df9b4bb)




# Evaluation

![Screenshot 2025-05-15 220117](https://github.com/user-attachments/assets/f6797ca3-e883-434d-b3a8-71c7fe2ebaae)

---

## Results

| Metric                                | Value   |
| ------------------------------------- | ------- |
| Mean Absolute Percentage Error (MAPE) | 30.93%  |
| Root Mean Squared Error (RMSE)        | 2520.90 |

### Insights:

* **Seasonality:** December shows a significant increase in sales.
* **Model Performance:**

  * The model predicts sales with an average error of about 31%.
  * RMSE indicates the average prediction error in sales units (\~2520).
* **Business Impact:**

  * Enables better inventory and marketing planning.
  * Identifies periods needing promotional efforts.

---

## Future Work i will be maybe 

* Adding lag and rolling average features to improve time-series dependency capture.
* Try deep learning models (LSTM) for better long-term forecasting.
* Incorporate holidays and local events into features.
* Hyperparameter tuning for XGBoost.
* trying get a good core  For a Real Business Application:

MAPE above 20% is often considered too high.

For decision-making (like inventory), you'd want MAPE < 15% ideally.



---



## Prediction Output Sample

| Id | Predicted Sales |
| -- | --------------- |
| 1  | 6839.46         |
| 2  | 6839.46         |
| 3  | 7145.07         |
| 4  | 7145.07         |
| 5  | 7145.07         |

.

---

## Conclusion

ON This project demonstrates a basic sales forecasting system using XGBoost on the Rossmann dataset. The insights and predictions generated can help businesses make data-driven decisions regarding inventory and marketing. Further improvements can enhance accuracy and robustness.

---
![Screenshot 2025-05-15 220840](https://github.com/user-attachments/assets/732c4cbe-8b78-446d-b88f-c52b323fb2b1)



