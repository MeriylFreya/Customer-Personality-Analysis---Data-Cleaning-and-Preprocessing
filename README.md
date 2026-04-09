# Data Cleaning & Preprocessing – Customer Personality Analysis

## Project Overview
This project focuses on cleaning and preprocessing the Customer Personality Analysis dataset to make it suitable for analysis and modeling.

Raw datasets often contain missing values, duplicates, inconsistent formats, and incorrect data types. The goal of this task is to transform messy data into a clean, structured format.

---

## Dataset
- Source: Kaggle  
- Name: Customer Personality Analysis  
- File Used: marketing_campaign.csv  

---

## Tools Used
- Python  
- Pandas  

---

## Data Cleaning Steps

### 1. Data Loading & Inspection
- Loaded dataset using Pandas  
- Checked structure using `.head()` and `.info()`  

### 2. Handling Missing Values
- Identified missing values using `.isnull().sum()`  
- Filled missing values in `Income` column using median imputation  
- Median is used instead of mean to avoid the effect of outliers  

### 3. Removing Duplicates
- Checked duplicate records using `.duplicated()`  
- Removed duplicates using `.drop_duplicates()`  

### 4. Column Name Standardization
- Converted column names to lowercase  
- Replaced spaces with underscores for consistency  

### 5. Date Format Conversion
- Converted `Dt_Customer` column to datetime format using `pd.to_datetime()`  

### 6. Text Standardization
- Cleaned categorical columns like:
  - `Education`
  - `Marital_Status`  
- Applied lowercase conversion and removed extra spaces  

### 7. Data Type Fixing
- Converted:
  - `Income` → float  
  - `Year_Birth` → integer  

### 8. Feature Engineering
- Created a new column `Age` from `Year_Birth`  
- This makes the dataset more meaningful for analysis  

### 9. Outlier Treatment (Optional)
- Used IQR (Interquartile Range) method to remove extreme values in `Income`  
- Helps improve data quality and analysis accuracy  

---

## Output
- Final cleaned dataset saved as:  
  `cleaned_customer_personality.csv`  

---

## Key Learnings
- Handling missing values effectively  
- Identifying and removing duplicate data  
- Standardizing inconsistent formats  
- Converting data types correctly  
- Creating meaningful features from raw data  
- Understanding the importance of clean data before analysis  

---

## Interview Questions Covered

**1. What are missing values and how do you handle them?**  
Missing values are absent data points. They can be handled by removing rows or filling them using mean, median, or mode depending on the data.

**2. Difference between dropna() and fillna()?**  
- dropna() removes missing data  
- fillna() replaces missing values  

**3. How do you treat duplicate records?**  
By identifying them using `.duplicated()` and removing them using `.drop_duplicates()`  

**4. What is outlier treatment?**  
It involves detecting and handling extreme values that can distort analysis  

**5. What is data standardization?**  
Making data consistent in format, such as text case or naming conventions  

**6. How do you handle inconsistent date formats?**  
Using `pd.to_datetime()` to convert into a uniform datetime format  

**7. Common data cleaning challenges?**  
Missing values, inconsistent formats, incorrect data types, duplicates  

**8. How to check data quality?**  
Using:
- `.info()`  
- `.describe()`  
- `.isnull().sum()`  
- `.duplicated()`  

---

## Conclusion
The dataset was successfully cleaned and transformed into a structured format. This prepares it for further analysis, visualization, or machine learning tasks.
