# 🌊 Smart Ocean Wave Prediction

Smart Ocean Wave Prediction for Fisherman Safety (Random Forest) This project implements a Random Forest Regression system to predict ocean wave conditions and classify fishing safety for different vessel types.

---

## 📖 Project Overview: 

Ocean wave conditions directly affect the safety of fishermen at sea. This project builds a machine learning pipeline that predicts significant wave height (Hs) and peak wave direction from oceanographic inputs, then classifies fishing safety (Safe / Caution / Unsafe) based on the predicted wave height and the type of vessel being used.

---
## 📂 Dataset:

- Synthetic Oceanographic Dataset (generated within the notebook)
- 2,000 samples
- Features: Hmax, Tz, Tp, SST, and date/time-derived features (hour, day, month, day of week)
- Targets: Significant Wave Height (Hs) & Peak Wave Direction (°)
- No external dataset required — real buoy/satellite data can be substituted for production use.

---

## 🛠️ Technologies Used:

- Python 🐍
- scikit-learn (RandomForestRegressor)
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Joblib

---

## 🧩 Model Architecture: The system consists of two Random Forest Regression models:

- Wave Height Model — predicts significant wave height (Hs)
- Peak Direction Model — predicts peak wave direction (°)
- Safety Classification Function — maps predicted Hs to a safety level based on vessel type
---
*Output*
--------------------------------
|=== Wave Height Model (Hs) ===|
--------------------------------
|MAE  | 0.1619 m               |
|RMSE | 0.2091 m               |
|R²   | 0.9760                 |
--------------------------------
---
------------------------------
|=== Peak Direction Model ===|
-----------------------------|
|MAE  : 93.3422 °            |  
|RMSE : 107.6051 °           |
|R²   : -0.0571              |
------------------------------

---

## ⚙️ Workflow:

1. Import libraries
2. Generate / load ocean wave dataset
3. Preprocess data (feature selection & train-test split)
4. Train Random Forest models (wave height & direction)
5. Evaluate model performance (MAE, RMSE, R²)
6. Save trained models (.pkl)
7. Build prediction function
8. Classify fishing safety by vessel type
9. Test all vessel types
10. Visualize results

---

## 📊 Results:

- The model successfully predicts wave height and peak direction from input conditions.
- Achieves strong R² performance on unseen test data.
- Fishing safety is correctly classified across all four vessel categories (shore, small, medium, large).

---

## ▶️ Visualization:

**Hmax vs Hs Scatter Plot**

<img width="554" height="455" alt="image" src="https://github.com/user-attachments/assets/85fdb26b-6eac-4d33-9538-4f1abebf77a3" />

---

**Significant Wave Height (Hs) Distribution Plot**

<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/ce5d2e26-aef9-4c78-a56b-f0cc6327d877" />

---

**Actual vs Predicted Hs Comparison Plot**

<img width="554" height="455" alt="image" src="https://github.com/user-attachments/assets/ce6a27c9-6a45-435d-abf3-1430ea2ce64c" />

---

## ⚓ Safety Classification:

| Vessel Type | Safe        | Caution      | Unsafe    |
|-------------|-------------|--------------|-----------|
| Shore       | Hs ≤ 0.5 m  | 0.5 – 1.0 m  | > 1.0 m   |
| Small Boat  | Hs ≤ 0.5 m  | 0.5 – 1.0 m  | > 1.0 m   |
| Medium Boat | Hs ≤ 1.0 m  | 1.0 – 2.0 m  | > 2.0 m   |
| Large Boat  | —           | Hs ≤ 3.0 m   | > 3.0 m   |
---

## ⚠️ Disclaimer: 

This project uses synthetic data for demonstration purposes only. Predictions are not derived from real oceanographic measurements and should not be used for actual navigation or safety decisions.

---
## 👨‍💻 Author: 

**Nagaraj M**

https://github.com/M-Nagaraj02
---
