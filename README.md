# Real Estate Price Prediction Notebook

This Jupyter Notebook demonstrates a complete, step-by-step machine learning workflow to predict real estate prices based on the `Real estate.csv` dataset.

The project starts with raw data, cleans it, explores it, and then builds and compares two different regression models to find the most accurate one.

## Notebook Structure

The notebook is broken down into the following key sections:

1. **Import Libraries:** Loads all necessary toolkits, including `pandas` (for data manipulation), `numpy` (for numerical operations), `matplotlib`/`seaborn` (for visualization), and `sklearn` (for machine learning).
2. **Load Data:** Reads the `Real estate.csv` file into a pandas DataFrame.
3. **Data Cleaning & Preparation:**
    - Drops the unnecessary 'No' column.
    - Renames all columns to be simple and Python-friendly (e.g., "X3 distance to the nearest MRT station" becomes "distance_to_mrt").
4. **Exploratory Data Analysis (EDA):**
    - Uses `.head()`, `.info()`, and `.describe()` to understand the data's structure, types, and statistical summary.
    - Generates a **correlation heatmap** to visually identify which features are most strongly related to the house price.
5. **Feature & Target Definition:**
    - Separates the data into `X` (the features used for prediction) and `y` (the 'price' target we want to predict).
6. **Train/Test Split:**
    - Splits the dataset into a training set (80%) and a testing set (20%) to ensure the model is evaluated on unseen data.
7. **Model 1: Linear Regression (Baseline)**
    - A simple, baseline model is trained on the data.
    - The model is evaluated using **R-squared (**$R^2$**)** and **Root Mean Squared Error (RMSE)**.
    - Its predictions are visualized on a scatter plot against the actual prices.
8. **Model 2: Random Forest Regressor (Improved Model)**
    - A more powerful and complex model (`RandomForestRegressor`) is trained on the *same* data.
    - It is also evaluated using R-squared and RMSE.
    - Its predictions are visualized on a separate scatter plot.
9. **Model Comparison:**
    - The performance metrics (R² and RMSE) for both models are printed side-by-side, demonstrating that the Random Forest model provides a more accurate prediction for this dataset.

## How to Use

1. Ensure you have Jupyter Notebook or JupyterLab installed.
2. Place the `realestate-model.ipynb` file and the `Real estate.csv` dataset in the same directory.
3. Open the notebook.
4. Run the cells from top to bottom.

## Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn` (sklearn)
