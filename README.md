# Air Quality Analysis & AQI Prediction

## Project Overview

This project analyzes air quality data and predicts the Air Quality Index (AQI) using Machine Learning.

The project includes:

* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Machine Learning regression
* Model comparison and evaluation
* AQI prediction
* Interactive Streamlit web application
* Power BI dashboard

## Live Demo

**Streamlit App:**
https://nti-final-project-eatoegwgs44mmxlsqo7bkn.streamlit.app/

## Dataset

The project uses the Taiwan Air Quality Dataset (2016–2024) from Kaggle.

The dataset is downloaded automatically when `train_model.ipynb` is executed using KaggleHub.

## Data Preprocessing

The preprocessing pipeline includes:

* Removing unnecessary columns
* Cleaning column names
* Converting data types
* Handling missing values
* Removing negative measurements
* Handling outliers using the IQR method
* Preparing numerical features for Machine Learning

## Machine Learning

Two regression models were implemented:

* Linear Regression
* Decision Tree Regressor

The models were evaluated using:

* MAE
* RMSE
* R² Score

The best-performing model is automatically selected and saved as:

```text
models/best_model.pkl
```

## Streamlit Application

The application provides:

### 1. EDA Dashboard

Displays:

* Average AQI
* Average PM2.5
* Average CO
* AQI trends over time
* AQI by county
* Monitoring station analysis

### 2. AQI Prediction

Users can enter environmental and pollutant measurements and obtain a predicted AQI value.

The application also displays the corresponding AQI category.

### 3. Model Evaluation

Displays:

* Model comparison
* MAE
* RMSE
* R² Score
* Actual vs. Predicted AQI
* Prediction error analysis
* Residual distribution

## Cloud Dataset Optimization

The complete cleaned dataset is large and contains approximately 5 million records.

For the deployed Streamlit application, a random sample of **500,000 records** is used in:

```text
models/app_air_quality.csv
```

This optimization was necessary to reduce memory usage and improve application stability in the cloud environment.

The original complete dataset is still used for the full project workflow and local execution.

## Running the Project Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Darin-Za/NTI-Final-Project.git
cd NTI-Final-Project
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Generate the Required Files

Open:

```text
train_model.ipynb
```

Run all cells from beginning to end.

The notebook automatically:

1. Downloads the dataset using KaggleHub.
2. Cleans and preprocesses the data.
3. Creates the required files inside the `models` folder.
4. Trains the Machine Learning models.
5. Selects the best model.
6. Saves the trained model and evaluation results.

### 4. Run the Streamlit Application

After completing the notebook, run:

```bash
streamlit run app.py
```

The application will open locally at:

```text
http://localhost:8501
```


## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Joblib
* Streamlit
* KaggleHub
* Power BI
* Git & GitHub
* Git LFS

## How the System Works

```text
Kaggle Dataset
      ↓
Data Cleaning & Preprocessing
      ↓
Feature Preparation
      ↓
Machine Learning Models
      ↓
Model Evaluation
      ↓
Best Model Selection
      ↓
Streamlit Application
      ↓
AQI Prediction & Visualization
```

## Project Goal

The main goal of this project is to develop an interactive system capable of analyzing air quality data and predicting AQI using Machine Learning models.

## Repository

GitHub Repository:

https://github.com/Darin-Za/NTI-Final-Project
