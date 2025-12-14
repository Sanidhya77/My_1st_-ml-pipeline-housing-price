# My_1st_-ml-pipeline-housing-price
End-to-end machine learning pipeline for housing price prediction using scikit-learn, including preprocessing, training, model persistence, and inference.
# Housing Price ML Pipeline

This repository demonstrates a **complete end-to-end machine learning pipeline** for predicting housing prices using **scikit-learn**.

The project focuses on **correct ML structure**, not flashy models:
- Data preprocessing using pipelines
- Stratified train-test split
- Model training
- Model and pipeline persistence
- Reproducible inference

This is intended as a **foundational ML project** and a reference for building clean ML workflows.

---

## 📂 Project Structure

├── housing.csv # Original dataset
├── input.csv # Saved test data for inference
├── predictions.csv # Model predictions
├── model.pkl # Trained RandomForest model
├── pipeline.pkl # Preprocessing pipeline
├── main.py # Training & inference script
├── README.md


---

## 🧠 Key Concepts Covered

- Stratified sampling based on income categories
- Numerical and categorical preprocessing using `Pipeline` and `ColumnTransformer`
- Median imputation and feature scaling
- One-hot encoding for categorical variables
- Random Forest regression
- Model & pipeline persistence using `joblib`
- Batch inference on unseen data

---

## ⚙️ How It Works

### 1. Training Phase
- Loads housing dataset
- Creates income-based strata
- Splits data using `StratifiedShuffleSplit`
- Trains preprocessing pipeline
- Trains `RandomForestRegressor`
- Saves model and pipeline to disk

### 2. Inference Phase
- Loads saved model and pipeline
- Transforms unseen input data
- Generates predictions
- Saves results to `predictions.csv`

The training step runs **only if the model does not already exist**.

---

## ▶️ How to Run

### Install dependencies
```bash



