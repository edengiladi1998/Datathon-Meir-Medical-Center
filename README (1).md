# Datathon Meir Hospital – Staff Planning and Task Forecasting

This project was developed as part of the Afeka College Datathon, using real-world task data from Meir Medical Center. The goal was to analyze and forecast hospital task loads in order to improve staff allocation and workload management.

## Project Objective

Hospitals face unpredictable workloads that can lead to staff shortages during peak hours or inefficient resource usage during off-peak times. Our goal was to:

- Analyze historical task data (blood tests, cleaning, physician visits, etc.)
- Predict daily and hourly task volumes using machine learning
- Provide staffing recommendations based on forecasted workload
- Support more efficient and data-driven workforce planning in hospitals

## Dataset

The dataset was provided by Meir Medical Center and includes thousands of rows, with columns such as:
- `timestamp`: Date and time of request  
- `department`: Hospital department  
- `room`: Patient room  
- `requirement`: Type of task  
- `status`: Request status  

The data spans several months and was cleaned and processed using Python (Pandas, matplotlib, scikit-learn, XGBoost).

## Main Analyses & Models

### 1. Task Analysis & Visualization
- Breakdown of task types by department and time
- Identification of departments with the highest task failure rates (e.g., partial/not_required)
- Heatmaps and trend graphs to visualize peak hours

### 2. Forecasting Model (XGBoost)
- Predicts future task volumes using:
  - Task type
  - Day of the week
  - Is weekend
  - Lag features (previous day requests)
- Achieved high accuracy with R² ≈ 0.87–0.91 on test sets

### 3. 7-Day Prediction Model
- Generates predictions for each department+task pair
- Supports operational planning a week ahead

### 4. Staffing Recommendation Engine
- Calculates recommended staff count based on task volume (e.g., 1 staff per 20 tasks/hour)
- Visualized per hour to optimize shift scheduling

## Sample Visualizations

- Actual vs Predicted Task Volume  
- Error Distribution (Overfitting Check)  
- Hourly Load Heatmap  
- Recommended Staffing per Hour

*(see `/images` folder or project report for graphs)*

## Team

This project was developed by a multidisciplinary team of students from Afeka College, combining knowledge in data science, engineering, and healthcare management.

## Project Structure

```bash
├── data/                # Raw and processed datasets
├── notebooks/           # Jupyter Notebooks with full analysis
├── models/              # Trained ML models (optional)
├── images/              # Visualizations and plots
├── main.py              # Core scripts (optional)
└── README.md            # Project documentation
