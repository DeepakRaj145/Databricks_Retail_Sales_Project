# End-to-End Retail Sales Machine Learning Project Using Databricks

## 📌 Project Overview

This project demonstrates an end-to-end retail sales analytics and machine learning workflow implemented using Databricks.

The project covers data processing, exploratory data analysis, feature engineering, machine learning, experiment tracking, model registration, model serving, REST API inference, and natural-language business analytics using Databricks Genie.

---

## 🎯 Business Problem

Retail businesses generate large volumes of sales data containing information about products, categories, customers, locations, quantities, prices, and revenue.

The objective of this project is to build a Databricks-based solution that can:

- Analyze historical retail sales data.
- Identify important sales and revenue patterns.
- Prepare ML-ready data.
- Predict total revenue.
- Compare multiple regression models.
- Track experiments using MLflow.
- Register and manage the selected model using Unity Catalog.
- Deploy the model using Databricks Model Serving.
- Generate predictions through a REST API.
- Provide natural-language business analytics using Databricks Genie.

---

## 🏗️ Architecture

Raw Data
↓
Bronze Layer
↓
Silver Layer
↓
Gold Layer
↓
EDA & Feature Engineering
↓
Machine Learning
↓
Model Evaluation
↓
MLflow
↓
Unity Catalog
↓
Model Registry
↓
Model Serving
↓
REST API

Gold Data
↓
Databricks Genie
↓
Natural Language Queries
↓
SQL
↓
Business Insights

---

## 🛠️ Technologies Used

- Databricks
- PySpark
- Delta Lake
- Unity Catalog
- Spark ML
- XGBoost
- MLflow
- Databricks Model Serving
- REST API
- Databricks Genie
- SQL

---

## 📊 Dataset

The ML-ready dataset contains:

- product_id
- category
- gender
- city
- state
- Month
- Quarter
- WeekOfYear
- DayOfWeek
- DayOfMonth
- Total_quantity
- Max_price
- Total_revenue

### Target Variable

`Total_revenue`

---

## 🔄 Data Processing

The project follows a Medallion Architecture:

### Bronze

Initial structured representation of the retail sales data.

### Silver

Cleaned and transformed data prepared for analysis.

### Gold

Business-ready and ML-ready datasets used for analytics and machine learning.

---

## 🔍 Exploratory Data Analysis

EDA was performed across:

- Category
- Product
- Gender
- State
- City
- Month
- Sales Quantity
- Revenue

The analysis was used to understand sales patterns and prepare appropriate features for machine learning.

---

## 🤖 Machine Learning

The project evaluated multiple regression models:

| Model | RMSE | MAE | R² |
|---|---:|---:|---:|
| Decision Tree | 5364.00 | 3684.71 | 0.9914 |
| Random Forest | 9057.15 | 6566.77 | 0.9755 |
| XGBoost | 4556.37 | 3233.61 | 0.9938 |

XGBoost achieved the best performance among the evaluated models.

---

## 🧪 XGBoost Experimentation

Five XGBoost experiments were performed.

The best recorded experiment achieved:

- MSE: 20,081,582.68
- RMSE: 4,481.25
- MAE: 3,217.56
- R²: 0.993995

---

## 📈 MLflow

MLflow was used for:

- Experiment tracking
- Parameter tracking
- Metric tracking
- Model logging
- Model signature
- Model lifecycle management

---

## 🗂️ Model Registry

The selected model was registered in Unity Catalog as:

`retail_project.gold.retail_sales_xgboost`

The model was versioned and maintained through the Databricks model registry.

---

## 🚀 Model Serving

The registered XGBoost model was deployed using Databricks Model Serving.

Serving endpoint:

`retail-sales-xgboost-endpoint`

REST API testing successfully returned:

`Status Code: 200`

with a prediction response.

---

## 💬 Databricks Genie

A Genie Space named:

`Retail Sales Analytics Genie`

was created using:

`retail_project.gold.ml_model_sales_data`

Genie was configured with:

- Table description
- Column descriptions
- Business instructions
- Revenue aggregation rules
- Natural-language analytics requirements
- Anti-hallucination instructions

Example questions:

- What is the total revenue?
- What is the revenue by category?
- Which product generated the highest total revenue?
- Which state generated the highest total revenue?

---

## 💡 Key Insights

1. Retail revenue can be analyzed across product, category, gender, geography, and time.
2. Time-based feature engineering provides additional information for ML modeling.
3. Multiple regression models were compared instead of relying on a single algorithm.
4. XGBoost achieved the strongest recorded performance among the evaluated models.
5. XGBoost experimentation demonstrated the effect of model configuration on performance.
6. MLflow provided centralized experiment tracking.
7. Unity Catalog provided centralized model management and versioning.
8. Model Serving successfully exposed the selected model for inference.
9. REST API testing successfully generated predictions.
10. Genie enabled natural-language access to the Gold sales data.

---

## 🔮 Future Improvements

- Implement time-based model validation.
- Add more data to get better results.
- Perform additional data-leakage analysis.
- Add automated data-quality checks.
- Implement model and data drift monitoring.
- Add automated model retraining.
- Implement CI/CD.
- Build a production business dashboard.
- Evaluate specialized forecasting approaches for future revenue prediction.
- The model achieved an R² score of 99.39%. However, this high score is likely influenced by the small dataset. Training the model with a larger and more diverse dataset in the future can improve its generalization capability and provide more reliable evaluation results.
---

## 🏁 Conclusion

This project demonstrates an end-to-end Databricks workflow combining data engineering, analytics, machine learning, MLflow, Unity Catalog, model deployment, REST API inference, and Genie-based business analytics.

The project provides a production-oriented foundation for building scalable retail analytics and machine learning solutions on Databricks.

Note: Users should replace the placeholder with their own token(Databricks Token) before running the notebook.