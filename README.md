# Advanced Supply Chain Resilience and Disruption Modeling

## Enterprise Grade Predictive and Prescriptive Analytics System

---

## Project Overview

This project implements a comprehensive end to end supply chain analytics system designed to analyze, predict, and mitigate delivery delays and operational risks in a global supply chain. The system integrates data engineering, machine learning, network science, optimization, risk simulation, and scenario analysis into a single reproducible pipeline.

The objective of the project is not limited to delay prediction. It aims to explain delay drivers, quantify uncertainty, evaluate structural vulnerabilities, and recommend actionable strategies for improving supply chain resilience under normal and disrupted conditions.

---

## Key Objectives

- Predict shipment delays using advanced machine learning models  
- Engineer temporal, structural, and risk based features  
- Model supply chain structure using graph theory  
- Quantify inventory and service level risk using Monte Carlo simulation  
- Optimize service levels under competing cost and risk objectives  
- Evaluate resilience under multiple disruption scenarios  
- Generate executive level dashboards and reproducible reports  

---

## Repository Structure

├── README.md
├── notebooks/
│ └── SCRM.ipynb
├── data/
│ ├── supply_chain_advanced_data.csv
│ ├── feature_importance.csv
│ ├── scenario_analysis.csv
│ ├── optimized_routes.csv
│ └── supplier_analysis.csv
├── outputs/
│ ├── executive_dashboard.png
│ ├── network_topology.png
│ ├── monte_carlo_simulation.png
│ └── supply_chain_full_execution_report.pdf
---

## Dataset Description

### supply_chain_advanced_data.csv

The primary dataset consists of 1,000 historical shipment records spanning the period from January 2023 to December 2023. Each record represents a shipment with operational, temporal, cost, supplier, and geographic attributes.

### Key Attributes

- Order and delivery dates  
- Shipment quantity and value  
- Transport cost and shipping mode  
- Supplier and destination identifiers  
- Delivery outcome indicator  

---

## Engineered Features

The project derives a rich set of advanced features, including:

- Rolling delay rates over 30 and 90 day windows  
- Exponential moving average of delays  
- Route volatility metrics  
- Supplier, country, and shipping mode risk scores  
- Seasonal indicators such as month, quarter, peak season, and winter  
- Cost benefit and value quantity ratios  

---

## Methodology Overview

The analytical pipeline is divided into four major phases.

---

## Phase 1 Advanced Data Engineering and Network Analysis

This phase focuses on preparing the dataset and modeling the structural relationships within the supply chain.

### Key Steps

- Data cleaning and preprocessing  
- Temporal feature extraction  
- Risk score computation for suppliers, countries, and transport modes  
- Construction of a directed supply chain network  

The supply chain is modeled as a graph where nodes represent suppliers, warehouses, and destinations, and edges represent shipment flows. Network metrics are later used to assess dependency concentration and structural risk.

### Output

- network_topology.png  

---

## Phase 2 Predictive Modeling and Forecasting

### Machine Learning Model

A gradient boosted decision tree model using XGBoost is trained to classify shipments as on time or delayed.

### Key Characteristics

- Hyperparameter optimization using GridSearchCV  
- Three fold cross validation  
- ROC AUC as the primary evaluation metric  
- Explicit handling of class imbalance  

### Test Set Performance

- ROC AUC approximately 0.76  
- Balanced precision and recall across both classes  

---

### Model Interpretability

Feature importance analysis identifies the most influential predictors of delay, including rolling delay rates, supplier risk, route volatility, and scheduling characteristics.

### Output

- feature_importance.csv  

---

### Time Series Forecasting

An ARIMA model is used to forecast the aggregate delay rate over a 30 day horizon, providing insight into near term operational trends and stability.

---

## Phase 3 Optimization Risk Simulation and Scenario Analysis

### Multi Objective Optimization

A constrained optimization framework is used to determine optimal service levels across high value routes. The objective balances service reliability against cost and risk exposure.

### Output

- optimized_routes.csv  

Routes are categorized into service level tiers such as enhanced and standard based on optimization results.

---

### Monte Carlo Risk Simulation

Inventory risk is quantified using Monte Carlo simulation with 10,000 iterations per route.

### Metrics Computed

- Stockout probability  
- Average monthly holding cost  
- Value at Risk at the 95 percent confidence level  

This approach captures uncertainty and tail risk that deterministic models fail to represent.

### Output

- monte_carlo_simulation.png  

---

### Scenario Analysis

The system evaluates supply chain performance under multiple disruption scenarios.

### Scenarios Evaluated

- Baseline  
- Mild disruption  
- Moderate disruption  
- Severe disruption  
- Black swan event  

Each scenario is assessed in terms of delay, transport cost, revenue impact, and total financial exposure.

### Output

- scenario_analysis.csv  

The analysis also estimates risk premiums and recommends contingency budgets.

---

### Supplier Diversification Strategy

Supplier concentration is evaluated using revenue share and the Herfindahl Hirschman Index. High dependency and high delay suppliers are flagged for diversification.

### Output

- supplier_analysis.csv  

---

## Phase 4 Advanced Visualization and Reporting

### Executive Dashboard

A consolidated executive dashboard is generated to summarize operational performance, risk drivers, and scenario impacts. The dashboard is intended for senior leadership and decision makers.

### Output

- executive_dashboard.png  

---

## Full Execution Report

### supply_chain_full_execution_report.pdf

This document captures the complete execution of the pipeline, including:

- Phase wise logs  
- Model performance summaries  
- Optimization and simulation outputs  
- Strategic recommendations  
- Embedded visual outputs  

The report serves as a reproducible and audit ready artifact.

---

## Exported Artifacts Summary

- supply_chain_advanced_data.csv  
- feature_importance.csv  
- optimized_routes.csv  
- scenario_analysis.csv  
- supplier_analysis.csv  
- executive_dashboard.png  
- network_topology.png  
- monte_carlo_simulation.png  
- supply_chain_full_execution_report.pdf  

---

## How to Run the Project

1. Open the notebook `notebooks/SCRM.ipynb`  
2. Install required Python libraries  
   - pandas, numpy, matplotlib  
   - scikit learn, xgboost  
   - networkx, statsmodels  
3. Run all cells sequentially  
4. Outputs are automatically saved to the outputs directory  

---

## Intended Use Cases

- Supply chain risk and resilience assessment  
- Logistics and operations strategy planning  
- Academic research and coursework  
- Analytics and machine learning portfolios  
- Consulting case studies and demonstrations  

---

## Key Takeaway

This project demonstrates how predictive modeling, network science, optimization, and risk simulation can be integrated into a unified decision support system for complex supply chains. It emphasizes interpretability, uncertainty quantification, and actionable insights rather than prediction alone.
