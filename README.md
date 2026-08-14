# Banking Customer Analytics Project

This is my analysis of a banking dataset - I did the EDA in Python first, then building a Power BI dashboard on top of the cleaned data. Putting this together to practice the full workflow: raw data → cleaning/analysis → dashboard.

## About the dataset

'Banking.csv' has 3,000 retail bank customers with 25 columns covering their demographics (age, nationality, occupation), account activity (deposits, loans, credit cards, checking/savings), and some internal classification fields (loyalty tier, fee structure, risk weighting). No missing values anywhere and no duplicate client IDs, so it was already in decent shape to work with - didn't need to do any real cleanup beyond fixing the date format on Joined Bank (it was stored as text).

Each row is one customer, so this is basically a snapshot of the bank's customer base at a point in time - not transaction-level data, just account balances and profile info per person.

## Dataset

Files: [Banking.csv](https://github.com/user-attachments/files/30910750/Banking.csv)

3,000 rows, 25 columns, no missing data, no duplicate client IDs.

## What I did

1. Loaded the data and checked it over - shape, dtypes, nulls, duplicates
2. Converted Joined Bank from text to an actual date column
3. Went through each column individually to see how it's distributed - age, income, loyalty tiers, nationality, etc.
4. Started comparing columns against each other - income by loyalty tier, risk weighting vs age/income, a full correlation matrix across all the numeric fields
5. Ran an IQR-based outlier check on the financial columns to see which ones had extreme values
6. Tried PCA on 9 of the financial columns just to see if customers naturally separate into clusters
7. Exported the cleaned dataset plus a few summary tables (outliers, correlation matrix, PCA results, loyalty tier breakdown) so I could pull everything into Power BI
8. Built a 4-page dashboard in Power BI on top of that - Demographics, Financial Health, Risk & Loyalty, and Account Portfolio pages
