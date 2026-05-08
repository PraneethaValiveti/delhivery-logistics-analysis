# delhivery-logistics-analysis
End-to-end logistics and delivery data analysis project using Python, EDA, feature engineering, hypothesis testing, aggregation, and business insights generation.
# Delhivery Logistics Data Analysis

## Project Overview

This project focuses on analyzing logistics and delivery operations data to identify delivery inefficiencies, operational delays, route performance, and shipment patterns.

The dataset contains trip-level as well as segment-level shipment information. Since one trip can consist of multiple delivery segments, aggregation and feature engineering techniques were used to transform the dataset into meaningful trip-level insights.

The project includes:

* Exploratory Data Analysis (EDA)
* Feature Engineering
* Row Aggregation
* Hypothesis Testing
* Missing Value Treatment
* Outlier Treatment
* Categorical Encoding
* Data Standardization
* Business Insights & Recommendations

---

# Problem Statement

The objective of this project is to analyze logistics and delivery operations data to:

* Improve delivery efficiency
* Identify operational bottlenecks
* Compare actual delivery performance with OSRM estimated metrics
* Analyze route and corridor performance
* Detect abnormal delivery delays and outliers
* Generate actionable business recommendations

---

# Business Questions Solved

1. Are actual delivery times significantly different from OSRM predicted times?
2. Which routes/corridors are busiest?
3. Which transportation types perform better (FTL vs Carting)?
4. Are there abnormal delays or distance outliers present in the data?
5. Which states/cities contribute the highest number of deliveries?
6. How can logistics operations and delivery efficiency be improved?

---

# Dataset Information

The dataset contains shipment segment-level logistics information.

## Important Features

| Column Name                    | Description                         |
| ------------------------------ | ----------------------------------- |
| trip_uuid                      | Unique ID for each trip             |
| source_center                  | Source warehouse ID                 |
| destination_center             | Destination warehouse ID            |
| route_type                     | Transportation type (FTL / Carting) |
| actual_time                    | Actual delivery time                |
| osrm_time                      | Estimated delivery time using OSRM  |
| osrm_distance                  | Estimated route distance            |
| segment_actual_time            | Segment-level delivery time         |
| segment_osrm_time              | Segment-level estimated time        |
| actual_distance_to_destination | Actual delivery distance            |

---

# Project Workflow

## 1. Exploratory Data Analysis (EDA)

* Dataset structure analysis
* Missing value detection
* Duplicate checking
* Distribution analysis
* Outlier detection
* Correlation analysis

## 2. Feature Engineering

* Extracted month, day, hour, weekday features
* Created trip duration feature
* Extracted source and destination state information
* Built corridor-level features

## 3. Aggregation of Rows

The dataset originally contained segment-level shipment records.

Aggregation was performed in two stages:

1. Source-Destination level aggregation
2. Trip-level aggregation

This helped convert the dataset into complete trip-level records.

## 4. Hypothesis Testing

Performed paired t-tests for:

* Actual Time vs OSRM Time
* Actual Time vs Segment Actual Time
* OSRM Distance vs Segment OSRM Distance
* OSRM Time vs Segment OSRM Time

## 5. Missing Value & Outlier Treatment

* Missing values treated using median and mode imputation
* Outliers handled using IQR method

## 6. Categorical Encoding

* One-Hot Encoding applied on categorical features

## 7. Standardization

* StandardScaler used for numerical feature scaling

---

# Key Insights

* Actual delivery times are generally higher than OSRM estimated times.
* Certain delivery corridors handle significantly higher shipment volumes.
* Long-distance routes contribute heavily to delivery delays.
* Segment-level delays directly affect complete trip performance.
* Transportation mode impacts delivery efficiency.
* Outliers indicate occasional operational disruptions.

---

# Business Recommendations

## Improve High-Delay Corridors

* Monitor congested routes
* Optimize route planning
* Improve operational support

## Strengthen Operations in High-Demand States

* Increase warehouse capacity
* Allocate additional vehicles and manpower

## Optimize Transportation Modes

* Use FTL for long-distance shipments
* Use Carting for shorter deliveries

## Reduce Segment-Level Delays

* Improve hub coordination
* Reduce waiting time during transfers

## Monitor Extreme Delays

* Track abnormal shipment delays
* Create operational alert systems

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy
* Google Colab

---

# Project Structure

```bash
Delhivery-Logistics-Analysis/
│
├── delhivery_data.csv
├── Delhivery_Logistics_Analysis.ipynb
├── README.md
```

---

# Conclusion

This project successfully transformed segment-level logistics data into meaningful trip-level insights.

Through EDA, aggregation, feature engineering, hypothesis testing, and business analysis, several operational inefficiencies and delivery patterns were identified.

The recommendations provided can help improve:

* delivery speed
* route optimization
* operational efficiency
* customer satisfaction

---

# Author

Praneetha VL
