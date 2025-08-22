# Real-Estate-Market-Insights-An-Exploratory-Analysis-of-Zameen.com-Listings-in-Pakistan
Uncovering what drives property prices across cities in Pakistan with EDA.
This repository contains an exploratory data analysis (EDA) of property listings from **Zameen.com**, showcasing the use of Python, particularly Pandas, NumPy, Matplotlib, and Seaborn, to uncover pricing patterns, regional trends, and investment insights in Pakistan’s real estate market.  

---

## Overview  
This project explores and analyzes a dataset of **18,239 property listings** from Zameen.com. The analysis was conducted in multiple stages to ensure a structured approach:  

### Initial Exploration:  
- Examined the dataset’s shape, features, and first/last rows using `head()` and `tail()`.  
- Gained an initial sense of property attributes such as city, price, area, and type.  

### Data Understanding:  
- Checked column data types with `info()` and generated descriptive statistics with `describe()`.  
- Documented key patterns in property features such as area distribution and bedroom/bathroom counts.  

### Missing Values Analysis:  
- Identified missing values across the dataset using `.isnull().sum()`.  
- Dropped high-missing-value columns (e.g., parking spaces, servant quarters).  
- Applied imputation strategies: mode for categorical features and median for numerical ones.  

### Duplicate Rows Analysis:  
- Confirmed data integrity by checking for duplicate rows with `.duplicated()`.  

### Data Cleaning & Consistency:  
- Standardized city names using **FuzzyWuzzy** and removed whitespace/casing inconsistencies.  
- Converted property areas into square feet for uniformity.  
- Standardized property types (e.g., “flat” vs “apartment”).  

### Feature Engineering:  
- Created new features for richer insights:  
  - `price_per_sqft`  
  - `price_category` (Low, Mid, High, Luxury)  
  - `property_age_group`  
  - `log_price` (for skewed distribution)  

### Analysis Performed  

**Univariate Analysis:**  
- Most listings are houses (73%).  
- Market dominated by low- and mid-priced categories.  
- Bedroom distribution shows price rises until 10 bedrooms, then declines.  

**Bivariate Analysis:**  
- Location strongly drives prices → DHA (Karachi), Gulberg (Lahore), Bahria Town (Islamabad) lead in price per sqft.  
- Weak correlation between area and price (r ≈ 0.0009).  
- Bedrooms and bathrooms strongly correlated (r = 0.86).  

**Multivariate Analysis:**  
- Price per sqft varies significantly across cities and property types.  
- Older properties in prime locations command higher values.  

---

## Tools and Libraries Used  
- **Python**: Core programming language  
- **Pandas & NumPy**: Data wrangling and preprocessing  
- **Matplotlib & Seaborn**: Data visualization  
- **FuzzyWuzzy**: String matching for city name standardization  
- **Jupyter Notebook**: Analysis environment  

