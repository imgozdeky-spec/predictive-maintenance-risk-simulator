# AI-Based Predictive Maintenance and Risk Simulator

## Project Overview

This project presents an AI-assisted predictive maintenance and risk analysis system designed to support data-driven maintenance decisions.

The system analyzes equipment sensor data, estimates failure risk, classifies equipment risk levels, and evaluates alternative maintenance scenarios based on expected operational and financial impacts.

The project combines machine learning, predictive maintenance, risk analysis, simulation, and industrial engineering methods.

## Project Objectives

* Analyze equipment sensor data
* Identify abnormal equipment behavior
* Estimate equipment failure probability
* Calculate equipment risk scores
* Classify maintenance risk levels
* Simulate alternative maintenance scenarios
* Estimate potential operational and financial impacts
* Support data-driven maintenance planning

## System Architecture

```text
Sensor Data
     │
     ▼
Data Analysis
     │
     ▼
Failure Prediction Model
     │
     ▼
Risk Scoring
     │
     ▼
Maintenance Scenario Simulation
     │
     ▼
Decision Support
```

## Input Data

The system uses simulated equipment data containing:

* Temperature
* Vibration
* Pressure
* Energy consumption
* Operating hours
* Maintenance history
* Previous failures
* Maintenance duration

The dataset is created for demonstration purposes and does not represent real company or defense-industry data.

## Machine Learning

A Random Forest classification model is used as an example machine learning approach for estimating equipment failure risk.

The model uses sensor and operational variables including:

* Temperature
* Vibration
* Pressure
* Energy consumption
* Operating hours

The output is an estimated failure probability.

## Risk Scoring

In addition to the machine learning prediction, a weighted risk score is calculated using selected equipment indicators.

The system classifies equipment into:

* Low Risk
* Medium Risk
* High Risk
* Critical Risk

This provides an interpretable layer for maintenance decision support.

## Maintenance Scenario Simulation

The project evaluates different maintenance strategies, such as:

1. Immediate maintenance
2. Maintenance after 12 hours
3. Maintenance after 24 hours

Each scenario considers factors such as:

* Maintenance cost
* Maintenance duration
* Expected production loss
* Potential failure cost
* Delay-related risk

The objective is to support comparison of alternative maintenance decisions.

## Decision Support

The decision engine converts analytical outputs into an interpretable maintenance recommendation.

The system can identify whether equipment should:

* Continue to be monitored
* Be scheduled for maintenance
* Be considered for immediate maintenance

The recommendation is based on calculated risk and scenario information rather than a single sensor measurement.

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Random Forest
* Statistical Analysis
* Predictive Maintenance
* Risk Analysis
* Scenario Simulation

## Project Structure

```text
predictive-maintenance-risk-simulator/
│
├── data/
│   ├── sensor_data.csv
│   └── maintenance_history.csv
│
├── models/
│
├── outputs/
│   ├── charts/
│   └── reports/
│
├── src/
│   ├── data_analysis.py
│   ├── failure_prediction.py
│   ├── risk_scoring.py
│   ├── scenario_simulator.py
│   └── decision_engine.py
│
├── notebooks/
│
├── README.md
└── requirements.txt
```

## Example Decision Flow

```text
High Temperature
       +
High Vibration
       +
High Energy Consumption
       ↓
Increased Failure Risk
       ↓
Risk Classification
       ↓
Maintenance Scenario Analysis
       ↓
Estimated Cost and Operational Impact
       ↓
Maintenance Decision Support
```

## Assumptions and Limitations

This project uses simulated data and simplified assumptions for demonstration purposes.

The current version is not intended to make real-world safety-critical maintenance decisions.

For a real industrial implementation, the system would require validated historical failure data, domain-specific thresholds, model validation, real maintenance records, and integration with operational systems.

## Future Improvements

Potential future developments include:

* Real-world time-series datasets
* More advanced time-series forecasting
* Anomaly detection
* XGBoost or other machine learning models
* Model explainability using SHAP
* Remaining Useful Life (RUL) prediction
* Real-time sensor monitoring
* Dynamic maintenance scheduling
* Multi-equipment optimization
* Production planning integration
* Interactive dashboard
* Digital twin integration
* Vehicle and mission-level operational impact analysis

## Purpose

This project was developed as an industrial engineering and artificial intelligence portfolio project to demonstrate the application of machine learning and decision-support techniques to predictive maintenance and operational risk management.
