📊 Bank Loan Analysis – End-to-End Data Analytics Project

A comprehensive analysis of bank loan data using SQL and Power BI, focused on understanding loan performance, borrower behavior, portfolio health, and key financial indicators.
This project demonstrates expertise in data cleaning, data modelling, SQL query writing, DAX understanding, KPI creation, and interactive dashboard building.

📁 Project Overview

The goal of this project is to analyze bank loan applications and evaluate the quality of issued loans.
Using SQL, all required metrics were generated, and a Power BI dashboard was created to visualize:

Monthly loan performance

Borrower characteristics

Good vs. bad loan distribution

Funding and repayment behavior

Key financial ratios (Interest Rate, DTI)

This project helps banks and analysts identify trends, manage credit risk, and monitor loan portfolio performance.

🏗️ Project Architecture
✔ Dataset

Includes fields such as:
Loan ID, Issue Date, Loan Amount, Interest Rate, Total Payment, Grade, Sub-grade, Employment Details, DTI, Loan Status, Purpose, State, Home Ownership.

✔ Tools Used

SQL (PostgreSQL-style queries) – To generate KPIs & summary tables

Power BI – Interactive dashboard

DAX – For modeling measures (if applied in the .pbit template)

🔍 Key Performance Indicators (KPIs)
📌 Loan Volume & Funding

Total Loan Applications

MTD (Month-to-date) Loan Applications

PMTD (Previous month-to-date) Loan Applications

Total Funded Amount

MTD & PMTD Funded Amount

📌 Collection & Repayment

Total Amount Received

MTD & PMTD Collection Amount

📌 Financial Ratios

Average Interest Rate

Average DTI (Debt-to-Income Ratio)

📌 Loan Quality Metrics

Good Loan Percentage

Bad Loan Percentage

Good Loan – Count, Funded Amount, Amount Received

Bad Loan – Count, Funded Amount, Amount Received

🧠 SQL Logic Overview

The SQL queries include:

✔ KPI Queries

Counts

SUM aggregations

Month-to-date (MTD) & PMTD filtering using EXTRACT(MONTH/YEAR)

Average calculations for Interest Rate & DTI

Good vs. Bad loan classification using loan_status

✔ Category-Level Analysis

Breakdowns were created for:

Loan Status

Month

State

Term

Employment Length

Purpose

Home Ownership

✔ Example Query Snippet
SELECT 
    EXTRACT(MONTH FROM issue_date) AS Month_Number,
    COUNT(id) AS Total_Loan_Applications,
    SUM(loan_amount) AS Total_Funded_Amount,
    SUM(total_payment) AS Total_Amount_Received
FROM Bank_loan
GROUP BY EXTRACT(MONTH FROM issue_date)
ORDER BY Month_Number;

🗂️ Data Terminologies (Simplified for Understanding)

A few important fields used in this analysis:

Loan ID

Unique identifier to track each loan.

Address State

Used to analyze geographical loan patterns & risk.

Employee Length

Indicates stability of borrower’s job history.

Grade & Sub-grade

Bank-assigned credit risk categories.

Loan Status

Shows whether a loan is Current, Fully Paid, Charged Off, etc.

DTI (Debt-to-Income Ratio)

Measures borrower’s repayment capacity.

Issue Date

Loan origination date used for trend analysis.

Interest Rate & Installment

Determine borrowing cost and repayment schedule.

📈 Dashboard Insights

The Power BI dashboard (created using your .pbit file) highlights:

🔹 1. Portfolio Summary

Total funded amount

Total collected amount

Loan performance summary

Monthly trends

🔹 2. Good vs. Bad Loans

Good Loan % vs Bad Loan %

Funding vs repayment comparison

Risk concentration

🔹 3. Borrower Insights

Loan distribution by:
✔ Purpose
✔ Employment Length
✔ Home Ownership
✔ State

🔹 4. Time-Based Trends

Monthly loan applications

Monthly funding amount

Monthly collection trends

📘 Project Learnings

During this project, I worked on:

✔ Writing optimized SQL queries
✔ Data modelling and ensuring relationship accuracy
✔ Building intuitive and interactive dashboards
✔ Understanding financial KPIs used by banks
✔ Interpreting loan behavior and repayment patterns
✔ Translating raw data into business insights

🏁 Conclusion

This project provides a complete overview of bank loan analytics, combining SQL analysis and Power BI visualization to deliver valuable insights into loan performance, credit risk, borrower behavior, and financial trends.

It showcases end-to-end data analytics capabilities suitable for portfolio monitoring, risk assessment, and financial reporting.
