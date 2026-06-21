# Data Cleaning Steps

The main notebook documents a practical data cleaning workflow for the Online Retail II dataset.

## Steps Covered

1. Load the two Excel worksheets for the 2009-2010 and 2010-2011 periods.
2. Combine both worksheets into one dataframe.
3. Standardise column names by trimming spaces and replacing spaces with underscores.
4. Check the dataset shape, data types, missing values, and duplicate rows.
5. Convert `InvoiceDate` to datetime format.
6. Convert `Customer_ID` to a nullable integer type where customer IDs are available.
7. Convert `StockCode` to text to support filtering and grouping.
8. Create `TotalSales` as `Quantity * Price`.
9. Identify cancelled or returned invoices where invoice numbers start with `C`.
10. Create a valid sales dataset by excluding cancelled invoices, non-positive quantities, and non-positive prices.
11. Create monthly fields for trend analysis.
12. Prepare grouped datasets for product, customer, country, and return analysis.

## Notes

Missing customer IDs are retained for sales-level analysis but excluded from customer-level analysis where a customer identifier is required.

Returns and cancellations are reviewed separately because they can distort gross sales trends if mixed directly with valid sales.

The notebook should be run from top to bottom before publishing final findings so that all figures and written observations match the latest outputs.
