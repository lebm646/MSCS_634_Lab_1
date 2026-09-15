# MSCS-634 Lab 1

## Data Visualization, Data Preprocessing, and Statistical Analysis Using Python

### Overview

This project was completed for MSCS-634 Advanced Big Data and Data Mining. The purpose of this lab is to demonstrate basic data analysis techniques using Python and Jupyter Notebook.

The lab focuses on data visualization, data preprocessing, and statistical analysis using a synthetic sales dataset.

---

## Dataset

The dataset contains 100 sales records with the following attributes:

- Date
- Product
- Category
- Region
- Units Sold
- Unit Price
- Customer Rating
- Discount
- Revenue

Missing values and outliers were intentionally introduced into the dataset to demonstrate data cleaning and preprocessing techniques.

---

## Data Visualization

The dataset was explored using multiple visualization techniques, including:

- Scatter plot of Units Sold vs Revenue
- Bar chart of Average Revenue by Product Category

The scatter plot showed that revenue generally increases as more units are sold, although revenue is also influenced by unit price and discount.

The bar chart showed differences in average revenue between product categories.

---

## Data Preprocessing

Several preprocessing techniques were applied to prepare the data for analysis.

### Missing Values

Missing values were detected using Pandas.

- Missing `Unit_Price` values were replaced with the mean unit price.
- Missing `Customer_Rating` values were replaced with the median rating.
- Missing revenue values were recalculated after the unit prices were filled.

### Outlier Detection

The Interquartile Range (IQR) method was used to identify outliers in the `Revenue` column.

Values below:

`Q1 - 1.5 × IQR`

or above:

`Q3 + 1.5 × IQR`

were considered outliers and removed from the dataset.

### Data Reduction

Two data reduction techniques were demonstrated:

- Random sampling was used to retain 70% of the cleaned dataset.
- The `Discount` column was removed to demonstrate dimensionality reduction.

### Data Scaling and Discretization

Min-Max Scaling was applied to the `Revenue` column to transform revenue values to a range between 0 and 1.

Revenue was also discretized into three categories:

- Low
- Medium
- High

---

## Statistical Analysis

The following statistical analysis techniques were performed:

- General dataset overview using `info()` and `describe()`
- Minimum and maximum values
- Mean
- Median
- Mode
- Range
- Quartiles
- Interquartile Range (IQR)
- Variance
- Standard deviation
- Correlation analysis

The correlation matrix was used to examine relationships between numerical variables such as Units Sold, Unit Price, Customer Rating, Discount, and Revenue.

---

## Key Insights

The analysis produced several useful observations:

- Revenue generally increases as the number of units sold increases.
- Unit price also contributes to differences in revenue.
- Several extreme revenue values were detected as outliers using the IQR method.
- Missing values can be successfully handled using statistical replacement techniques such as mean and median imputation.
- Data scaling and discretization can make numerical values easier to compare and prepare them for further analysis or machine learning.
- Correlation analysis helps identify relationships between numerical features.

---

## Challenges and Decisions

One challenge was determining appropriate techniques for handling missing values and outliers.

The mean was used to replace missing unit prices because it provides a reasonable estimate based on the available price data. The median was used for customer ratings because it is less affected by extreme values.

The IQR method was selected for outlier detection because it is a simple and effective technique that does not rely heavily on assumptions about the distribution of the data.

A synthetic dataset was used so that missing values and outliers could be intentionally included and used to demonstrate each required preprocessing technique.

---

## Files

- `MSCS_634_Lab_1.ipynb` - Jupyter Notebook containing all lab code and analysis
- `sales_data.csv` - Original sales dataset
- `sales_data_cleaned.csv` - Cleaned dataset after preprocessing
- `screenshots/` - Screenshots of required outputs and visualizations

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
