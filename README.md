# Passenger Flow Forecasting Using AI Models

This repository contains the implementation of passenger flow data preprocessing and forecasting models for urban public transport demand prediction.

The project focuses on transforming raw passenger flow logs into structured time-series data and training machine learning models to forecast passenger demand.

---

## Project Objective

Efficient public transportation systems require accurate passenger demand forecasting.  
This project investigates forecasting approaches using historical passenger flow data and machine learning techniques.

The forecasting task is defined as:

- **24-hour ahead forecasting**
- **96 time steps**
- **15-minute time intervals**

---

## Data Processing Pipeline

The preprocessing pipeline includes several steps to prepare the data for forecasting models:

- Parsing and sorting timestamped passenger flow logs
- Converting cumulative counters into interval passenger counts
- Aggregating observations into 15-minute time bins
- Handling missing intervals using zero-imputation
- Detecting and controlling extreme outliers
- Generating lag features and rolling statistics
- Adding calendar-based features such as hour and weekday indicators

These steps ensure that the dataset is consistent and suitable for time-series forecasting.

---

## Forecasting Models

This project evaluates several baseline forecasting methods together with an advanced machine learning model.

### Baseline Models

- Naive Forecast
- Seasonal Naive (Daily Seasonality)
- Weekly Seasonal Naive
- Moving Average

### Machine Learning Model

- **OIKAN (Optimized Interpretable Kolmogorov-Arnold Network)**

---

## Validation Strategy

Model performance is evaluated using **walk-forward validation**, also known as **rolling origin evaluation**.

This approach simulates real forecasting scenarios by repeatedly training the model on historical data and predicting future horizons.

---

## Evaluation Metrics

The forecasting models are compared using standard regression error metrics:

- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**
- **Symmetric Mean Absolute Percentage Error (sMAPE)**

## Repository Structure

passenger-flow-forecasting
│
├── forecasting_model.ipynb   # Main forecasting implementation (Google Colab)
└── README.md


The notebook includes the full workflow:

- Data preprocessing
- Feature engineering
- Model training
- Forecast generation
- Evaluation and visualization

---

## Authors

**Mohammad Aslam Khorami**  
Computer Science Student  
Astana IT University  
Astana, Kazakhstan  

Email: 243084@astanait.edu.kz

---

**Sayed Nasibullah Turan**  
Computer Science Student  
Astana IT University  
Astana, Kazakhstan  

Email: 243100@astanait.edu.kz

---

## Advisor

**N. Khaimuldin**  
Senior Lecturer  
Astana IT University  
Astana, Kazakhstan  

Email: n.khaimuldin@astanait.edu.kz

---

## Research Project

Passenger Flow Data Collection and Preprocessing for AI-Based Load Forecasting

Astana IT University  
2026
