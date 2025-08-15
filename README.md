# CAPSTONE 3 – Saudi Arabia Used Cars Price Prediction

## Project Overview
This project analyzes and predicts used car prices in Saudi Arabia using data sourced from **syarah.com**, a popular car trading platform. The dataset contains **5,624 records**, each describing details of a listed used car.  

The main objective is to **develop a price prediction model** that can assist both **buyers** and **sellers** in estimating fair market values based on a car’s features.

---

## Problem Statement
Car buyers and sellers in Saudi Arabia often face uncertainty regarding the fair price of a vehicle.  
A reliable price prediction system would:
- Improve **decision-making** for both buyers and sellers.
- Increase **trust** in online car marketplaces.
- Reduce **negotiation time** by providing a baseline estimate.

---

## Dataset Description
The dataset contains various types of features:

### Boolean
- `Negotiable` – `True` if price is `0` (negotiable).

### Categorical
- `Type` – Model/type of the car.
- `Region` – Geographic region where the car is listed.
- `Make` – Car manufacturer (e.g., Toyota, Nissan).
- `Gear_Type` – Transmission type.
- `Origin` – Country of origin.
- `Options` – Trim/options of the car.

### Numerical
- `Year` – Manufacturing year.
- `Engine_Size` – Engine displacement (L).
- `Mileage` – Distance traveled (km).
- `Price` – Listed price (SAR).

---

## Data Preprocessing Steps
1. **Handle Negotiable Prices** – Replace `0` prices with `NaN` or process accordingly.
2. **Remove Duplicates** – As duplicates are minimal, they are dropped.
3. **Data Type Conversion** – Convert `Year` from numerical to string since it’s categorical.
4. **Missing Values** – No missing values found in the dataset.
5. **Encoding & Transformation** – Prepare data for machine learning (label encoding, scaling).

---

## Project Workflow
1. **Data Collection** – From `syarah.com`.
2. **Data Cleaning & Preprocessing** – Remove inconsistencies and prepare features.
3. **Exploratory Data Analysis (EDA)** – Understand patterns & relationships.
4. **Feature Engineering** – Create new features or transform existing ones.
5. **Modeling** – Apply machine learning algorithms for price prediction.
6. **Evaluation** – Measure model performance using regression metrics.

---

## Conclusion
This project successfully developed a **machine learning model** to predict used car prices in Saudi Arabia using data from **syarah.com**.  
After data cleaning, preprocessing, and testing several algorithms, the **K-Nearest Neighbors Regressor (KNN)** with hyperparameter tuning delivered the best balance between accuracy and generalization.  

Key takeaways:
- **Feature preprocessing** (encoding, scaling, and categorical handling) significantly improved model performance.
- **KNN** outperformed Linear Regression and Decision Tree Regressor in terms of error metrics (MAE and RMSE).
- The model achieved **low test error**, indicating it can provide reliable estimates for unseen data.
- This solution can help **buyers, sellers, and dealerships** make more informed decisions and set competitive yet fair prices.

Future improvements could involve:
- Integrating **real-time market data** for more dynamic predictions.
- Including **external factors** like fuel prices and seasonal trends.
- Deploying the model as a **web or mobile application** for instant public access.

---

## Recommendations

### Machine Learning
1. **Expand Feature Engineering**  
   - Create `Car_Age = Current Year - Year of Manufacture`.  
   - Derive `Price_per_KM = Price / Mileage`.  
   - Combine related features, e.g., `Engine_Size × Options`.

2. **Address Outliers More Rigorously**  
   - Remove unrealistic prices or mileage values.  
   - Use IQR filtering or Isolation Forest.

3. **Experiment with More Models**  
   - Test Gradient Boosting algorithms (XGBoost, LightGBM, CatBoost).  
   - Compare their performance against KNN.

4. **Optimize Hyperparameters Further**  
   - Expand search space for `n_neighbors`, `weights`, and `p` values in KNN.  
   - Tune parameters for tree-based models.

5. **Model Interpretability**  
   - Use SHAP values or feature importance plots to explain results.

6. **Cross-validation Strategy**  
   - Consider stratified sampling based on car type or year.  
   - Report R² alongside MAE and RMSE.

### Business
1. **Integrate Model into Online Platforms**  
   - Deploy into `syarah.com` or dealership systems.  
   - Allow users to input car details for instant valuation.

2. **Provide Price Confidence Ranges**  
   - Show price ranges instead of a single prediction.

3. **Dynamic Pricing Strategy**  
   - Update predictions with current market data.  
   - Detect overpriced or underpriced listings.

4. **Value-added Insights**  
   - Offer comparisons with similar cars.  
   - Show historical price trends.

5. **Partnership Opportunities**  
   - Collaborate with insurance companies and banks.

6. **User Engagement Features**  
   - Allow users to save predictions and track changes over time.  
   - Send alerts when market conditions are favorable.

---

## Files in Repository
- `CAPSTONE 3 MUHAMMAD NAFI ADZIQ.ipynb` – Main analysis & modeling notebook.
- `data_saudi_used_cars.csv` – Raw dataset (if included).
- `README.md` – Project documentation.

---

## Author
**Muhammad Nafi Adziq**
