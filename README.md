# Autonomous-Vehicle-Disengagement-Reports-EDA
In this notebook I want to use the "Autonomous Vehicle Disengagement Reports" dataset and explore it.

# Autonomous Vehicle Disengagement Reports - Exploratory Data Analysis (EDA)

## Overview

This notebook conducts an Exploratory Data Analysis (EDA) on the **2019 Autonomous Vehicle Disengagement Reports** dataset. The dataset contains reports of instances where autonomous vehicles disengaged from self-driving mode, requiring human intervention due to system malfunctions or complex driving scenarios.

The goal of this analysis is to clean, process, and explore the dataset to uncover insights about disengagement patterns, manufacturers, and contributing factors.

---

## Dataset Description

The dataset includes **8,885** reports of autonomous vehicle disengagements with the following columns:

- **Manufacturer**: Name of the company testing the autonomous vehicle.  
- **Permit Number**: Permit issued to the company for self-driving tests.  
- **DATE**: Date of the disengagement event.  
- **VIN NUMBER**: Unique vehicle identifier.  
- **VEHICLE IS CAPABLE OF OPERATING WITHOUT A DRIVER (Yes or No)**: Indicates if the vehicle can operate autonomously without a driver.  
- **DRIVER PRESENT (Yes or No)**: Indicates if a driver was present during the test.  
- **DISENGAGEMENT INITIATED BY (AV System, Test Driver, Remote Operator, or Passenger)**: Who or what initiated the disengagement.  
- **DISENGAGEMENT LOCATION (Interstate, Freeway, Highway, Rural Road, Street, or Parking Facility)**: Location type where the disengagement occurred.  
- **DESCRIPTION OF FACTS CAUSING DISENGAGEMENT**: Narrative of the reasons for disengagement.

---

## Key Steps

### Importing Libraries

- Used `pandas` and `numpy` for data manipulation  
- Utilized `matplotlib` and `seaborn` for visualization  
- Employed `dateutil.parser` for handling date formats  

### Data Cleaning

- Standardized the **DATE** column, which had inconsistent formats (e.g., dots, slashes, and month names), and converted it to a datetime format in a new `date` column  
- Handled problematic date entries using a custom parsing function with `dateutil.parser`  
- Dropped the original **DATE** column after cleaning  

---

## Observations

- The dataset contains **8,885** rows, each representing a disengagement report  
- All reports indicate a **driver was present** during testing  
- Fewer than **1,000** vehicles were reported as requiring a driver by design  
- Top manufacturers with the most disengagement reports:
  - Toyota Research Institute  
  - Mercedes-Benz Research & Development North America  
  - Lyft  
  - NVIDIA  
  - Udelv  

---

## Prerequisites

To run this notebook, ensure you have the following Python libraries installed:

- pandas  
- numpy  
- matplotlib  
- seaborn  
- python-dateutil  

Install them using pip:

```bash
pip install pandas numpy matplotlib seaborn python-dateutil

```
Dataset
Source: https://www.kaggle.com/datasets/art12400/2019-autonomous-vehicle-disengagement-reports

File: 2019AutonomousVehicleDisengagementReports.csv

Notes
This notebook focuses on data cleaning and initial exploration

Further analysis (e.g., visualizations, statistical insights) can be extended based on specific research questions

The dataset reflects 2019 data; results may not generalize to other years or contexts
