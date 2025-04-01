# Walmart Sales Data Analysis

## 📈 Project Overview

This project provides an end-to-end data analysis solution to extract key business insights from Walmart sales data. It integrates Python for data processing and analysis, SQL for advanced querying, and Tableau for interactive visualizations.

By leveraging data-driven decision-making, we aim to analyze sales trends, customer purchasing behavior, and revenue patterns to help businesses optimize their strategies.

## 📂 Dataset Overview

The dataset consists of Walmart sales transactions, including key attributes such as:

**Invoice ID**: Unique transaction ID

**Branch**: Store location (A, B, or C)

**City**: The city where the branch is located

**Customer Type**: Type of customer (Member/Normal)

**Gender**: Customer gender

**Product Category**: Different categories of items sold

**Unit Price**: Price per unit

**Quantity**: Number of items purchased

**Total**: Total amount for each transaction

**Date & Time**: Timestamp of purchase

**Payment Method**: Cash, Credit Card, or E-wallet

**Rating**: Customer feedback rating (1–10)

## 🛠️ Technologies Used

**Python**: pandas, numpy, sqlalchemy, matplotlib

**SQL**: MySQL and PostgreSQL for database storage and querying

**Tableau**: For interactive dashboards and data visualization

**Jupyter Notebook**: For exploratory data analysis

**Kaggle API**: For dataset retrieval

## 📈 Project Workflow

**1. Data Collection & Preparation**

Downloaded the dataset from Kaggle

Cleaned and transformed the data using Python (pandas, numpy)

Converted date/time fields into proper formats

Handled missing values, duplicates, and outliers

**2. Data Storage & SQL Processing**

Stored cleaned data into MySQL and PostgreSQL databases

Created structured tables for efficient querying

Performed complex SQL queries for trend analysis, revenue tracking, and customer insights

**3. Business Insights & Data Visualization**

Created interactive Tableau dashboards for:

Branch-wise revenue trends

Top-selling product categories

Customer purchase patterns (Time & City-wise)

Sales performance by payment method

Peak sales periods

Used Python (matplotlib, seaborn) for additional data visualizations

## 📊 Tableau Dashboard

📍 Explore the interactive dashboard here: https://public.tableau.com/app/profile/anand.khanna/viz/walmart_analysis_17434846279930/performancedashboard?publish=yes
(performance dashboard.png)

Branch & City-Wise Sales Performance

Product Category Analysis

Customer Rating Distribution

Sales Trends Over Time

## 🔖 SQL Queries & Key Insights

Below are some critical SQL queries performed for analysis:

**1. Revenue Trends by Branch & Category**

SELECT Branch, Category, AVG(Rating) AS avg_rating
FROM walmart
GROUP BY Branch, Category;

📌 Insight: The highest-rated product categories vary by branch, providing insights into customer satisfaction.

**2. Sales Performance by Payment Method**

SELECT Payment_Method, SUM(Total) AS revenue
FROM walmart
GROUP BY Payment_Method;

📌 Insight: Understanding customer payment preferences helps in streamlining transaction processing.

**3. Identifying Peak Sales Hours**

SELECT 
    EXTRACT(HOUR FROM Time) AS Hour, 
    SUM(Total) AS Total_Sales
FROM walmart
GROUP BY EXTRACT(HOUR FROM Time)
ORDER BY Total_Sales DESC;

📌 Insight: Sales peak during afternoon and evening hours, helping in staff allocation and inventory management.


## 📈 Future Improvements

🔹 Implement Machine Learning: Predict future sales trends using ML models

🔹 Customer Segmentation: Use clustering algorithms to segment customers based on buying behavior

🔹 Automated Reporting: Create scheduled SQL queries & dashboards for real-time insights
