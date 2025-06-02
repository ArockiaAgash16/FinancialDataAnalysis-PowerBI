# 📊 End-to-End Financial Risk and Loan Default Analytics Solution using Power BI Dataflows and SQL Server

## 📌 Overview

This project delivers a **Financial Risk Metrics Dashboard** using **Power BI**, integrating data from an **on-premises SQL Server** via **Power BI Dataflow** and a **Data Gateway**. The dashboard visualizes key loan-related metrics, providing insights into loan disbursement trends, default rates, and risk profiles based on borrower demographics.

---

## 🎯 Key Objectives

- Track **Year-over-Year (YOY) changes** in loan amounts and default rates.
- Analyze **loan distribution by credit score, income bracket, and employment type**.
- Build a **centralized and reusable dataflow** to standardize data transformation.
- Ensure **secure and reliable access to on-premises data sources** through a **Power BI Gateway**.

---

## 📡 Data Pipeline

- **Source**: MS SQL Server Database (`loan` database)
- **ETL Layer**: Power BI Dataflow (Gen1)
- **Access Medium**: On-premises Data Gateway (Standard Mode)
- **Report Layer**: Power BI Desktop (`.pbix` file)

---

## 🔌 Connection Workflow

1. **Install and configure On-premises Data Gateway (Standard Mode)** to bridge on-prem SQL Server with Power BI Service.
2. **Prepare SQL Server database and tables** using SQL Server Management Studio (SSMS).
3. **Create a Power BI Dataflow** in Power BI Service connecting to the SQL Server via the gateway.
4. **Load and transform data centrally** in the Dataflow.
5. **Consume the Dataflow in Power BI Desktop** for building visuals and reports.

📄 Detailed instructions for this are available in:
- `/gateway-setup/Gateway_Installation_and_Config.md`
- `/dataflow-setup/PowerBI_Dataflow_Setup.md`

---

## 📊 Visualizations and Rationale

### 📊 Tab 1 — Loan Default & Overview
| Chart | Type | Description |
|:-------|:------------|:--------------|
| Loan Amount by Purpose | Line Area Chart (Step) | Loan disbursement trends by purpose. |
| Avg Income by Employment Type | Line Area Chart (Step) | Compare average applicant incomes. |
| Default Rate % by Employment Type | Line Area Chart (Step) | Proportion of defaults per employment type. |
| Average Loan by Age Group | Line Area Chart | Average loan amounts by age groups. |
| Default Rate % by Year | Line Area Chart | Default trends year-over-year. |

---

### 📊 Tab 2 — Applicant Demographics & Financial Profile
| Chart | Type | Description |
|:-------|:------------|:--------------|
| Median Loan Amount by Credit Score Category | Line Area Chart | Central tendency of loans across credit bands. |
| Average Loan Amount (High Credit) by Age & Marital Status | Donut Chart | High-credit loans distribution. |
| Total Loans (Adults) by Credit Score Category | Line Area Chart | Adult applicants' loan disbursement patterns. |
| Loan (Middle Age Adults) with Mortgage/Dependents | Clustered Column Chart | Loan distribution by dependents and mortgage status. |
| Number of Loans by Education Type | Line Area Chart | Loan counts per education type. |

---

### 📊 Tab 3 — Financial Risk Metrics
| Chart | Type | Description |
|:-------|:------------|:--------------|
| YOY Loan Amount Change (%) by Year | Line Area Chart | Annual loan growth trends. |
| YOY Default Loans Change (%) by Year | Line Area Chart | Annual default rate fluctuations. |
| YOY Loan Amount by Credit Score Category and Marital Status | Ribbon Chart | Trend comparison by risk and marital status. |
| Loan Amount by Income Bracket and Employment Type | Decomposition Tree | Interactive risk breakdown. |

---

## 📐 DAX Measures Used

Key DAX calculations created for the report:

Columns:

- **Year Extraction**
- **Income Brackets**
- **Credit Score Bins**
- **Age Groups**
  
Measures for the Tab 1

- **Average Income by Employment Type**
- **Average Loan by Age Group**
- **Default Rate by Employment Type**
- **Default Rate by Year**
- **Loan Amount by Purpose**

Measures for the Tab s

- **Average Loan Amount (High Credit Scores)**
- **Loan Counts by Education Type**
- **Median Loan Amount**
- **Total Loan by Credit Score Category**
- **Total Loan by Age Group (Middle Adults)**
  
Measures for the Tab 3

- **YOY Default Loans Change (%)**
- **YOY Loan Amount Change (%)**
- **YTD Loan Amount**

📄 Full DAX definitions are available in:
- `/dax-measures/FinancialMetrics_DAX_Measures.txt`

---

## 📸 Live Report

(https://app.powerbi.com/view?r=eyJrIjoiYzgxODNiZjYtZjdlYS00M2EzLWEyNzUtOGQ0NGQxOTkwMTI5IiwidCI6IjE0YzAyY2YxLWE4ZjYtNGI3My1iMmNjLTQ0YTM0MjE5N2FiZiJ9)

---

## 📎 Dependencies & Requirements

- Power BI Desktop (latest version)
- Power BI Service (Pro/Premium)
- MS SQL Server (2019+ recommended)
- On-Premises Data Gateway (Standard Mode)
- SQL Server Management Studio (SSMS)

---
