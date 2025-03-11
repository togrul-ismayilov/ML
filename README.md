# Car Price Anomaly Detection using Machine Learning

## Overview

This project aims to identify cars listed at a price lower than the market value using machine learning techniques. The dataset was scraped from Turbo.az, a popular car sales website, and stored in a MySQL database. The project involves data preprocessing, feature engineering, model training, and evaluation using XGBoost.

## Dataset

The dataset consists of various attributes related to car listings, including:

- Make
- Model
- Year
- Engine
- Price
- Mileage
- Fuel Type
- Transmission
- Drive Type
- Features (e.g., ABS, sunroof, leather seats, etc.)

### Data Preprocessing

Several preprocessing steps were applied to the dataset:

- Dropped unnecessary columns such as `ad_id`, `url`, `seats_count`, `prior_owners_count`, `vin`, `updated`, `number_of_views`, `price_original`, and `product_extras`.
- One-hot encoded categorical features, especially `product_extras`, which contained multiple features in a comma-separated format.
- Retained `Make`, `Model`, `Year`, and `Engine` as separate features instead of concatenating them.

## Model Selection

- **XGBoost**: A gradient boosting algorithm known for its performance in structured data problems.

## Implementation

The project is implemented in a Jupyter Notebook (`Turboaz_model.ipynb`) and consists of:

1. Data Loading
2. Preprocessing
3. Feature Engineering
4. Model Training & Evaluation

## Results

The trained models were evaluated based on metrics such as:

- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)
- R-squared (R²) Score

The best-performing model was used to identify listings significantly lower than the predicted price, flagging them as potential bargains or anomalies.

## Requirements

To run this project, install the necessary dependencies:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn sqlalchemy wordcloud category_encoders
```

## Usage

1. Clone the repository:

```bash
git clone https://github.com/togrul-ismayilov/ML/turboaz-ml-project.git
```

2. Navigate to the project folder and open the Jupyter Notebook:

```bash
jupyter notebook Turboaz_model.ipynb
```

3. Run the cells to execute the entire pipeline.
