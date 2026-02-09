# Prepare

## Dataset Overview
-   Dataset name: online_retail_II
-   Source: UCI Machine Learning Repository
-   Company type: UK-based and registered, non-store online retail
-   Time Period: 01/12/2009 - 09/12/2011
-   Data Type:  Transactional-level Data

## Unit of Analysis
Each row represent a single transaction within a customer

## Key Firleds
-   InvoiceNo: Unique 6-digit integral number (starts with the letter 'c', it indicates a cancellatio)
-   StockCode:  Unique product code
-   Description: Product Name
-   Quantity: The quantities of each product (item) per transaction. 
-   InvoiceDate:    The day and time when a transaction was generated.
-   UnitPrice:  Product price per unit in GBP
-   CustomerID: Unique 5-digit integral number
-   Country:    Country name

## Data Credibility and Limitations
-   Dataset based on a real online retail transaction data set of two years, while increase Credibility
-   There are missing value in CustomerID , zero or negative number in Quantity & Unit Price.
-   Cancelled transactions are inclued and require careful handling.
-   No information on product cost , market campaigns. We can't calculate net profit.

## Suitabnility for Analysis
This dataset is suitable for analysing sales trend, product performance and customer purchasing behaviour.


