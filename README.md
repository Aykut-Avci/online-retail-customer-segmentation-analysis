# RFM-Based Customer Segmentation for a UK Online Retailer

![Project Cover](data/project_cover.png)

## Project Overview 

This project aims to segment customers based on their purchasing behavior using the "Online Retail II" dataset. This dataset contains transactions from a UK-based online retailer, covering the period from 01/12/2009 to 09/12/2011. By performing RFM (Recency, Frequency, Monetary) analysis, we identify distinct customer segments, which helps in developing targeted marketing strategies to boost sales and enhance customer satisfaction.
 
This repository includes data preprocessing, exploratory analysis, and recommendations. At the end of the analysis on jupyter notebook, customer segments are labeled in the clean dataset and visualized using Tableau.

## Table of Contents


1. [Data](#data)
2. [Analysis](#analysis)
3. [Visualization](#visualization)
4. [Results](#results)

## Data

The dataset contains transactions from a real UK-based online retail company, which mainly sells unique all-occasion giftware. The raw dataset consists of 1,067,371 records and 8 attributes:

   1. **InvoiceNo:** Invoice number. *Nominal*. A 6-digit integral number uniquely assigned to each transaction. Invoice numbers that start with the letter 'C' indicates a cancellation.
   2. **StockCode:** Product (item) code. *Nominal*. A 5-digit integral number uniquely assigned to each distinct product.
   3. **Description:** Product (item) name. *Nominal*.
   4. **Quantity:** The quantities of each product (item) per transaction. *Numeric*.
   5. **InvoiceDate:** Invoice date and time. *Numeric*. The day and time when a transaction was generated.
   6. **UnitPrice:** Unit price. *Numeric*. Product price per unit in sterling (£).
   7. **CustomerID:** Customer number. *Nominal*. A 5-digit integral number uniquely assigned to each customer.
   8. **Country:** Country name. *Nominal*. The name of the country where a customer resides.

Originally **Description** and **CustomerID** columns contains null values with 22.77% of the rows for customerid being null, we proceeded with dropping these rows since deduction of these customerid from invoice numbers wasn't possible. Dropping null customerids resulted in all non-null description column. For RFM analysis, we omitted cancelled orders since they had negative quantities and would affect the monetary value of the customers with cancelled orders. Clean dataset contains `824364` records.

[Source of dataset - Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset/data)

## Analysis 

**1. Data Preparation:**  Data is preprocessed to remove duplicates, null values and implausible values.

**2. RFM Score calculation:**  

*  **Recency:** Number of days between the reference date and the date each customer made their last purchase.
*  **Frequency:** The total number of purchases made by the customer.
*  **Monetary:** The total amount spent by the customer across all transactions.

After calculation of these metrics for each customer, they have been given a score(1-5), with higher scores indicating better performance(more recent purchase, higher frequency and higher spending).

**3.Customer Segmentation:**

After calculation of RFM Score by summing up individual Recency, Frequency and Monetary Scores, customers were divided into 4 meaningful categories such as `Champions`, `Loyal Customers`, `Needs Attention` and `At Risk`.
Then we described segment profiles by identifying key statistics for each segment, such as mean, max, min, and total (sum) and shared insights and recommendations tailored to each segment. 

**4.Visualization:**

After assignment of segment labels to each customers, we exported clean segment labelled dataset, consisting of purchases to create a dashboard on Tableau to visualize Sales and Customer Segmentation related plots. You can view the interactive Tableau dashboard for this project [here](https://public.tableau.com/app/profile/aykut.avci/viz/CustomerSegmentationAnalysis-UKOnlineRetailDataset/CustomerDashboard). 

  ##### **Dashboard Overview:**
  
  - **Big Aggregate Numbers**: This section displays three key performance indicators (KPIs) that can be filtered across different years.
  - **Order Frequency and Recency**: Visualizations of order frequency and recency provide insights into customer behavior over time.
  - **Top 10 Customers**: A graph showing the top 10 customers based on monetary value helps identify high-value customers.



## Results
