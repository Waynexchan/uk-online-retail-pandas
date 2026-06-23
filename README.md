# UK Online Retail Pandas Analysis

## Project Summary

This project uses Python, pandas, and Jupyter Notebook to analyse UK online retail transaction data. The analysis explores revenue trends, customer behaviour, product performance, country-level patterns, returns, cancellations, and practical business observations.

## Purpose of This Repository

This is a standalone Python / pandas exploratory data analysis project. It complements, but is separate from, my main UK Retail Power BI / BigQuery dashboard project.

This repository demonstrates how I can use Python and pandas to clean, explore, analyse, and communicate insights from transactional retail data.

## Business Problem

A retail business wants to understand sales performance, customer behaviour, product performance, and transaction patterns using historical order data.

The analysis is designed to answer practical commercial questions about revenue trends, customer concentration, product performance, country contribution, and data quality issues that need to be handled before reporting.

## Key Questions

- How does revenue change over time?
- Which products generate the most revenue?
- Which customers contribute the most revenue?
- Which countries contribute the most revenue?
- Are sales concentrated among a small number of customers or products?
- What data quality issues need to be considered before analysis?
- What return or cancellation patterns should be reviewed separately from valid sales?

## Dataset Overview

The project uses the Online Retail II dataset, identified in the existing project documentation as sourced from the UCI Machine Learning Repository.

Main fields used:

- Invoice number
- Stock code
- Product description
- Quantity
- Invoice date
- Unit price
- Customer ID
- Country

The raw dataset is not intended to be uploaded to GitHub. See [data/README.md](data/README.md) for local setup instructions.

## Tools Used

- Python
- pandas
- Jupyter Notebook
- matplotlib
- openpyxl

## Data Cleaning and Preparation

The notebook performs and documents the following preparation steps:

- loaded the two yearly worksheets from the Excel dataset
- standardised column names
- checked dataset shape, data types, missing values, and duplicate rows
- converted invoice dates to datetime format
- converted customer IDs to a nullable integer type where available
- converted stock codes to text
- created a revenue field from quantity and price
- separated valid sales from cancellations and returns
- filtered invalid quantity and price values for sales analysis
- created month fields for time-based analysis
- prepared grouped datasets for product, customer, country, and return analysis

## Analysis Performed

- revenue trend analysis
- monthly sales analysis
- top product analysis
- top customer analysis
- country-level revenue analysis
- customer revenue concentration
- product revenue concentration
- cancellation and return review

## Key Findings

- The combined raw dataset contains 1,067,371 rows before filtering.
- After excluding cancellations/returns and non-positive quantity or price values, the valid sales dataset contains 1,041,670 rows.
- The top 10 filtered product codes account for 7.99% of filtered product revenue.
- The top 20% of identified customers account for 77.24% of identified customer revenue.
- Additional seasonal, country-level, and returns observations should be confirmed from the final notebook outputs before publishing.

These findings are based on a local validation run of `notebooks/uk_online_retail_pandas_analysis.ipynb`. Final written observations should still be checked against a fresh top-to-bottom notebook run before GitHub publication.

## Business Recommendations

- Monitor revenue trends by month to identify seasonal changes.
- Review customer concentration risk, especially among high-value accounts.
- Identify top products for stock planning, sales planning, and commercial review.
- Investigate returns or cancelled invoices separately from valid sales.
- Use customer and product insights to support commercial decision-making.

## Limitations

- The dataset is historical only.
- The dataset does not include marketing cost data.
- The dataset does not include customer demographic data.
- Returns and cancelled invoices require careful handling.
- Product descriptions may need further standardisation.
- Findings should be validated with additional business context before being used for business decisions.

## Future Improvements

- Add RFM customer segmentation.
- Add cohort analysis.
- Add automated data validation checks.
- Compare pandas results with the Power BI / SQL version.
- Convert repeated analysis steps into reusable Python functions.
- Add more visualisations.

## Repository Structure

```text
uk-online-retail-pandas-analysis/
├── README.md
├── CHANGELOG.md
├── github_publish_checklist.md
├── requirements.txt
├── notebooks/
│   ├── uk_online_retail_pandas_analysis.ipynb
│   ├── 01_data_check.ipynb
│   ├── 02_sales_trend.ipynb
│   ├── 03_top_products_customers.ipynb
│   └── 04_cancellations_returns.ipynb
├── docs/
│   ├── business_problem.md
│   ├── data_cleaning_steps.md
│   ├── analysis_summary.md
│   └── limitations.md
├── assets/
│   └── screenshots/
└── data/
    └── README.md
```

## How to Run

1. Clone the repository.
2. Install the required packages:

```bash
pip install -r requirements.txt
```

3. Download the Online Retail II dataset and place the Excel file in `data/raw/online_retail_II.xlsx`.
4. Open `notebooks/uk_online_retail_pandas_analysis.ipynb`.
5. Run the cells from top to bottom.

Raw and processed data files should stay local and should not be committed to GitHub.
