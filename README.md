# Exploratory Data Analysis (EDA) on Online Retail Dataset

##  Project Overview
This project performs **Exploratory Data Analysis (EDA)** on the *Online Retail* dataset from the UCI Machine Learning Repository. The goal of this analysis is to understand sales patterns, customer behavior, and product trends using data cleaning, visualization, and feature engineering techniques.

---

## 📁 Dataset
**Source:** UCI Machine Learning Repository – Online Retail Dataset  
The dataset contains transactional data including:
- Invoice number  
- Stock code  
- Product description  
- Quantity  
- Invoice date  
- Unit price  
- Customer ID  
- Country  

---

##  Objectives
In this project, I aimed to:

- Clean and preprocess the raw dataset  
- Handle missing and invalid values  
- Remove cancelled and erroneous transactions  
- Perform feature engineering (e.g., Month, TotalSales)  
- Analyze monthly sales trends  
- Visualize key insights using Matplotlib  

---

##  Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook / VS Code**

---

##  Key Steps Performed

###  Data Cleaning
- Removed rows with missing descriptions  
- Filtered out negative prices and quantities  
- Handled duplicate product descriptions per StockCode  

###  Feature Engineering
Created new features such as:
- `TotalSales = Quantity * UnitPrice`
- `Month` extracted from `InvoiceDate`

###  Aggregation & Analysis
Calculated:
```python
monthly_sales = df4.groupby("Month", as_index=False)["TotalSales"].sum()
