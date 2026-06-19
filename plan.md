# Project Execution Plan: House Price Prediction

This plan outlines the detailed steps and methodology for executing the Week 1 Internship Project from start to final submission.

---

## 🛠️ Step 1: Environment & Setup
1. **Verify Python & Libraries:** Ensure Python 3.x is installed along with the required scientific stack:
   * Data Manipulation: `pandas`, `numpy`
   * Machine Learning: `scikit-learn`
   * Visualization: `matplotlib`, `seaborn`
   * Notebook Environment: `jupyter` or `ipykernel`
2. **Directory Structure Setup:** Create the folder structure required for deliverables:
   * `HousePricePrediction_RishiSrivastava/` (Submission folder)
     * `Housing.csv`
     * `analysis.ipynb`
     * `summary.pdf` (or `summary.docx`)
     * `charts/`
       * `price_distribution.png`
       * `correlation_heatmap.png`
       * `actual_vs_predicted.png`

---

## 📥 Step 2: Data Acquisition
1. **Download Dataset:** We will download the Kaggle dataset (`Housing.csv`) containing 545 records and 13 columns.
2. **Download Strategy:** If downloading directly via Kaggle requires credentials, we will retrieve the identical verified dataset from a public GitHub raw URL using python to automate the process, and place it in the target directory as `Housing.csv`.

---

## 📓 Step 3: Jupyter Notebook Development (`analysis.ipynb`)
We will structure the Jupyter notebook following the 5 requested tasks:

### Task 1: Data Loading & Exploration
* Load `Housing.csv` using `pd.read_csv()`.
* Print the first 10 rows using `df.head(10)`.
* Run `df.shape` and `df.info()` to inspect row/column counts and data types.
* Programmatically identify numeric vs categorical columns.
* Print the missing value count for each column using `df.isnull().sum()`.

### Task 2: Data Cleaning & Preprocessing
* **Missing Values:** If any missing values exist, we will impute numerical columns with the median and categorical columns with the mode (or drop rows if the percentage of missing values is negligible).
* **Duplicates:** Check for and drop duplicate rows using `df.drop_duplicates()`.
* **Categorical Encoding:**
  * Map binary categorical features (`mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea`) from `yes`/`no` to `1`/`0`.
  * One-Hot Encode multi-category columns (e.g., `furnishingstatus` which has values: `furnished`, `semi-furnished`, `unfurnished`) using `pd.get_dummies()`, dropping the first column (`drop_first=True`) to avoid multicollinearity.
* **Feature Selection:** Evaluate columns to ensure only meaningful features are kept.

### Task 3: Model Building & Evaluation
* **Train-Test Split:** Split the clean dataset into training (80%) and testing (20%) sets using `train_test_split` from `sklearn.model_selection` with a set `random_state` for reproducibility.
* **Feature Scaling:** Apply standard scaling (`StandardScaler`) to features if necessary to improve regression convergence and interpretability.
* **Model 1: Linear Regression**
  * Train `LinearRegression` from `sklearn.linear_model`.
  * Make predictions on the test set.
  * Compute MAE, RMSE, and R² scores.
* **Model 2: Random Forest Regressor**
  * Train `RandomForestRegressor` from `sklearn.ensemble` (tune hyper-parameters like `n_estimators` and `max_depth`).
  * Make predictions on the test set.
  * Compute MAE, RMSE, and R² scores.
* **Comparison:** Create a comparative table/dataframe containing the metrics for both models to identify which is superior.

### Task 4: Visualization
Create and save three high-resolution charts as `.png` using `matplotlib.pyplot` and `seaborn`:
* **Chart 1 (Histogram):** Distribution of housing prices with a kernel density estimate (KDE) curve.
* **Chart 2 (Heatmap):** Correlation matrix heatmap of all numerical and encoded columns.
* **Chart 3 (Custom - Scatter Plot):** Actual vs. Predicted house prices for both models to visually inspect model fit and residuals.

### Task 5: Business Insights & Summary
Write a Markdown cell containing a 5-8 line executive summary:
1. Identifying the most influential housing features (based on coefficients of Linear Regression and feature importances of Random Forest).
2. Explaining model accuracy in plain, business-friendly terms.
3. Highlighting any surprising trends or outliers.
4. Providing a key strategic recommendation for real estate investment or pricing strategy.

---

## 📄 Step 4: Executive Summary Report (`summary.pdf`)
* Compile the findings, performance comparison table, and insights into a neat 1-page PDF document.
* Include the saved charts from Task 4 inside the PDF report to present a professional executive-ready deliverable.

---

## 🚀 Step 5: Git & GitHub Deployment
1. **Local Repository Setup:** Initialize a local git repository in the project folder.
2. **Ignore Unnecessary Files:** Create a `.gitignore` file to ignore cache, checkpoints, and local virtual environments.
3. **Commit Assets:** Add and commit all required files (`analysis.ipynb`, `Housing.csv`, `summary.pdf`, `charts/`).
4. **Create GitHub Repository:** Create a public GitHub repository named `XYlofyAI-Internship-Project1`.
5. **Push Code:** Link the local repository to remote and push the commits to the `main` branch.

---

## ✅ Step 6: Verification & Final ZIP Packaging
1. Validate that the Jupyter notebook runs from top-to-bottom without any errors (`Kernel -> Restart & Run All`).
2. Verify that all figures are rendered and saved properly.
3. Compress the folder `HousePricePrediction_RishiSrivastava` into a `.zip` file.
4. Verify that the ZIP file contains all required files and fits the size constraints.
