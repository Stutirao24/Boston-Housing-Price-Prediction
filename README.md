#  Boston Housing Price Prediction

This project implements **Linear Regression** and other ML models to predict the **median value of houses (MEDV)** in Boston suburbs based on various socio-economic and geographical factors.  

---

##  Objective
The goal is to build a predictive model that estimates house prices using features like crime rate, average number of rooms, pollution levels, and accessibility to highways.  

---

##  Dataset
- **Source:** [Boston Housing Dataset (OpenML)](https://www.openml.org/d/531)  
- **Instances:** 506  
- **Features:** 13 predictive variables  
- **Target Variable:** `MEDV` → Median value of owner-occupied homes in $1000’s  

### Features:
- `CRIM` – per capita crime rate by town  
- `ZN` – proportion of residential land zoned for large lots  
- `INDUS` – proportion of non-retail business acres  
- `CHAS` – Charles River dummy variable  
- `NOX` – nitric oxides concentration  
- `RM` – average number of rooms per dwelling  
- `AGE` – proportion of old houses  
- `DIS` – distance to employment centres  
- `RAD` – accessibility to highways  
- `TAX` – property tax rate  
- `PTRATIO` – pupil-teacher ratio  
- `B` – proportion of Black residents  
- `LSTAT` – % lower status population  

---

##  Methodology
1. **Data Preprocessing**
   - Train-test split (80%-20%)  
   - Standardization using `StandardScaler`  

2. **Models Used**
   - Linear Regression  
   - Ridge Regression  
   - Lasso Regression  
   - Random Forest Regressor (for comparison)  

3. **Evaluation Metrics**
   - Mean Squared Error (MSE)  
   - Root Mean Squared Error (RMSE)  
   - Mean Absolute Error (MAE)  
   - R² Score  

---

##  Results

### Linear Regression:
- MSE: ~21.9  
- RMSE: ~4.68  
- MAE: ~3.3  
- R²: ~0.73  

### Random Forest (best performance):
- R²: >0.85  

### Key Features:
- 🔼 `RM` (average rooms) increases house price  
- 🔽 `LSTAT` (% lower status population) decreases house price  
- `DIS` and `NOX` also negatively impact house prices  

---

##  Visualizations
- **Actual vs Predicted** scatter plot  
- **Residuals vs Predicted** plot  
- **Feature Importance Barplot**  

---

##  Conclusion
- Linear Regression provides a strong baseline model.  
- Random Forest achieves the best performance (R² > 0.85).  
- `RM` and `LSTAT` are the most influential predictors of house prices.  

---

##  Technologies Used
- Python   
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  

---


---

##  Project Structure
├── boston_housing.ipynb # Jupyter Notebook with full code
├── README.md # Project documentation
└── requirements.txt # Dependencies


---
## ⚠ Limitations

- **Outdated dataset:** The Boston Housing dataset was collected in the 1970s and may not reflect current housing trends.  
- **Ethical concerns:** The `B` (Black population) feature has racial bias issues, which is why `load_boston()` was removed from scikit-learn.  
- **Small dataset size:** Only 506 instances, which limits the ability to train more complex models.  
- **Model assumptions:**  
  - Linear Regression assumes linearity, no multicollinearity, and constant variance of residuals. These assumptions are not fully satisfied in this dataset.  
  - The model is sensitive to outliers.  
- **Performance:** Linear Regression explained only ~73% variance (R² ≈ 0.73), whereas tree-based models performed better.  

---

##  Future Work

- Use larger and more recent housing datasets (e.g., California Housing dataset).  
- Apply **feature engineering** to handle non-linear relationships.  
- Implement **regularization techniques** (Ridge, Lasso, ElasticNet) to handle multicollinearity.  
- Try **ensemble models** (Random Forest, Gradient Boosting, XGBoost) for better performance.  
- Perform **cross-validation** to get more reliable performance estimates.  
- Deploy the model using **Flask / FastAPI / Streamlit** for real-world usability.  


---

##  Author
- **Stuti Rao**  
- [LinkedIn](www.linkedin.com/in/stuti-rao06) | [GitHub](https://github.com/Stutirao24)  

---
