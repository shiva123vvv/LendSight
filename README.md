# LendSight — Loan Intelligence & Credit Risk Analytics

<p align="center">
  <strong>An Interactive Power BI Dashboard for Loan Portfolio Analysis</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI" />
  <img src="https://img.shields.io/badge/Microsoft-Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white" alt="Microsoft Excel" />
  <img src="https://img.shields.io/badge/DAX-Analytics-0078D4?style=for-the-badge" alt="DAX Analytics" />
</p>

---

## Project Overview

**LendSight** is an interactive financial analytics project developed using Microsoft Power BI to explore loan applications, funded amounts, recorded payment values, interest rates, debt-to-income (DTI) ratios and loan-status distributions.

The project transforms a structured synthetic loan dataset into an interactive report designed to demonstrate financial data analysis, KPI development, data modelling and business intelligence reporting.

The report contains two pages:

- **Summary:** Portfolio KPIs, Good/Bad loan classification, funded-versus-payment comparisons and loan-status analysis.
- **Overview:** Monthly application trends, loan-term distribution, home ownership, loan purpose and state-code distribution.

## Dashboard Preview

### Summary Dashboard

![LendSight Summary Dashboard](https://raw.githubusercontent.com/shiva123vvv/LendSight/main/Screenshots/dashboard.png)

### Overview Dashboard

![LendSight Overview Dashboard](https://raw.githubusercontent.com/shiva123vvv/LendSight/main/Screenshots/overview.png)

## Project Objectives

- Analyse overall loan application volume.
- Measure total funded principal and recorded payment values.
- Monitor average interest rates and debt-to-income ratios.
- Compare loan applications across status categories.
- Explore application trends and loan-purpose distributions.
- Examine loan terms and home-ownership categories.
- Present portfolio information through interactive Power BI visuals.

## Tools and Technologies

| Technology | Purpose |
|---|---|
| Microsoft Power BI Desktop | Dashboard design and interactive reporting |
| Microsoft Excel | Dataset storage |
| Power Query | Data import and transformation |
| DAX | Measures and analytical calculations |
| Git and GitHub | Version control and project presentation |

## Dashboard Pages

### 1. Summary

The Summary page provides a high-level view of the selected loan portfolio.

**Key Performance Indicators**

- Total Loan Applications
- Total Funded Amount
- Total Amount Received
- Average Interest Rate
- Average DTI Ratio

**Visualisations**

- Good Loan and Bad Loan application distribution
- Funded Amount versus Amount Received
- Application counts by loan status
- Average interest rate by loan status
- Average DTI ratio by loan status

**Purpose:** To compare loan-status groups, examine funding and recorded payment values, and review interest-rate and DTI patterns.

### 2. Overview

The Overview page explores application trends and portfolio segmentation.

**Visualisations**

- Monthly Loan Applications
- Loan Applications by State Code
- Loan Applications by Term
- Loan Applications by Home Ownership
- Loan Applications by Purpose

**Purpose:** To examine application activity over time and compare loan records across terms, housing categories and stated loan purposes.

The state-code values are synthetic. If the map visual is unavailable, a state-code bar chart can be used instead.

## Key Performance Indicators

| KPI | Calculation or interpretation |
|---|---|
| Total Loan Applications | Count of loan records |
| Total Funded Amount | Sum of `LOAN_AMOUNT` |
| Total Amount Received | Sum of `TOTAL_PAYMENT`; simulated values |
| Average Interest Rate | Average of `INT_RATE` |
| Average DTI Ratio | Average of `DTI` |
| Good Loan Applications | Count classified as Good under the project rule |
| Bad Loan Applications | Count classified as Bad under the project rule |

The report's figures respond to the active filters. See the Power BI report for the current values.

### Loan Status Classification

For this project, **Fully Paid** and **Current** records are grouped as Good Loan Applications. All other statuses are grouped as Bad Loan Applications.

This is a project-specific reporting rule, not a validated credit-risk policy or a universal banking standard.

## Dataset

The project uses a synthetic loan dataset stored in:

`LendSight_Synthetic_Loan_Data.xlsx`

| Dataset property | Detail |
|---|---|
| Power BI table | `financial_loan` |
| Records | 22,253 |
| Source columns | 23 |
| Date window | 2026–2027 |
| Data type | Synthetic practice data |

### Main Fields

The dataset includes:

- `ID` and `MEMBER_ID`
- `ISSUE_DATE`
- `PURPOSE`
- `GRADE` and `SUB_GRADE`
- `LOAN_STATUS`
- `HOME_OWNERSHIP`
- `EMP_LENGTH` and `EMP_TITLE`
- `ANNUAL_INCOME`
- `DTI`
- `INSTALLMENT`
- `TERM`
- `LOAN_AMOUNT`
- `INT_RATE`
- `TOTAL_PAYMENT`
- `TOTAL_ACC`
- `VERIFICATION_STATUS`
- `ADDRESS_STATE`
- `LAST_CREDIT_PULL_DATE`
- `LAST_PAYMENT_DATE`
- `NEXT_PAYMENT_DATE`

### Data Limitations

- The dataset contains synthetic records and does not represent actual borrowers.
- Dates were generated for 2026–2027 and do not establish real historical lending trends.
- State-code assignments are synthetic and must not be interpreted as verified borrower locations.
- `TOTAL_PAYMENT` is simulated and is not an audited repayment ledger.
- The source workbook does not explicitly define the currency unit.

These limitations should be considered when interpreting the dashboard.

## Data Model and DAX

The report uses the `financial_loan` table and a Calendar table for date-based analysis. A date relationship between `Calendar[Date]` and `financial_loan[ISSUE_DATE]` supports time-intelligence calculations.

### Core Measures

**Total Loan Applications**
```DAX
Total Loan Applications =
COUNTROWS(financial_loan)
```

**Total Funded Amount**
```DAX
Total Funded Amount =
SUM(financial_loan[LOAN_AMOUNT])
```

**Total Amount Received**
```DAX
Total Amount Received =
SUM(financial_loan[TOTAL_PAYMENT])
```

**Average Interest Rate**
```DAX
Average Interest Rate =
AVERAGE(financial_loan[INT_RATE])
```

**Average DTI Ratio**
```DAX
Average DTI Ratio =
AVERAGE(financial_loan[DTI])
```

These measures calculate values within the current filter context. Interest rate and DTI values should be formatted as percentages in Power BI.

## Report Interactivity

The report includes:

- Loan-grade filtering (A–G)
- Loan-purpose filtering
- Summary and Overview page navigation
- A Reset Filters bookmark
- Interactive visual filtering according to configured relationships and interactions

The reset button is intended to restore the saved default filter state.

## Repository Structure

```text
LendSight/
│
├── LendSight_Loan_Intelligence_Credit_Risk_Analytics.pbix
├── LendSight_Synthetic_Loan_Data.xlsx
├── LendSight_Project_Documentation_Final.pdf
├── README.md
└── Screenshots/
    ├── dashboard.png
    └── overview.png
```

The filenames and screenshot paths shown above should match the files committed to the repository.

## How to Use

1. Clone or download this repository.
2. Open `LendSight_Loan_Intelligence_Credit_Risk_Analytics.pbix` in Microsoft Power BI Desktop.
3. If prompted, update the Excel source path to `LendSight_Synthetic_Loan_Data.xlsx`.
4. Refresh the data if required.
5. Navigate between Summary and Overview.
6. Use the report filters and visuals to explore the dataset.

## Analytical Questions

LendSight can be used to investigate:

- How does application volume change over issue time?
- What is the total funded principal represented in the data?
- How do recorded payment values compare with funded amounts?
- Which loan purposes account for the largest application volumes?
- How are records distributed across loan terms and home-ownership categories?
- How do average interest rates and DTI ratios vary by loan status?
- How does the selected portfolio divide between the project's Good and Bad loan categories?

These are exploratory questions; findings should be derived from the actual report and interpreted within the dataset's limitations.

## Skills Demonstrated

- Power BI dashboard development
- DAX measures and KPI design
- Data preparation and modelling
- Interactive reporting and data visualisation
- Financial metric analysis
- Loan portfolio segmentation
- Git and GitHub project documentation

## Disclaimer

LendSight is an independent educational portfolio project. It is not affiliated with or endorsed by any bank or financial institution. The synthetic dataset and its calculated metrics are intended to demonstrate analytics techniques; they must not be used as evidence of real lending performance or as the sole basis for actual credit decisions.

---

<p align="center">
  <strong>LendSight — Turning Loan Data into Clearer Financial Insights</strong>
</p>
