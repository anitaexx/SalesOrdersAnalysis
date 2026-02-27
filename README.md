# SalesOrdersAnalysis
ERP Sales Order Data Exploration, Cleaning and Manipulation using Python

This project analyzes ERP-exported sales order data and transforms transactional records into structured analytical feature layers.

The goal was to:

Separate realized revenue from pipeline exposure
Quantify revenue concentration
Evaluate execution reliability
Measure financial exposure
Engineer reusable order-, customer-, and sales-rep-level features
The project emphasizes business-aware data handling and operational analytics.

1. Data Cleaning

Notebook: 01_data_exploration_cleaning.ipynb

Steps Performed :

Loaded ERP-exported dataset (CSV)
Corrected data types (dates, numeric fields)
Removed non-analytical fields (CRM metadata, remarks, unused attributes)
Handled missing execution dates using business logic
Removed duplicates using order-level business keys
Preserved signed financial values:
Positive balance → customer owes

2. Exploratory Data Analysis

Notebook: 02_Exploratory_data_analysis.ipynb

Revenue Structure

- Separated executed vs draft orders

- Quantified realized revenue vs pipeline exposure

- Revenue Concentration

Ranked customers by total revenue

- Identified right-skewed distribution

- Confirmed concentration risk

Order Value Distribution

- Heavy right skew in order totals

- Large orders disproportionately impact totals

Sales Rep Analysis

- Execution rate by sales rep

- Pipeline exposure by rep

Financial exposure ratios

- Fulfillment gap frequency

3. Feature Engineering

Notebook: 03_Feature_Engineering.ipynb

Order-Level Features
Customer-Level Features
Sales-Rep-Level Features


Key Findings :

Revenue is highly right-skewed.
A small subset of customers drives a disproportionate share of total revenue.
Execution reliability varies across sales reps.
Financial exposure (outstanding balances) is unevenly distributed.
Fulfillment gaps represent operational friction rather than customer behavior.

Technologies Used

Python Libraries :
Pandas
NumPy
Matplotlib
Seaborn


Notes :

The dataset represents a snapshot export from ERP.

