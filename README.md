# 🚗 Car Price Prediction Model

This project builds a **machine learning model** to predict car prices based on a comprehensive set of features.  
The model leverages **data analysis**, **feature engineering**, and a powerful **Random Forest Regressor** to achieve **high-accuracy price predictions**.

---

## 📈 Project Overview
The primary goal of this project is to take a raw car dataset and transform it into a robust machine learning model.  
The process involves several key stages:

- 🔍 **Exploratory Data Analysis (EDA):** To understand the data and identify patterns.  
- 🛠️ **Feature Engineering:** To clean messy data and create new, more predictive features.  
- 🤖 **Model Training & Evaluation:** Using a Random Forest Regressor and hyperparameter tuning.  
- 🎯 **Prediction:** A user-friendly CLI interface for making car price predictions.  

---

## 📊 Dataset
The project uses a raw dataset **Cars.csv** containing a variety of features, including:

- 🏢 **Company Names** – Manufacturer of the car.  
- 🚘 **Cars Names** – Specific model name.  
- 🔧 **Engines** – Raw engine details (messy text format).  
- ⚡ **CC/Battery Capacity** – Displacement (cc) or battery capacity.  
- 🐎 **HorsePower** – Power output.  
- 🏎️ **Total Speed** – Top speed (km/h).  
- ⏱️ **Performance (0-100) KM/H** – Acceleration time.  
- 💰 **Cars Prices** – Target variable.  
- ⛽ **Fuel Types** – Petrol, Diesel, Hybrid, Electric, etc.  
- 💺 **Seats** – Number of seats.  
- 🌀 **Torque** – Engine torque.  

---

## 🛠️ Methodology

### 🔹 Data Preprocessing & Feature Engineering
- ✅ **Handling Missing Values:** Imputation for CC/Battery Capacity, Torque, Performance.  
- ✅ **Standardizing Categorical Data:** Cleaned & normalized text values.  
- ✅ **Engine Feature Extraction:** From messy `Engines` column → created structured features:  
  - `Engine_Displacement_L`  
  - `Engine_layout` (V, Inline, Rotary, Electric)  
  - `Engine_Cylinder_count`  
  - `Engine_Aspiration` (Turbo, SuperCharged, Naturally Aspirated)  
  - `Engine_Motor_Count`  

- ✅ **Encoding Categorical Features:** One-hot encoding applied.  

---

### 🤖 Model Training & Evaluation
- 📌 **Model Used:** Random Forest Regressor.  
- ⚙️ **Hyperparameter Tuning:** `GridSearchCV` for optimization.  
- 📊 **Metrics Used:** MAE, MSE, R².  

---

## 📈 Results

- **MAE:** `19974.27`  
- **MSE:** `3666180496.34`  
- **R² Score:** `0.913`  
- **OOB R² Score:** `0.477`  

✅ The model explains **91.3% of the variance** in car prices — a strong performance!  

---

## 💻 How to Use

The **interactive CLI** allows you to input new car configurations for price predictions.  
You’ll be prompted to enter:

- Company Name  
- Car Name  
- Engine Layout (e.g., I4, V6, Electric)  
- Engine Aspiration (None, Turbo, SuperCharged)  
- Fuel Type (Petrol, Diesel, Hybrid, Electric)  
- CC/Battery Capacity  
- HorsePower  
- Total Speed  
- Performance (0-100 KM/H)  
- Number of Seats  
- Torque  
- Engine Displacement (L)  
- Number of Cylinders  
- Motor Count  

➡️ The model will then return a **💰 Predicted Car Price**.  

---

## 📦 Dependencies
Install the following before running the project:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```
Also uses Python's built-in:
- re (regular expressions)
