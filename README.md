# **Optimization Sparse Regression Approach In Chemometrics Using Machine Learning**

This project aims to predict the magnesium content (`Mg`) in aluminum alloys using machine learning models. We used two regression models: **Linear Regression** and **Random Forest Regressor** to develop a prediction model based on features from an aluminum spectrometry dataset. The dataset contains various physical and chemical properties of aluminum alloys, and the objective is to predict the magnesium content (`Mg`) based on these features.

The project involves data preprocessing, model training, evaluation, and comparison of both regression models to assess their predictive accuracy.

## **Objective**

- To predict the `Mg` content (magnesium) of aluminum alloys using machine learning models.
- To evaluate and compare the performance of **Linear Regression** and **Random Forest Regressor** using evaluation metrics such as **R²**, **Mean Squared Error (MSE)**, **Mean Absolute Error (MAE)**, and **Root Mean Squared Error (RMSE)**.

## **Methodology**

1. **Data Loading**: We load and clean two datasets, including features related to aluminum alloys and chemical elements.
2. **Data Preprocessing**: 
    - Handle missing values through mean imputation.
    - Drop irrelevant columns.
    - Merge datasets to align features and target values.
3. **Model Training**: 
    - We train two models: **Linear Regression** and **Random Forest Regressor**.
4. **Evaluation**: Evaluate both models using metrics such as **R²**, **MSE**, **MAE**, and **RMSE**.
5. **Visualization**: Scatter plots of actual vs predicted values are plotted to visually assess model performance.

## **Results**

### Model Comparison Table

| **Metric**               | **Linear Regression** | **Random Forest Regressor** |
|--------------------------|-----------------------|-----------------------------|
| **R² Score**             | 0.9999                | 0.9998                      |
| **Mean Squared Error**   | 2.2877e-25            | 2.1817e-06                  |
| **Mean Absolute Error**  | 1.7234e-13            | 1.2312e-03                  |
| **Root Mean Squared Error** | 4.7829e-13          | 0.0015                      |

### **Key Insights**
- Both models achieved near-perfect performance with very high **R² scores** (close to 1, which might indicate an overfitting), indicating that the models explain most of the variance in the target variable.
- **Linear Regression** demonstrated a perfect performance with almost no error, with **MSE** and **RMSE** approaching zero.
- **Random Forest** performed slightly less well in terms of **MSE** and **RMSE** but still provided highly accurate predictions, which might indicate robustness and less susceptibility to overfitting.

## **Usage**

To use this project and run the models, follow these steps:

1. **Clone the repository** (or download the project files):
   ```bash
   git clone https://github.com/barkiayoub/chemometrics-ml.git
   cd chemometrics-ml
   ```

2. **Install dependencies**: You will need Python 3.x and several Python libraries. You can install them using `pip`:
   ```bash
   pip install -r requirements.txt
   ```

3. **Prepare the datasets**: Place the required datasets in the `Data/` directory. The datasets should include:
   - `Al_Spectre.xlsx`
   - `CRM ELEMISSION Maroc-1.xlsx`

4. **Run the main notebook**:  
   ```bash
   jupyter notebook chemometrics_ml.ipynb
   ```

5. **View results**: The notebook will output evaluation metrics (R², MSE, MAE, RMSE) and show visualizations of actual vs predicted values for both models.

---

## **Conclusion**

Both **Linear Regression** and **Random Forest Regressor** models demonstrated excellent performance in predicting magnesium content in aluminum alloys. While **Linear Regression** provided slightly better accuracy, the **Random Forest** model offers a more flexible and potentially more robust approach, especially when dealing with more complex, non-linear relationships in the data.