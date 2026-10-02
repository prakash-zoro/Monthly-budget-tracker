# Monthly Budget Allocation & Balance Tracker

An Excel workbook that splits monthly income across spending categories
and shows how much is left in each one.

## Why I built it
I wanted to divide my income by goal instead of just recording expenses,
and know the balance remaining in each category at any point in the month.
I've used it every month for 6+ months.

## How it works
Everything sits on one sheet, "Monthly split", in two connected parts:

- **Summary table (A:D):** Category, Allocation, Total Spent, Balance
  (Allocation minus Total Spent), plus a TOTAL row.
- **Transaction log (G:I):** Category, Amount, Description.

Total Spent pulls from the log with
`=SUMIF($G$2:$G$102,A2,$H$2:$H$102)`, so every logged expense updates
the summary automatically.

## Features
- Category dropdown (data validation) so every entry matches a summary category
- Conditional formatting turns a Balance red when a category is overspent
- Room for about 100 transactions (rows 2 to 102)

## Categories
Petrol, Bills & Utilities, Investment, Entertainment, Food, Other Exps, Savings

## How to use
1. Enter your allocation for each category in column B.
2. Log each expense in columns G to I and pick the category from the dropdown.
3. Read the remaining balance in column D.

## Tools
Microsoft Excel: SUMIF, Data Validation, Conditional Formatting
