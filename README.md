# Sales Data Processing on Cloud with MapReduce and Amazon RDS

This project implements a scalable, cloud-based data processing pipeline to analyze liquor sales data from 2012 to 2020. The solution leverages distributed computing and storage using AWS and Hadoop ecosystem tools. This project was developed as part of an assignment at the International Institute of Information Technology Bangalore.

## 📌 Problem Statement

The project involves building a cloud-based, distributed data pipeline to extract business insights from liquor sales data. The key goals are:

- Efficiently ingest, clean, and prepare large-scale data for analysis.
- Perform batch processing and trend analysis using MapReduce.
- Analyze revenue, store/vendor performance, and sales trends.
- Derive insights and recommendations to optimize sales strategies.

## 🎯 Assignment Tasks

### 1. Data Ingestion and Preparation
- Upload the 'Liquor Sales Data Set' (2012–2020) into **AWS RDS (MySQL)** with proper schema.
- Split the dataset into manageable chunks if necessary.
- Use **Apache Sqoop** to transfer data from AWS RDS to **HBase**, with appropriate schema (column families and row keys).
- Validate data consistency across RDS and HBase.

### 2. Data Cleaning
- Remove rows with missing/incomplete values.
- Handle formatting issues and invalid values.
- Standardize categories and correct data formats.
- Remove duplicate records to ensure data integrity.

### 3. Batch Processing Using MapReduce

**Revenue and Sales Analysis**
- Calculate total revenue per store.
- Identify top-selling liquor categories using `Bottles_Sold` and `Sale_Dollars`.
- Aggregate sales by county to get total revenue and volume (litres/gallons).

**Store and Vendor Performance**
- Rank stores based on total revenue, volume sold, and average sales per transaction.
- Rank vendors by total revenue and volume using `Vendor_Name` and `Sale_Dollars`.

**Time-Based and Trend Analysis**
- Perform monthly/yearly trend analysis using the `Date` field.

### 4. Conclusion and Recommendations
- Recommend strategies to optimize store operations and increase sales.
- Suggest promoting top liquor categories to maximize revenue.
- Recommend scaling operations of top-performing vendors.
- Propose marketing adjustments based on time and county-based trends.

## 🛠️ Tools & Technologies Used

- **AWS RDS (MySQL)** – for structured data ingestion
- **Apache Sqoop** – for data transfer to HBase
- **AWS EMR** – for running Hadoop and MapReduce
- **HDFS** – for distributed data storage
- **Hadoop MapReduce** – for batch processing
- **SQL** – for preprocessing and analysis
- **Linux (SSH, PuTTY)** – for remote CLI access
- **Jupyter Notebook** – for documenting and tracking outputs
