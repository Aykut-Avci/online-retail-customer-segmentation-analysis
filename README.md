# RFM-Based Customer Segmentation for a UK Online Retailer

![Project Cover](data/project_cover.png)

## Project Description 

This project aims to segment customers based on their purchasing behavior using the "Online Retail II" dataset. This dataset contains transactions from a UK-based online retailer, covering the period from 01/12/2009 to 09/12/2011. By performing RFM (Recency, Frequency, Monetary) analysis, we identify distinct customer segments, which helps in developing targeted marketing strategies to boost sales and enhance customer satisfaction.
 
This repository includes data preprocessing, exploratory analysis, and recommendations. Customer segments are labeled in the clean dataset and visualized using Tableau.

## Table of Contents

- Data: Dataset contains the transactions from a real UK-based online retails company, which mainly sells unique all-occasion gift-ware. Raw dataset consists of 1067371 records and 8 attributes as:
  - InvoiceNo: Invoice number. Nominal. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.
  * StockCode: Product (item) code. Nominal. A 5-digit integral number uniquely assigned to each distinct product.
  * Description: Product (item) name. Nominal.
  * Quantity: The quantities of each product (item) per transaction. Numeric.
  * InvoiceDate: Invice date and time. Numeric. The day and time when a transaction was generated.
  * UnitPrice: Unit price. Numeric. Product price per unit in sterling (Â£).
  * CustomerID: Customer number. Nominal. A 5-digit integral number uniquely assigned to each customer.
  * Country: Country name. Nominal. The name of the country where a customer resides.
- Analysis
- Results
- Visualization


  You can view the interactive Tableau dashboard for this project [here](https://public.tableau.com/app/profile/aykut.avci/viz/CustomerSegmentationAnalysis-UKOnlineRetailDataset/CustomerDashboard)
