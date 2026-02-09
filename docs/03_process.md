# Process

## Data Cleaning Overview
The data cleaning process focused on ensuring data quality and consistency while preserving records relevant to solving the business question which created in the ask phrase.

## Cancelled Transactions
Transactions with invoice numbers starting with the letter 'C' indicate cancellations or returns.
These records were excluded from gross revenue analysis to avoid distorting sales performance trends.
However, cancellation data was retained and analysed separately to calculate net sales and understand return patterns.

## Invalid Quantity and Unit Price
Transactions with Quantity less than or equal to zero were treated as invalid sales records rather than returns, as cancelled transactions are explicitly identified by invoice numbers starting with 'C'. 
Similarly, records with zero or negative UnitPrice values were excluded, as they do not represent valid revenue-generating transactions.

## Missing CustomerID
Some transactions do not contain CustomerID values, likely representing one off or anonymous purchases.
These records were retained for sale analysis but excluded from customer-level analysis.

## Derived Fields
A new field , TotalSales was created by multiplying Quantity by unitPrice to enable revenue-based analysis.

## Data Consistency
Basic checks were performed to ensure consistent date formats and currency values across the dataset before analysis.

