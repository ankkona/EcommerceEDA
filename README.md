# E-commerce Sales Analysis | Python EDA

## Project Overview

This project focuses on analyzing an e-commerce sales dataset using Python to uncover insights related to sales performance, profitability, customer behavior, and operational efficiency.

The workflow includes data cleaning, preprocessing, feature engineering, exploratory data analysis (EDA), and visualization to understand the key factors affecting revenue and profit.

The dataset used in this project is a synthetic dataset generated using ChatGPT and designed to simulate real-world e-commerce transaction data with intentional data quality issues for practicing data cleaning and analysis.

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Data Cleaning & Preparation

The raw dataset contained multiple inconsistencies which were handled before analysis:

- Converted date columns into datetime format
- Removed currency symbols and converted price columns into numeric format
- Standardized inconsistent categorical values
- Handled missing values
- Corrected invalid age and customer rating values
- Processed discount values into numerical format
- Created new business metrics for analysis

## Feature Engineering

Created new analytical columns:

- Revenue
- Profit
- Profit Margin %
- Delivery Days
- Order Year
- Order Month

These features helped analyze business performance beyond the original transactional data.

## Exploratory Data Analysis

### Univariate Analysis

Analyzed individual variables to understand:

- Customer age distribution
- Category distribution
- Selling price distribution
- Customer ratings
- Order quantity patterns

### Bivariate Analysis

Explored relationships between two variables:

- Category vs Revenue
- City vs Revenue
- Category vs Profit
- Discount vs Profit
- Return Status distribution

### Multivariate Analysis

Analyzed multiple variables together:

- Category + City + Revenue
- Category + Return Status + Profit
- Category + Payment Method + Revenue
- Correlation analysis between numerical variables

## Key Insights

### Product Performance

- Electronics is the strongest category overall, with the highest order count, revenue, and profit. This indicates that sales volume is successfully translating into earnings rather than only generating high turnover.

- Kolkata is the top-performing city across categories, with the largest performance gap observed in Electronics, showing that city performance is concentrated rather than evenly distributed.

### Profitability Analysis

- Selling Price is the strongest driver of Profit with a correlation of 0.78, supported by a near-linear scatter relationship.

- Cost Price negatively impacts Profit with a correlation of -0.63, as expected.

- Discount levels do not appear to reduce profit. However, this may be influenced by higher-priced products receiving larger discounts rather than discounts directly increasing profitability.

- Customer Age, Quantity, and Customer Rating show minimal correlation with Profit, indicating that profitability is mainly driven by pricing factors rather than customer demographics.

### Order-Level Profitability

- Median order profit is only slightly positive (~₹500–600).

- The middle 50% of orders range approximately between -₹700 and +₹1800, showing that many individual orders are loss-making despite strong overall category-level performance.

### Sales Trend Analysis

- Revenue fluctuates month-to-month rather than showing steady growth.

- Revenue peaks in February (~₹1.8M) and reaches the lowest point in October (~₹1.42M), suggesting seasonal or event-driven demand patterns.

### Operational Analysis

- Delivery Days are evenly distributed between 0 and 8 days, indicating no major systemic shipping delay issue.

- Return counts increase proportionally with order volume, with no category showing an unusually high return rate.

### Data Quality Observation

- Around 39% of rows contained Cost Price higher than Selling Price, resulting in unrealistic negative profit margins.

- This was identified as a synthetic data quality issue rather than a genuine business pattern.

- These records were excluded from margin analysis instead of being artificially corrected.

## Jupyter Notebook

[View Complete EDA Notebook](9.6%20EDA6Ecommerce.ipynb)

## Conclusion

The analysis shows that category performance and pricing strategy are the major drivers of profitability. Electronics dominates overall performance, while city-level differences and pricing relationships provide useful insights for improving business decisions.

Project workflow:

Raw Data → Data Cleaning → Feature Engineering → Exploratory Analysis → Business Insights
