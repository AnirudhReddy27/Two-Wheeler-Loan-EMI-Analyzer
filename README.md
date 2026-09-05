# Two-Wheeler Loan & EMI Analyzer (Excel)

An Excel-based financial modeling project that compares two-wheeler loan offers across multiple Indian lenders, builds a full EMI amortization schedule, simulates loan prepayment scenarios, and visualizes everything on a KPI dashboard.

## Why this project

Built as a practical, formula-driven complement to my SQL and Python analytics projects — this one focuses on core Excel financial-modeling skills: `PMT`, `INDEX`/`MATCH`, data validation, dynamic charts, and scenario simulation, all without a single hardcoded result.

The scenario: financing a mid-capacity motorcycle (~₹4,00,000 on-road price, in line with bikes like the Aprilia Tuono 457) and deciding which lender offers the best deal.

## Workbook structure

| Sheet | Purpose |
|---|---|
| **Inputs** | Loan terms (principal, rate, tenure, processing fee) for 5 lenders, plus a live cost-comparison table (EMI, total payment, total interest per lender) |
| **Amortization** | Full month-by-month EMI schedule for a lender selected via dropdown — interest, principal, and closing balance recalculate instantly when you switch lenders |
| **Prepayment Simulator** | What-if analysis: enter a lump-sum prepayment amount and month, see the revised schedule, months saved, and total interest saved vs. no prepayment |
| **Dashboard** | KPI cards (best lender, lowest interest, selected lender's totals, interest saved) and 3 charts: total interest by lender, outstanding balance over time, principal vs. interest per month |

## Key formulas & features

- `PMT`, `INDEX`/`MATCH` for dynamic lender lookups (no `XLOOKUP`, for broad Excel-version compatibility)
- Data validation dropdowns driving cross-sheet calculations
- Tenure-reduction prepayment logic — EMI stays fixed, loan term shortens
- Color-coded cells: blue = editable inputs, black = formulas, green = cross-sheet links
- Fully dynamic charts sourced directly from formula-driven ranges

## Sample findings (illustrative data)

Across 5 lenders on a ₹4,00,000 / 36-month loan:

- **Cheapest option:** State Bank of India (~₹59,593 total interest)
- **Most expensive option:** Bajaj Finance (~₹74,854 total interest) — a difference of over ₹15,000 for the same principal and tenure
- A ₹20,000 prepayment in month 6 shortens the loan by 1 month and saves roughly ₹5,200 in interest (SBI scenario)

> Note: Lender names, rates, and fees are illustrative figures for demonstration purposes, not live market quotes.

## Tools used

Excel (formulas, data validation, charts) · openpyxl (for programmatic generation)

## Files

- `Two_Wheeler_Loan_Analyzer.xlsx` — the workbook

## Related projects

- [AutoPulse — Indian Two-Wheeler Dealership Analytics](https://github.com/AnirudhReddy27/AutoPulse-Indian-Two-Wheeler-Dealership-Analytics) (SQL)
- [India CPI Inflation EDA](https://github.com/AnirudhReddy27) (Python/EDA)
- TriGuna Tracker (Python CLI)
