# Integrated 3-Statement Financial Model

A fully linked Income Statement, Balance Sheet, and Cash Flow Statement built in Excel,
including a circular debt schedule and a DSO/DIO/DPO-driven working capital build.

## What this demonstrates

- Full 3-statement integration: every line on the Balance Sheet and Cash Flow
  Statement is formula-linked back to the Income Statement, not hardcoded.
- Circular debt schedule: Interest Expense depends on the average revolver balance,
  which depends on Cash Flow Available, which depends on Net Income, which depends
  on Interest Expense. Requires iterative calculation enabled in Excel
  (File > Options > Formulas > Enable iterative calculation).
- Cash sweep mechanic: the revolver draws when cash falls short of a minimum
  balance, and pays down automatically when there's surplus cash.
- Working capital schedule: Accounts Receivable, Inventory, and Accounts Payable
  driven by Days Sales Outstanding, Days Inventory Outstanding, and Days Payable
  Outstanding, rather than flat percentage-of-revenue assumptions.
- Balance sheet integrity check: Total Assets equals Total Liabilities plus Total
  Equity in every forecast period, confirming the model is internally consistent.

## Structure

| Section | What it covers |
|---|---|
| Operating Assumptions | Revenue growth, margins, tax rate, DSO/DIO/DPO, interest rate |
| Income Statement | Revenue through Net Income, 5-year forecast |
| Working Capital Schedule | AR, Inventory, AP, Net Working Capital |
| Cash Flow Statement | Operating, Investing, and Financing cash flows |
| Debt Schedule | Revolver balance, draws, paydowns, average balance for interest |
| Balance Sheet | Full balance sheet with an integrity check row |

## Note on the data

Figures in this model are illustrative placeholders built for practice purposes.
They are not the actual reported financials of any real company.

## Tools

Built in Microsoft Excel. Requires iterative calculation enabled to resolve the
circular reference between the Income Statement and the Debt Schedule.
