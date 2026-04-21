# petrolconsumptiondataset_multilinearregression
# Petrol Consumption Prediction using Linear Regression

## 📌 Project Overview

This project uses **Linear Regression** to predict petrol consumption based on various influencing factors such as population, income, and petrol price.

---

## 📊 Dataset Description

The dataset contains information about petrol consumption in different regions.

### Features:

* **Petrol_tax**: Tax imposed on petrol
* **Average_income**: Average income of people
* **Paved_Highways**: Length of paved highways
* **Population_Driver_licence(%)**: Percentage of people with driving licenses

### Target Variable:

* **Petrol_Consumption**: Amount of petrol consumed

---

## 🎯 Objective

To build a model that predicts **petrol consumption** using independent variables.

---

## ⚙️ Steps Involved

1. Import required libraries
2. Load dataset
3. Data preprocessing
4. Split dataset into training and testing sets
5. Train the model using Linear Regression
6. Make predictions
7. Evaluate the model

---

## 🧮 Model Used

* Linear Regression

The model follows the equation:

[
Y = b_0 + b_1X_1 + b_2X_2 + b_3X_3 + b_4X_4
]

Where:

* (Y) = Petrol Consumption
* (b_0) = Intercept
* (b_1, b_2, b_3, b_4) = Coefficients
* (X_1, X_2, X_3, X_4) = Input features

---

## 📈 Evaluation Metrics

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)

---

## 💻 Example Code

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

# Load dataset
dataset = pd.read_csv('petrol_consumption.csv')

# Features and target
X = dataset[['Petrol_tax', 'Average_income', 'Paved_Highways', 'Population_Driver_licence(%)']]
y = dataset['Petrol_Consumption']

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Model training
model = LinearRegression()
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)
```

---

## 📌 Conclusion

Linear Regression helps in understanding how different factors affect petrol consumption and allows prediction of future consumption trends.

---

## 🔗 Applications

* Fuel demand forecasting
* Transportation planning
* Government policy decisions

---
