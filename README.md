
# Retail Sales Data Analysis

This repository contains a comprehensive Python script for analyzing retail sales data. The analysis spans data cleaning, transformation, and visualization, providing insights into sales trends, customer demographics, and channel performance. The script leverages powerful libraries such as `pandas`, `seaborn`, `matplotlib`, and `plotly` to handle the data and generate meaningful visualizations.

## Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Running the Script](#running-the-script)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
  - [Handling Missing Values](#handling-missing-values)
  - [Correcting Data Inconsistencies](#correcting-data-inconsistencies)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Sales by Channel](#sales-by-channel)
  - [Department Sales Analysis](#department-sales-analysis)
  - [Price and Sales Distribution](#price-and-sales-distribution)
  - [Customer Demographics](#customer-demographics)
- [Data Visualization](#data-visualization)
  - [Using Matplotlib and Seaborn](#using-matplotlib-and-seaborn)
  - [Interactive Plots with Plotly](#interactive-plots-with-plotly)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The goal of this project is to perform a detailed analysis of retail sales data, uncovering trends and patterns that can inform business decisions. The analysis includes:
- **Data Cleaning**: Identifying and handling missing or inconsistent data.
- **Aggregation and Grouping**: Analyzing data across various dimensions such as sales channels, departments, and customer demographics.
- **Visualization**: Creating both static and interactive visualizations to communicate insights clearly.

## Getting Started

### Prerequisites

To run the script, ensure you have the following Python libraries installed:

```bash
pip install pandas seaborn matplotlib plotly cufflinks chart-studio
```

### Running the Script

1. **Data Files**: The script reads from two main Excel files: `varejo.xlsx` (sales data) and `cliente_varejo.xlsx` (customer data). Ensure these files are located in the same directory as the script.

2. **Execution**: The script can be run in any Python environment (e.g., Jupyter Notebook, VSCode). It processes the data, performs analyses, and generates visualizations directly within the environment.

## Data Cleaning and Preparation

### Handling Missing Values

The dataset may contain missing values that need to be addressed to ensure accurate analysis:
- **Dropping Null Values**: The script removes rows with null values where necessary using `dropna()`.
- **Imputation**: For certain columns, missing values are filled with either a specific value (e.g., a default state code) or the mean of the column using `fillna()`.

### Correcting Data Inconsistencies

Inconsistent data can skew results, so the script includes steps to standardize and correct the dataset:
- **Replacing Inconsistent Values**: Strings in categorical columns are standardized (e.g., replacing 'APP' with 'Aplicativo').
- **Filtering Outliers**: Transactions with prices higher than the total price including freight are identified and excluded from the analysis.

## Exploratory Data Analysis (EDA)

### Sales by Channel

The script groups the sales data by sales channel (`idcanalvenda`) and calculates the unique number of purchases for each channel. This helps identify the most and least popular sales channels.

### Department Sales Analysis

The analysis includes examining sales across different departments:
- **Sales Volume**: The script counts the number of unique purchases per department.
- **Price Analysis**: Average prices (including freight) are calculated for each department, providing insights into pricing strategies.

### Price and Sales Distribution

The script explores the distribution of sales over time, particularly focusing on monthly trends:
- **Sales by Month**: Sales are aggregated by month to identify seasonal trends.
- **Price Analysis**: The distribution of prices is analyzed to identify any unusual patterns.

### Customer Demographics

By joining the sales data with customer data, the script analyzes:
- **Average Income by Sales Channel**: Aggregates income data by sales channel to understand the financial profile of customers in different channels.
- **Average Age by Store Brand**: Analyzes the average age of customers by store brand to identify demographic trends.

## Data Visualization

### Using Matplotlib and Seaborn

The script includes multiple visualizations created using `matplotlib` and `seaborn`:
- **Bar Charts**: Used to visualize categorical data such as average age by brand and average income by sales channel.
- **Line Charts**: Used to show trends over time, such as the number of sales per day.

### Interactive Plots with Plotly

For more dynamic exploration, the script also utilizes `plotly` to create interactive visualizations:
- **Interactive Bar Charts**: Allow for hovering over data points to reveal detailed information.
- **Interactive Line Charts**: Provide a zoomable and pan-able interface for exploring time series data.


