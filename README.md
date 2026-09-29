# Predictive Maintenance & Risk Simulator

An AI-assisted predictive maintenance and risk analysis project designed to estimate equipment failure risk, evaluate maintenance scenarios, and support data-driven maintenance decisions.

> **Note:** This project uses simulated equipment data for educational and portfolio purposes. It is not intended for real-world safety-critical decisions.

---

## Project Overview

Unplanned equipment failures can cause production delays, unexpected maintenance costs, and operational disruptions.

This project combines **machine learning, risk scoring, and maintenance scenario simulation** to create a decision-support framework for industrial equipment.

The system analyzes:

* Temperature
* Vibration
* Pressure
* Energy consumption
* Operating hours
* Maintenance history

Based on these variables, the system estimates failure probability, calculates an operational risk score, and compares different maintenance strategies.

---

## Project Objectives

* Analyze industrial equipment sensor data
* Identify potential failure conditions
* Estimate equipment failure probability using machine learning
* Calculate interpretable equipment risk scores
* Compare different maintenance scenarios
* Estimate potential maintenance and production-loss costs
* Provide a simple decision-support mechanism
* Demonstrate how predictive analytics can support industrial engineering decisions

---

## System Architecture

```text
Sensor Data
     │
     ▼
Data Analysis
     │
     ├───────────────┐
     ▼               ▼
Failure Prediction  Risk Scoring
     │               │
     └───────┬───────┘
             ▼
   Maintenance Scenarios
             │
             ▼
      Cost Estimation
             │
             ▼
     Decision Support
```

---

## Input Data

The project uses simulated sensor and maintenance data.

### Sensor Variables

| Variable           | Description                     |
| ------------------ | ------------------------------- |
| temperature        | Equipment operating temperature |
| vibration          | Equipment vibration level       |
| pressure           | Operating pressure              |
| energy_consumption | Energy consumption              |
| operating_hours    | Total operating hours           |
| equipment_id       | Equipment identifier            |
| timestamp          | Measurement timestamp           |

### Maintenance Variables

| Variable                   | Description                     |
| -------------------------- | ------------------------------- |
| last_maintenance_days      | Days since the last maintenance |
| previous_failures          | Number of previous failures     |
| maintenance_duration_hours | Estimated maintenance duration  |

---

## Machine Learning

A **Random Forest Classifier** is used as an example machine learning model for estimating failure probability.

The model uses:

* Temperature
* Vibration
* Pressure
* Energy consumption
* Operating hours

The resulting probability can be used as an input for the maintenance decision-support process.

---

## Risk Scoring

In addition to the machine learning component, an interpretable risk score is calculated.

The current scoring model combines:

```text
Temperature Risk      → 40%
Vibration Risk        → 40%
Energy Consumption    → 20%
```

The resulting score is classified into four levels:

| Risk Score  | Risk Level |
| ----------- | ---------- |
| < 0.30      | Low        |
| 0.30 – 0.49 | Medium     |
| 0.50 – 0.74 | High       |
| ≥ 0.75      | Critical   |

This provides an easily interpretable representation of equipment condition.

---

## Maintenance Scenario Simulation

The project compares different maintenance timing strategies:

1. Immediate Maintenance
2. Maintenance After 12 Hours
3. Maintenance After 24 Hours

Each scenario considers:

* Maintenance cost
* Maintenance duration
* Production loss
* Expected failure cost
* Delay-related risk

The objective is to demonstrate how maintenance timing can affect expected operational cost.

---

## Decision Support

The decision engine uses failure probability and estimated cost to generate a simple maintenance recommendation.

Example decision flow:

```text
Failure Probability
        │
        ▼
 ┌─────────────────┐
 │   Risk Level    │
 └────────┬────────┘
          │
          ▼
Maintenance Scenario
          │
          ▼
Estimated Cost
          │
          ▼
Decision Support
```

---

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Random Forest
* CSV Data Processing
* Predictive Analytics
* Risk Analysis

---

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
│   └── risk_scoring.py
│
├── notebooks/
│
├── requirements.txt
└── README.md
```

---

## Example Use Case

Consider an industrial machine showing:

* Increasing temperature
* Increasing vibration
* Increasing energy consumption

The system can identify the changing operating conditions, estimate failure probability, calculate a risk level, and compare the expected cost of different maintenance timings.

This creates a simplified **predictive maintenance decision-support workflow**.

---

## Industrial Engineering Perspective

The project connects machine learning with industrial engineering concepts such as:

* Maintenance management
* Production loss analysis
* Cost optimization
* Risk management
* Equipment utilization
* Decision support
* Data-driven operations

The goal is not only to predict a possible failure, but also to investigate **what the operational and economic consequences of different maintenance decisions could be**.

---

## Assumptions & Limitations

This is a portfolio and educational project based on simulated data.

The current implementation has several limitations:

* The dataset is small and simulated.
* Failure labels are generated using predefined threshold rules.
* The Random Forest model is therefore a demonstration rather than a validated production model.
* Maintenance costs are assumed values.
* Production-loss costs are assumed values.
* Real industrial equipment requires domain-specific sensor thresholds and historical failure data.

Therefore, the results should not be interpreted as predictions for real industrial equipment.

---

## Future Improvements

Possible future developments include:

* Real industrial sensor datasets
* Time-series forecasting
* Anomaly detection
* XGBoost-based prediction
* SHAP-based model explainability
* Remaining Useful Life (RUL) prediction
* Real-time sensor monitoring
* Automated maintenance scheduling
* Multi-equipment optimization
* Integration with production planning
* Digital twin simulation
* Interactive dashboard development
* Maintenance optimization under production constraints

---

## Portfolio Purpose

This project demonstrates the integration of:

**Industrial Engineering + Data Analytics + Machine Learning + Predictive Maintenance + Decision Support**

It was developed as a portfolio project to explore how AI-based analytical methods can support industrial operations and maintenance planning.
