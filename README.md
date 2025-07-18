# Bank-Loan-Report-Dashboard-Using-Power-BI-and-MySQL
A complete data-driven loan reporting solution that analyzes bank loan performance using MySQL queries and Power BI dashboards to support decision-making, risk assessment, and operational insights.

📌 Project Overview:
This project builds a comprehensive Business Intelligence dashboard for bank loan analysis using Power BI integrated with MySQL. It visualizes key insights about loan applications, borrower demographics, loan performance, and repayment behavior.

The system comprises three core dashboards:

Overview Dashboard – high-level KPIs

Detailed Analysis Dashboard – borrower & loan breakdown

Summary Dashboard – region-wise and purpose-wise insights

🎯 Project Purpose:
Transform raw banking data into visual and analytical insights

Enable banks to monitor loan performance, optimize lending, and manage risk

Provide stakeholders with data-driven, actionable reporting

🧠 Objectives:
Analyze loan applications, funding trends, and repayment amounts

Profile borrowers based on income, employment, home ownership, and DTI

Evaluate loan statuses (Fully Paid, Current, Charged Off) for performance monitoring

Detect regional trends and optimize loan allocation strategies

Assess KPIs like interest rates, loan terms, and repayment behaviors

📊 Importance & Significance:
Promotes data-driven decision-making in loan processing and customer profiling

Helps detect early warning signs in loan defaults or regional risks

Improves operational efficiency through automated, visual reporting

Fosters a culture of analytics in the banking domain

🗂️ Dimensions & Key Features Analyzed:

Loan Status

Borrower Location (State)

Home Ownership Type

Employment Length and Title

Annual Income and DTI

Loan Purpose

Interest Rate and Loan Term

Dates: Issue Date, Last Payment, Next Payment

🧮 SQL KPIs & Queries Used(some example):

Total Loan Applications

SELECT COUNT(DISTINCT id) FROM finance_loan;
Monthly Loan Trends

SELECT MONTH(issue_date), COUNT(*) FROM finance_loan GROUP BY MONTH(issue_date);
Total Funded Amount, Avg. Interest Rate & DTI

SELECT SUM(loan_amount), AVG(int_rate), AVG(dti) FROM finance_loan;
Loan Status Summary


SELECT loan_status, COUNT(*), AVG(int_rate), SUM(loan_amount) FROM finance_loan GROUP BY loan_status;
Good vs Bad Loans Classification

Good: Fully Paid, Current

Bad: Charged Off

Purpose-wise, State-wise, and Home Ownership-wise Analysis

KPIs by borrower purpose, geography, home ownership

Aggregated interest rates, DTI, payment totals

All SQL queries used are provided in the SQL_QUERY_DOC.docx file.

🧾 Domain Knowledge Incorporated:

Explained how banks collect and use loan data

Discussed the entire loan approval process (Application → Disbursement → Monitoring)

Justified why analyzing loan data helps with:

Risk assessment

Fraud detection

Portfolio optimization

Customer insights

✅ Tools & Stack:

MySQL Workbench (Data extraction and transformation)

Power BI (Visualization and report building)

DAX & Power Query (Data modeling and calculations)

MS Word/Excel (Supporting documentation and schema tracking)
