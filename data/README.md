# Data Folder

This project expects the Online Retail II dataset to be available locally.

## Required Dataset

- Dataset name: Online Retail II
- Source identified in the existing project documentation: UCI Machine Learning Repository
- Expected local file path: `data/raw/online_retail_II.xlsx`

The notebook expects the Excel file to contain the following worksheets:

- `Year 2009-2010`
- `Year 2010-2011`

## Why Data Files Are Not Included

Raw and processed data files can be large and should not be uploaded to GitHub. Keeping them out of the repository avoids unnecessary storage use and reduces the risk of publishing files that should remain local.

The `.gitignore` file excludes common raw and processed data formats in the `data/` folder.

## Local Setup

Create the following local folder structure:

```text
data/
├── README.md
└── raw/
    └── online_retail_II.xlsx
```

Then open `notebooks/uk_online_retail_pandas_analysis.ipynb` and run the cells from top to bottom.
