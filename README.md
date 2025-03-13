# Retail-Chip-Analytics

## Overview
This project focuses on analyzing the chips category of a superstore. The analysis includes data cleaning, feature engineering, customer segmentation, and generating insights that help inform marketing strategies and product positioning for the chips category. The project leverages Python (with libraries such as Pandas, NumPy, Seaborn, and Matplotlib) to process transaction data and derive actionable insights.

## Project Objectives
- **Data Preparation:** Clean and preprocess the chip transaction data to remove non-relevant entries (e.g., salsa products) and outliers (e.g., bulk transactions).
- **Feature Engineering:** Extract key features such as pack size and brand from product names, ensuring standardized values.
- **Customer Segmentation:** Analyze and segment customers based on life stage and premium status to understand purchasing behaviors.
- **Insight Generation:** Identify key trends (e.g., price sensitivity, brand affinity) and generate recommendations for targeting high-value segments.
- **Visualization:** Create visual outputs (e.g., histograms, boxplots, and bar charts) to support the findings.

## Data Description
- **Transaction Data:** Contains chip transaction details with columns such as:
  - `DATE`: Transaction date (as an integer representing days since 1899-12-30).
  - `STORE_NBR`: Store number.
  - `LYLTY_CARD_NBR`: Loyalty card number (customer ID).
  - `TXN_ID`: Transaction identifier.
  - `PROD_NBR`: Product number.
  - `PROD_NAME`: Name of the product (e.g., chip type, flavor, pack size).
  - `PROD_QTY`: Quantity purchased.
  - `TOT_SALES`: Total sales amount.
- **Customer Data:** Contains customer demographics with columns such as:
  - `LYLTY_CARD_NBR`: Customer identifier.
  - `LIFESTAGE`: Life stage of the customer (e.g., YOUNG SINGLES/COUPLES, OLDER FAMILIES).
  - `PREMIUM_CUSTOMER`: Customer segment based on spending behavior (e.g., Budget, Mainstream, Premium).

## Methodology & Approach
1. **Data Cleaning:**  
   - Convert the date field from integer to a proper datetime format.
   - Remove entries that contain non-chip items (e.g., any row where `PROD_NAME` includes "salsa").
   - Identify and remove outlier transactions (e.g., bulk orders where `PROD_QTY` equals 200).

2. **Feature Engineering:**  
   - Extract `PACK_SIZE` from the `PROD_NAME` using regular expressions.
   - Extract and standardize the `BRAND` by taking the first word from `PROD_NAME` and applying corrections (e.g., merging “RED” with “RRD”).

3. **Customer Segmentation Analysis:**  
   - Merge the transaction and customer datasets on `LYLTY_CARD_NBR`.
   - Analyze customer purchasing behaviors across different life stages and premium segments.
   - Visualize metrics such as average price per unit, pack sizes, and brand preferences.

4. **Visualization:**  
   - Create histograms, boxplots, and bar charts to illustrate distribution of pack sizes, brand preferences, and segmentation performance.
   - Use consistent color schemes and formatting for clarity.

