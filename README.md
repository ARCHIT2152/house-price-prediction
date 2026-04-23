# 🏠 House Price Prediction Project

## 📌 Overview

This project focuses on predicting housing prices using machine learning techniques. It uses a dataset containing various housing features such as location, number of rooms, population, and more.

The goal is to build regression models that can accurately estimate the **median house value**.

---

## 📂 Dataset

* Dataset used: `housing.csv`
* Contains features like:

  * `longitude`, `latitude`
  * `total_rooms`, `total_bedrooms`
  * `population`, `households`
  * `median_income`
  * `ocean_proximity` (categorical)

---

## ⚙️ Project Workflow

### 1. Data Loading

* Loaded dataset using **pandas**

### 2. Data Cleaning

* Checked for missing values
* Dropped rows with null values:

```python
df.dropna(inplace=True)
```

### 3. Feature Engineering

* Applied **log transformation** to reduce skewness:

  * `total_rooms`
  * `total_bedrooms`
  * `population`
  * `households`

* Created new features:

  * `bedroom_ratio`
  * `household_rooms`

### 4. Encoding

* Converted categorical feature (`ocean_proximity`) using **one-hot encoding**

### 5. Train-Test Split

* Split data into training and testing sets:

```python
train_test_split(test_size=0.2, random_state=42)
```

---

## 📊 Data Visualization

* Histogram plots for feature distribution
* Heatmap for correlation analysis
* Scatter plot for geographic price distribution

---

## 🤖 Models Used

### 1. Linear Regression

* Simple baseline model
* Evaluated using **R² score**

### 2. Random Forest Regressor

* More powerful ensemble model
* Handles non-linearity better

---

## 📈 Results

* Linear Regression:

  * Training Score (R²): 0.6716
  * Test Score (R²): 0.6687

* Random Forest:

  * Test Score (R²): 0.8183635120697268

---

## 🛠️ Technologies Used

* Python 🐍
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## 🚀 How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/your-repo-name.git
```

2. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Run the notebook:

```bash
jupyter notebook hh.ipynb
```

---

## 💡 Future Improvements

* Handle missing values using imputation instead of dropping
* Try advanced models (XGBoost, Gradient Boosting)
* Hyperparameter tuning
* Feature selection

---

## 👤 Author

* Archit Bankey

---

## ⭐ If you like this project

Give it a star on GitHub!
