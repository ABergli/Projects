# Benchmarking Maintenance Efficiency Using Machine Learning: A Case Study at Statkraft's Hydropower Plants

This repository contains the code and documentation for a Bachelor's project focused on developing a Machine Learning (ML) solution for benchmarking the maintenance efficiency of Scandinavian hydropower plants, with a specific focus on Statkraft AS.

## Important Note: Intellectual Property

**Please note that the Machine Learning code developed as part of this project is proprietary to Statkraft AS and cannot be publicly disclosed in this repository.** This README.md provides a comprehensive overview of the project's methodology, results, and deliverables, but the underlying code remains confidential.

---

## Project Overview

This project addresses the complex challenge of assessing and improving maintenance efficiency in hydropower plants. By leveraging historical maintenance and operational data, we developed an ML-based "Maintenance-Based Efficiency" (MBE) score to provide Statkraft with a robust tool for benchmarking plant performance, identifying inefficiencies, and promoting best practices across their assets.

### Problem Statement

Hydropower plant operations are inherently complex, and a lack of established efficiency scores makes it difficult to benchmark performance and identify areas for improvement in maintenance. This project aimed to create a quantifiable MBE score to bridge this gap.

### Primary Goals

1.  **Analyze Historical Maintenance Data:** Conduct a maintenance-based analysis of historical data from 2021-2024.
2.  **Develop an ML Model for Efficiency Quantification:** Create a machine learning model capable of quantifying the efficiency of hydropower plants based on their maintenance performance.
3.  **Provide a Benchmarking Tool:** Deliver a tool that allows for the comparison of maintenance-based efficiency across different hydropower plants, business groups, and regions.
4.  **Inform Strategic Decisions:** Offer insights that help identify underperforming plants and areas of inefficiency, enabling data-driven maintenance management.

---

## Methodology

Our approach involved a structured Machine Learning pipeline, from data collection and preprocessing to model training, validation, and deployment.

### Data

Due to the absence of explicit "ground truth" efficiency scores in real-world data, a significant part of our methodology involved:
* **Synthetic Data Generation:** We created a synthetic dataset, grounded in real-world operational data (averaged from 2021-2023), with known efficiency relationships (P-values from 5% to 95%). This allowed us to train supervised learning models effectively.
* **Data Preprocessing:** This included extensive data cleaning, handling missing values, standardizing identifiers, transforming date formats, capturing downtime days, and feature engineering to create meaningful variables.

### Machine Learning Models

We evaluated four non-linear regression models for predicting the MBE score, representing both deep learning and ensemble approaches:

* **XGBoost Regressor:** Known for its efficiency, scalability, and accuracy in structured data problems.
* **Random Forest Regressor:** An ensemble method that builds multiple decision trees to improve predictive accuracy and control overfitting.
* **AutoEncoder + Regressor:** A hybrid model combining an unsupervised autoencoder for compressed representations with a supervised regression model for predictions.
* **Multi-Layer Perceptron (MLP) Regressor:** A feedforward neural network capable of modeling complex, non-linear relationships.

### Model Evaluation and Selection

Models were trained on the synthetic dataset, and hyperparameters were tuned using `RandomizedSearchCV` with 50 trials and 10-fold cross-validation. Performance was evaluated using:
* **Root Mean Square Error (RMSE)**
* **Mean Absolute Error (MAE)**
* **Coefficient of Determination ($R^2$)**

**Random Forest Regressor** emerged as the best-performing model, demonstrating strong predictive accuracy ($R^2 = 0.998927$, RMSE $= 0.956387$, MAE $= 0.190836$ on the synthetic hold-out set) and acceptable generalization ability.

---

## Solution & Deliverables

The project delivered a comprehensive solution comprising:

1.  **Machine Learning Model Code (Proprietary to Statkraft):** Fully documented Jupyter notebooks containing the complete model architectures (including synthetic data generation). The trained Random Forest model predicts time-series efficiency outputs for each power plant and a single aggregate efficiency score. **While the code itself cannot be shared, this repository describes its functionalities and the underlying methodologies.**
2.  **Power BI Dashboards for Historical Maintenance Analysis:** An interactive tool allowing in-depth analysis of maintenance expenditures, production levels, and downtime across various hierarchical levels (country/region, asset class, individual plants) from 2021-2024. This tool helps identify cost drivers, trends, and correlations, supporting data-driven maintenance planning.
3.  **Power BI Efficiency Score Benchmarking Tool:** Visualizes and categorizes predicted efficiency scores, enabling users to drill down from high-level overviews to individual plants. This tool is crucial for identifying underperforming or high-performing assets, guiding targeted interventions, and fostering performance excellence across the organization.

---

## Technologies Used

* **Python:** Primary programming language for ML model development.
* **Libraries:** `xgboost`, `scikit-learn`, `tensorflow`/`keras` (for AutoEncoder and MLP), `pandas`, `numpy`, `matplotlib`, `seaborn`.
* **Microsoft Power BI:** For interactive data visualization and dashboard creation.
* **SAP Analysis for Microsoft Office:** For data extraction from SAP systems.
* **Visual Studio Code (VS Code) with DataWrangler extension:** Primary IDE for development and exploratory data analysis.
* **Microsoft Teams:** For internal and external communication and collaboration.
* **GitLab:** For version control and shared workspace.

---

## Key Outcomes

* Successfully developed a novel MBE score for hydropower plants.
* Demonstrated the effectiveness of ML models, particularly Random Forest, in predicting maintenance efficiency using synthetic data.
* Provided practical Power BI tools for deep historical analysis and real-time benchmarking of plant performance.
* Laid a solid foundation for Statkraft to integrate predictive analytics into their maintenance strategies.

---

## Future Work

Several areas are identified for future improvements to enhance the model's robustness, accuracy, and practical applicability:

* **Enrich Feature Set:** Incorporate more technical details about plants (e.g., number of turbines/generators, bearing types, sensor types, environmental data like water hardness, silt amount, head, water volume, weather patterns).
* **SCADA Integration:** Integrate with SCADA systems for real-time prediction and early warning capabilities based on live operational sensor data.
* **Refine Synthetic Data Complexity:** Improve the realism and nuance of synthetic data to better capture real-world operational conditions.
* **Further Analysis:** Examine predicted efficiency scores in relation to factors like turbine type, equipment age, and overall facility age to understand their impact on maintenance needs and efficiency.

---

**Authors:**

* Andreas Manalo Bergli
* Davyd Lebedovskyi
* Richard Hansen
* Somjate Srirabai

**Institution:** Kristiania University of Applied Sciences, Oslo, Norway
**Client:** Statkraft
**Date:** May 15, 2025
