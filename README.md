# ML-Student-GPA-Predictor
Predicting student GPA using Linear Regression by converting categorical data into numerical format with dummy variables.



## 📊 Dataset Description

The dataset contains information for 1000 students.

**Features (Independent Variables):**
- **`Gender`:** Categorical (Male, Female)
- **`Age`:** Numerical
- **`Extra_Curricular`:** Categorical (No, Societies, Sports)
- **`Study_Hours`:** Numerical (Hours per week)
- **`Annual_Income`:** Numerical (Likely family income)
- **`Distance_From_Home`:** Numerical (Distance to university)
- **`ID`:** Unique identifier (was dropped as it's not a predictive feature)

**Target (Dependent Variable):**
- **`GPA`:** Numerical (Grade Point Average)

## 🎯 Key Learning Objectives

This project serves as a practical guide to:
1.  Handling categorical data using `pd.get_dummies()`.
2.  Avoiding the **Dummy Variable Trap** by dropping one category from each variable.
3.  Integrating engineered features back into the original dataset.
4.  Building and evaluating a Linear Regression model with mixed data types.

## 🛠️ Tech Stack & Libraries

- **Language:** Python
- **Libraries:**
  - `pandas` (Data manipulation and analysis)
  - `numpy` (Numerical operations)
  - `scikit-learn` (Machine learning: `train_test_split`, `LinearRegression`, `mean_squared_error`)
- **Environment:** Jupyter Notebook

## 🔧 Implementation Steps

1.  **Data Loading & Inspection:** Loaded the dataset and examined its structure.
2.  **Dummy Variable Creation:**
    - Identified categorical columns: `Gender` and `Extra_Curricular`.
    - Used `pd.get_dummies()` to convert them into numerical arrays.
    - **Avoided the Dummy Variable Trap** by dropping one redundant column from each set (`Gender_Female` and `Extra_Curricular_No`).
3.  **Data Preprocessing:**
    - Dropped the original categorical columns and the non-predictive `ID` column from the main dataframe.
    - Concatenated the new dummy variables with the remaining numerical features to create the final dataset for modeling.
4.  **Train-Test Split:** Divided the data into training (80%) and testing (20%) sets.
5.  **Model Training:** Trained a `LinearRegression` model on the processed training data.
6.  **Prediction & Evaluation:** Made predictions on the test set and evaluated the model's performance using:
    - **Mean Squared Error (MSE)**
    - **Root Mean Squared Error (RMSE)**


## 🚀 How to Run

1.  Ensure you have Python and Jupyter Notebook installed.
2.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn
    ```
3.  Place the `GPA_data.CSV` file in the correct directory or update the file path in the notebook.
4.  Open the `dummy variables.ipynb` notebook and run all cells.
