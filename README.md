# 🔧 Predictive Maintenance for Industrial Equipment

## 📄 Project Overview

This project aims to build a **predictive maintenance system** for industrial machinery. By analyzing key factors that contribute to equipment failures, this model helps forecast potential failures and provides actionable insights to **optimize maintenance schedules**, thereby reducing downtime and improving operational efficiency.

## 🎯 Objectives

- 🔍 **Understand** the factors contributing to equipment failure.
- 🤖 **Build** a predictive model to forecast machine failures.
- 💡 **Provide insights** to optimize maintenance schedules and minimize downtime.

## 📊 Dataset Description

The dataset consists of operational and environmental data from industrial machines with the following key columns:

| Column Name           | Description                                                   |
|-----------------------|---------------------------------------------------------------|
| **Machine ID**         | Unique identifier for each machine.                           |
| **Timestamp**          | Date and time of the data recording.                          |
| **Temperature**        | Operating temperature of the machine (°C).                    |
| **Pressure**           | Pressure inside the machine (PSI).                            |
| **Vibration**          | Vibration level of the machine (mm/s).                        |
| **Operational Hours**  | Total hours the machine has been in operation.                |
| **Maintenance History**| Binary indicator (Yes/No) if maintenance was performed.       |
| **Failure**            | Binary indicator (Yes/No) if the machine has failed.          |

## 🛠️ Data Processing

During preprocessing, the following steps were performed:

1. **Data Cleaning**: Removed null values, duplicate rows, and standardized the `Timestamp` column.
2. **Feature Engineering**: 
   - Grouped by `Machine ID` to calculate average temperature.
   - Created cumulative vibration and operational hours until failure.
3. **Label Encoding**: Converted categorical features like `Maintenance History` and `Failure` to numerical values.

## 📈 Exploratory Data Analysis (EDA)

Exploratory data analysis was performed to gain insights into the dataset:
- **Histograms**: For understanding the distribution of numerical features.
- **Correlation Matrix**: Visualized correlations between features.
- **Boxplots & Violin Plots**: Identified outliers and feature distributions.
  
*(Visualizations can be found in the project notebooks.)*

## 🧠 Machine Learning Models

Several machine learning models were tested to predict failures:

| Model                     | Accuracy | Precision | Recall | F1 Score |
|----------------------------|----------|-----------|--------|----------|
| **Logistic Regression**     | 0.49     | 0.56      | 0.44   | 0.49     |
| **Random Forest Classifier**| 0.52     | 0.57      | 0.59   | 0.58     |
| **Gradient Boosting Classifier**| 0.47 | 0.53      | 0.46   | 0.49     |
| **Support Vector Machine**  | 0.44     | 0.50      | 0.46   | 0.48     |
| **K-Nearest Neighbors (KNN)**| **0.58** | **0.63** | **0.59** | **0.61** |

**K-Nearest Neighbors (KNN)** achieved the best performance and was selected as the final model.

## 🧾 Prediction Results

- **Scenario 1**:  
   - Predicted Class: **No Failure**
   - Recommended Action: Operate normally, but monitor closely.
   - Probability of Failure: 40%
   - Probability of No Failure: 60%

- **Scenario 2**:  
   - Predicted Class: **Failure**
   - Recommended Action: Schedule maintenance soon.
   - Probability of Failure: 60%
   - Probability of No Failure: 40%

## 🚀 Conclusion

The predictive maintenance model helps forecast failures at an early stage, enabling companies to:
- 📅 **Optimize maintenance schedules** to prevent machine failures.
- ⏱️ **Reduce unplanned downtime** by addressing maintenance proactively.
- 💡 **Enhance operational efficiency** by monitoring critical machines.

## 🗂️ Repository Structure

