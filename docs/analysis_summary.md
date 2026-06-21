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

The notebook includes placeholders for final findings and recommendations. These should be completed only after confirming the outputs from a clean top-to-bottom run.
