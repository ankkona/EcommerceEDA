# 🛒 E-commerce Sales Analysis | Python EDA

## 📌 Project Overview

This project focuses on analyzing an e-commerce sales dataset using Python to uncover business insights related to sales performance, profitability, customer behavior, product categories, and operational efficiency.

The project includes data cleaning, preprocessing, feature engineering, exploratory data analysis (EDA), and visualization to understand the factors influencing revenue and profit.

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📂 Dataset Overview

The dataset contains e-commerce transaction details including:

- Order Information
- Customer Details
- Product Categories
- Pricing Information
- Discounts
- Payment Methods
- Customer Ratings
- Return Status
- Delivery Information

---

# 🔍 Data Cleaning & Preparation

The raw dataset contained multiple inconsistencies which were handled before analysis:

✔ Converted date columns into datetime format  
✔ Removed currency symbols and converted price columns into numeric format  
✔ Standardized inconsistent categorical values  
✔ Handled missing values  
✔ Corrected invalid age and rating values  
✔ Processed discount values into numerical format  
✔ Created new business metrics for analysis  

---

# ⚙️ Feature Engineering

New analytical columns were created:

- **Revenue**
- **Profit**
- **Profit Margin %**
- **Delivery Days**
- **Order Year**
- **Order Month**

These features helped analyze business performance beyond the raw transactional data.

---

# 📊 Exploratory Data Analysis

## Univariate Analysis

Analyzed individual variables to understand:

- Customer age distribution
- Category distribution
- Selling price distribution
- Customer ratings
- Order quantity patterns

---

## Bivariate Analysis

Explored relationships between two variables:

- Category vs Revenue
- City vs Revenue
- Category vs Profit
- Discount vs Profit
- Return Status distribution

---

## Multivariate Analysis

Analyzed multiple variables together:

- Category + City + Revenue
- Category + Return Status + Profit
- Category + Payment Method + Revenue
- Correlation analysis between numerical variables

---

# 📈 Key Insights

### 🏆 Product Performance

- **Electronics is the strongest category overall**, generating the highest order count, revenue, and profit. This indicates that sales volume is successfully converting into earnings rather than only creating high turnover.

- **Kolkata is the top-performing city across categories**, with the largest performance difference observed in Electronics, showing that city performance is concentrated rather than evenly distributed.

---

### 💰 Profitability Analysis

- **Selling Price is the strongest driver of Profit** with a correlation of **0.78**, supported by a near-linear scatter relationship.

- **Cost Price negatively impacts Profit** with a correlation of **-0.63**, as expected.

- Discount levels do not show a negative impact on profit. However, this may be influenced by higher-priced products receiving larger discounts rather than discounts directly improving profitability.

- Customer Age, Quantity, and Customer Rating show minimal correlation with Profit, indicating that profitability is primarily driven by pricing factors rather than customer demographics.

---

### 📦 Order-Level Profitability

- Median order profit is only slightly positive (~₹500–600).

- The middle 50% of orders range approximately between **-₹700 and +₹1800**, indicating that many individual transactions are loss-making despite strong overall category performance.

---

### 📅 Sales Trend Analysis

- Revenue fluctuates month-to-month rather than showing consistent growth.

- Highest revenue was observed in **February (~₹1.8M)**, while **October recorded the lowest (~₹1.42M)**, suggesting demand is influenced by seasonal or event-based factors.

---

### 🚚 Operational Analysis

- Delivery days are distributed evenly between **0 and 8 days**, indicating no major systematic delivery delay issue.

- Return counts increase proportionally with order volume, with no category showing an unusually high return rate.

---

### ⚠️ Data Quality Observation

- Around **39% of rows contained Cost Price higher than Selling Price**, creating unrealistic negative profit margins.

- This was identified as a **data quality issue** rather than a genuine business pattern.

- These records were excluded from margin-based analysis instead of being artificially corrected.

---

# 📓 Notebook

Complete EDA notebook:

[View E-commerce EDA Notebook](9.6%20EDA6Ecommerce.ipynb)

---

# 📌 Conclusion

The analysis shows that product pricing strategy and category performance are the major drivers of profitability. Electronics dominates overall business performance, while city-level differences and pricing relationships provide important insights for improving sales strategy.

The project demonstrates an end-to-end analytics workflow:

**Raw Data → Data Cleaning → Feature Engineering → Exploratory Analysis → Business Insights**
