# Laptop Price Predicting ML Model 💻📈

## 📝 Overview
This project provides a comprehensive  Analysis machine learning solution for predicting laptop prices based on technical specifications. By leveraging a rich dataset and state-of-the-art regression algorithms, the model quantifies how hardware variations like CPU frequency, RAM capacity, and storage technology affect market value.

## 🎯 Problem Statement
The laptop market is highly fragmented, with prices varying significantly based on small hardware deviations. Consumers and retailers often lack a data-driven way to determine if a laptop is fairly priced. This project solves this by:
- **Identifying key price drivers** (e.g., RAM, GPU quality).
- **Automating price estimation** for new or custom laptop configurations.
- **Reducing pricing uncertainty** through robust statistical modeling.

## 📊 Dataset
- **Source**: [Kaggle - Laptop Price Dataset](https://www.kaggle.com/datasets/muhammetvarl/laptop-price/data)
- **Description**: The dataset includes **1,303 instances** of laptops.
- **Features**: Brand (Company), Type (TypeName), Screen Size (Inches), CPU, RAM, Memory, GPU, Operating System, and Weight.
- **Row Count**: 1,303 entries.

## 🛠️ Technologies Used
- **Language**: Python 🐍
- **Analysis**: Pandas, NumPy
- **Visuals**: Matplotlib, Seaborn, Plotly
- **Machine Learning**: Scikit-Learn, XGBoost, GradientBoosting
- **API**: Kaggle API for data automation

## 🖼️ Visual Insights
Understanding the data through visualization was a key part of the project.

### 1. Feature Correlation
We analyzed how different features correlate with the price. Numerical columns like `RAM(GB)` and `Cpu_Freq(GHz)` showed the strongest positive correlations.

![Correlation Heatmap](./plot.png/Correlation_heatmap.png)

### 2. Market Distributions
We looked at the distribution of prices across different laptop types and companies.

![Laptop Type vs Price](./plot.png/TypenameVsPrice.png)

## 🔄 Project Workflow
1.  **Data Acquisition**: Automated download using Kaggle token logic.
2.  **Feature Engineering**:
    *   Parsed CPU and GPU strings to extract company and model information.
    *   Cleaned RAM and Weight into numeric values.
    *   Calculated `Touchscreen` and `Resolution` from screen descriptions.
3.  **Preprocessing**:
    *   Constructed a `ColumnTransformer` for mixed data types.
    *   **Ordinal Encoding** for categoricals and **Standard Scaling** for numericals.
4.  **Modeling**: Evaluated Linear Regression, KNN, Random Forest, XGBoost, and Gradient Boosting.
5.  **Optimization**: Tuned the **Random Forest** and **Gradient Boosting** models using `GridSearchCV`.

## 🏆 Results
The **Gradient Boosting Regressor** performed best, especially after log-transforming the target variable.

### Performance Metrics:
| Metric | Score |
| :--- | :---: |
| **R² Score** | **0.9078** |
| **MAE** | **0.2105** |
| **RMSE** | **0.2893** |

### Actual vs. Predicted Prices
The following plot shows the strong alignment between our model's predictions and the actual market prices.

![Gradient Boosting Performance](./plot.png/GradientBoostingActualVsPredictedPrices.png)



## 📂 Project Structure
```text
├── datasets/                 # CSV data source
├── plot.png/                 # Generated project visualizations
├── MLregressionLAPTOP1_FINAL3.ipynb # Main analysis notebook
└── README.md                 # Project documentation
```



## 👨‍💻 Author
**Laptop Project Team**  
Louay Mohammed ,
Amr Khaled,
Mahmoud Salah
