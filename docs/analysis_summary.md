# Analysis Summary

## Dataset Overview

The notebook starts by loading and inspecting the Online Retail II transaction data. This section checks the available fields, row counts, missing values, duplicate rows, and basic data types.

## Data Cleaning

The cleaning section prepares the data for analysis by standardising column names, creating a revenue field, converting dates, identifying cancellations or returns, and filtering valid sales records.

## Revenue Trend Analysis

The revenue trend section groups valid sales by month. It is intended to show how revenue changes over time and whether seasonal patterns appear in the dataset.

## Product Analysis

The product section groups revenue by stock code and description. It is intended to identify the highest revenue products and review whether revenue is concentrated among a small number of products.

## Customer Analysis

The customer section excludes rows without customer IDs, then groups revenue by customer. It is intended to identify high-value customers and review customer concentration risk.

## Country Analysis

The country section groups revenue by country. It is intended to show which countries contribute most to revenue.

## Returns and Cancellations

The returns section uses invoices beginning with `C` to review cancelled or returned transactions separately from valid sales. It is intended to highlight whether returns require additional investigation before business conclusions are made.

## Findings and Recommendations

The notebook validation run confirmed that the combined raw dataset contains 1,067,371 rows and the cleaned valid sales dataset contains 1,041,670 rows. It also confirmed that the top 10 filtered product codes account for 7.99% of filtered product revenue, while the top 20% of identified customers account for 77.24% of identified customer revenue.

Seasonal, country-level, and return-specific written observations should be checked against the final notebook outputs before publishing.
