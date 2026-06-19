# Project Overview: Week 1 House Price Prediction

Welcome to the **Week 1 Internship Project** at **Xylofy AI**. This project involves building a machine learning regression model to predict house prices using key property features and extracting business-actionable insights from the data.

---

## 🎯 Problem Statement
Real estate buyers and sellers often rely on guesswork, intuition, or outdated comps to estimate a property's fair market value. Outdated methods can lead to overpriced assets that sit on the market or underpriced listings that leave money on the table.

Our goal is to build an end-to-end data science solution:
1. **Develop a regression model** to predict housing prices based on features like size, bedrooms, bathrooms, stories, amenities, and location.
2. **Identify which features most strongly influence price** to assist a real estate business in optimizing their buying/selling strategies.
3. **Present our findings** visually using charts and a short executive report.

---

## 📅 Timeline
- **Assigned Date:** May 17, 2026
- **Submission Date:** May 21, 2026
- **Status:** In Progress (Planning Phase)

---

## 📊 Dataset Details
We will be using the **Housing Prices Dataset** (hosted on Kaggle by Yasser H). It contains **545 records** of homes with **13 columns**:

### Target Variable
* `price`: The sale price of the house (Numeric)

### Features (Predictors)
* `area`: Total area of the house in square feet (Numeric)
* `bedrooms`: Number of bedrooms (Numeric)
* `bathrooms`: Number of bathrooms (Numeric)
* `stories`: Number of stories/floors (Numeric)
* `mainroad`: Whether the house is connected to the main road (Categorical: yes/no)
* `guestroom`: Whether the house has a guest room (Categorical: yes/no)
* `basement`: Whether the house has a basement (Categorical: yes/no)
* `hotwaterheating`: Whether the house has hot water heating (Categorical: yes/no)
* `airconditioning`: Whether the house has central air conditioning (Categorical: yes/no)
* `parking`: Number of parking spaces (Numeric)
* `prefarea`: Whether the house is in a preferred neighborhood (Categorical: yes/no)
* `furnishingstatus`: Furnishing status of the house (Categorical: furnished, semi-furnished, unfurnished)

---

## 📝 Required Tasks
All analysis and modeling must be conducted inside a Jupyter Notebook (`analysis.ipynb`) broken down into five distinct phases:

### 🔍 Task 1 — Data Loading & Exploration
* Load the CSV dataset into a Pandas DataFrame.
* Display the first 10 rows to inspect the data format.
* Determine the dimensions of the dataset (row/column count).
* Identify the target variable and predictor features.
* Check for missing (`null`) values in each column.

### 🧹 Task 2 — Data Cleaning
* Handle missing values (impute or drop depending on columns).
* Remove duplicate rows, if any exist.
* Convert categorical variables (binary yes/no and furnishing status) into numeric representations using encoding techniques (e.g., One-Hot Encoding).
* Feature selection: retain only features relevant to the target.

### 🤖 Task 3 — Model Building
* Split the dataset into training and testing sets (80% train, 20% test).
* Train a baseline **Linear Regression** model.
* Evaluate performance using:
  * **Mean Absolute Error (MAE)**
  * **Root Mean Squared Error (RMSE)**
  * **R² (Coefficient of Determination) Score**
* Train a second model: **Random Forest Regressor** and compare its performance to the baseline Linear Regression model.

### 📈 Task 4 — Visualization (Minimum 3 Charts)
* **Chart 1:** Price distribution histogram.
* **Chart 2:** Correlation heatmap showing features relating to price.
* **Chart 3:** A custom plot of our choice (e.g., actual vs. predicted price scatter plot, or price vs. area scatter plot).

### 💡 Task 5 — Insights & Summary
Write a 5–8 line summary in the notebook answering:
1. Which features influence house price the most?
2. How accurate is the model (in plain terms)?
3. What was a surprising trend in the data?
4. One actionable recommendation for a real estate business.

---

## 📦 Deliverables & Submission Format
All deliverables must be packaged inside a folder named `HousePricePrediction_[YourName]` (in our case, `HousePricePrediction_RishiSrivastava`) containing:
1. `analysis.ipynb`: The complete Jupyter Notebook documenting all 5 tasks.
2. `Housing.csv`: The raw dataset used for analysis.
3. `summary.pdf` or `summary.docx`: A 1-page executive summary report outlining findings and model performance.
4. `charts/`: A folder containing the three generated charts saved in `.png` format.

The parent folder must be zipped (`.zip`) and submitted via the designated Google Form link.

Additionally, a Github repository named `XYlofyAI-Internship-Project1` must be initialized, containing all required deliverables for project presentation and code review.
