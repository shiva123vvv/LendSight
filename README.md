# LendSight — Loan Intelligence & Credit Risk Analytics

<p align="center">
  <strong>A Power BI Analytics Project for Loan Portfolio Monitoring, Lending Performance, and Credit Risk Insights</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI" />
  <img src="https://img.shields.io/badge/Microsoft-Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white" alt="Microsoft Excel" />
  <img src="https://img.shields.io/badge/Analytics-Financial%20Data-0078D4?style=for-the-badge" alt="Financial Analytics" />
</p>

---

## 📌 Project Overview

**LendSight** is an interactive financial analytics dashboard developed using Microsoft Power BI to explore loan applications, funded amounts, repayments, interest rates, debt-to-income ratios, and loan portfolio quality.

The project transforms a structured loan dataset into an interactive reporting experience that helps users understand lending activity, monitor portfolio performance, and compare good and bad loan categories.

The dashboard is organized into two main pages:

- **Summary:** High-level lending performance and portfolio distribution.
- **Overview:** Loan quality indicators and detailed lending metrics.

This project demonstrates practical skills in financial data analysis, dashboard design, data visualization, and business intelligence reporting.

## 🎯 Project Objectives

- Analyze overall loan application activity.
- Monitor total funded amounts and repayments received.
- Understand average interest rates and debt-to-income ratios.
- Compare good loan and bad loan categories.
- Examine loan status distributions and lending trends.
- Explore loan purposes, employment information, home ownership, and geographic distributions.
- Present financial information through clear and interactive Power BI visuals.

## 🛠️ Tools and Technologies

| Tool | Purpose |
|---|---|
| Microsoft Power BI Desktop | Dashboard development and data visualization |
| Microsoft Excel | Dataset storage and data preparation |
| Power Query | Data import and transformation, where applicable |
| DAX | Measures and calculated metrics, where applicable |
| Git and GitHub | Project versioning and portfolio presentation |

## 📊 Dashboard Pages

### 1. Summary Dashboard

The Summary page provides a high-level view of loan portfolio activity.

**Key metrics**
- Total Loan Applications
- Total Funded Amount
- Total Amount Received
- Average Interest Rate
- Average DTI Ratio

**Visualizations**
- Loan application trends by month
- Loan distribution by term
- Loan distribution by home ownership
- Loan purpose analysis using a treemap
- Geographic loan distribution visual

**Business value**

This page helps users identify changes in loan application activity, understand the distribution of lending products, and examine differences across loan categories.

### 2. Overview Dashboard

The Overview page focuses on loan quality and lending performance.

**Key metrics and analysis**
- Good Loan Applications
- Bad Loan Applications
- Funded amount and repayment analysis
- Loan applications by loan status
- Average interest rate
- Average debt-to-income ratio

**Business value**

This page helps users compare portfolio categories, examine loan status patterns, and understand the relationship between loan funding, repayments, interest rates, and borrower DTI.

## 📈 Key Performance Indicators

| KPI | Description |
|---|---|
| Total Loan Applications | Number of loan applications represented in the dataset |
| Total Funded Amount | Total amount funded through loans |
| Total Amount Received | Total repayment amount recorded in the dataset |
| Average Interest Rate | Average recorded interest rate across the relevant loans |
| Average DTI Ratio | Average recorded debt-to-income ratio |
| Good Loan Applications | Applications classified in the project's good-loan category |
| Bad Loan Applications | Applications classified in the project's bad-loan category |

*Exact totals depend on the dataset and report filters. The dashboard should be consulted for current values.*

## 🗂️ Project Structure

```text
LendSight/
│
├── LendSight_Loan_Intelligence_Credit_Risk_Analytics.pbix
├── LendSight_Synthetic_Loan_Data.xlsx
├── LendSight_Project_Guide.pdf
├── README.md
└── Screenshots/
    ├── Summary.png
    └── Overview.png
```

*The screenshot filenames above are suggested names. Use the actual filenames present in your Screenshots folder.*

## 📁 Dataset

The project uses a structured loan dataset containing fields associated with loan applications, borrowers, employment, loan terms, interest rates, and repayment information.

Example fields include:

- Loan ID and member ID
- Issue date
- Loan purpose and status
- Loan grade and sub-grade
- Home ownership
- Employment information
- Annual income
- Debt-to-income ratio
- Loan amount and installment
- Interest rate
- Total payment
- Last payment date and next payment date

**Data disclosure:** The included file `LendSight_Synthetic_Loan_Data.xlsx` is synthetic data prepared for this portfolio project. It is not a real bank's customer database and should not be interpreted as actual borrower or lending performance.

## 🔍 Analytical Questions

The dashboard is designed to explore questions such as:

1. How does loan application activity change over time?
2. What is the total value of loans funded?
3. How does the amount received compare with the amount funded?
4. Which loan purposes account for the largest application volumes?
5. How are applications distributed across loan terms and home ownership categories?
6. How do average interest rates and DTI ratios vary across loan statuses?
7. How does the portfolio divide between the project's good-loan and bad-loan categories?
8. Which loan statuses contribute most to overall application volume?

## 💡 Business Applications

The analytical approach demonstrated in this project can support:

- Lending performance reporting
- Portfolio monitoring
- Loan category analysis
- Financial KPI reporting
- Repayment trend analysis
- Management dashboards
- Data-driven discussions about portfolio quality

The report is an educational analytics project. It does not make automated credit decisions or provide validated predictions of borrower default risk.

## 🚀 How to Use the Project

1. Download or clone this repository.
2. Open `LendSight_Loan_Intelligence_Credit_Risk_Analytics.pbix` using Microsoft Power BI Desktop.
3. If prompted, update the Excel data source path to the location of `LendSight_Synthetic_Loan_Data.xlsx`.
4. Refresh the dataset if required.
5. Navigate between the Summary and Overview pages.
6. Interact with the report's filters and visuals to explore the data.

## 📷 Dashboard Screenshots

### Summary Dashboard

```markdown
![LendSight Summary Dashboard](https://raw.githubusercontent.com/shiva123vvv/LendSight/main/Screenshots/dashboard.png)
```

### Overview Dashboard

```markdown
![LendSight Loan Portfolio Overview](https://raw.githubusercontent.com/shiva123vvv/LendSight/main/Screenshots/overview.png)
```

## 📚 Skills Demonstrated

- Financial data analysis
- Business intelligence reporting
- Power BI dashboard development
- KPI design and interpretation
- Data visualization
- Loan portfolio analysis
- Credit risk reporting concepts
- Excel-based data handling
- Financial metric interpretation
- Portfolio documentation using GitHub

## 🔮 Future Enhancements

Potential future improvements include:

- Additional time-based comparisons
- Improved geographic visualizations
- More detailed loan-status drill-through
- Enhanced tooltip pages
- Automated data-refresh configuration
- Additional portfolio quality measures
- Scenario analysis and forecasting, with appropriate validation

These are potential enhancements and should not be considered implemented unless they are added to the project.

## ⚠️ Disclaimer

LendSight is an independent educational portfolio project developed for learning and demonstration purposes. The included dataset is synthetic. The dashboard is not affiliated with, endorsed by, or developed for any bank or financial institution.

The analysis is intended to demonstrate business intelligence techniques and should not be used as the sole basis for real lending, investment, or credit decisions.

## 👨‍💻 Author

**LendSight — Loan Intelligence & Credit Risk Analytics**

Developed as a portfolio project to demonstrate practical financial analytics and Power BI reporting skills.

---

<p align="center">
  <strong>Turning loan data into clearer financial insights.</strong>
</p>
