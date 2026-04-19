# 🏠 End-to-End Housing Price Prediction using PySpark

## Project Overview
This project builds a **scalable machine learning pipeline using PySpark** to predict housing prices based on various socio-economic and geographical features.

It covers the **complete data science lifecycle**:
- Data Ingestion
- Data Cleaning
- Feature Engineering
- Feature Scaling
- Categorical Encoding
- Model Building
- Evaluation

---

## Tech Stack
- Python 
- PySpark 
- Spark MLlib
- Pandas
- Google Colab

---

## Dataset Features
- `median_house_value` (Target)
- `median_income`
- `total_rooms`, `total_bedrooms`
- `population`, `households`
- `housing_median_age`
- `ocean_proximity` (Categorical)

---

## Data Preprocessing
- Added unique ID column
- Handled missing values using Imputer
- Removed unnecessary columns

---

## Exploratory Data Analysis (EDA)
- Aggregations using groupBy
- Mean calculations for all numerical columns
- Insights based on ocean_proximity

## Feature Engineering
- Created new feature using UDF:
- df.withColumn('total_rooms_squared', squared_udf('total_rooms'))

---

## Train-Test Split
- train, test = df.randomSplit([0.7, 0.3])

---

## Feature Transformation
### Numerical Processing
- VectorAssembler → Combine features
- StandardScaler → Normalize features
## Categorical Processing
- StringIndexer → Convert categories to index
- OneHotEncoder → Encode categorical variables

---

## Model Building
- Used Linear Regression (Spark MLlib)

---

## Predictions
Generated predictions for both train & test datasets

---

##Model Evaluation
- Used RegressionMetrics:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

---

## Key Learnings
- Built scalable ML pipelines using PySpark
- Learned distributed data processing
- Applied feature engineering using UDFs
- Understood MLlib workflow end-to-end

## Future Improvements
- Try advanced models (Random Forest, GBT)
- Hyperparameter tuning
- Deploy model using Streamlit / Flask
- Add dashboard visualization
