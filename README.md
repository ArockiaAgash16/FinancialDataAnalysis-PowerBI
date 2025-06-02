# 📊 End-to-End Financial Risk and Loan Default Analytics Solution using Power BI Dataflows and SQL Server

## 📌 Overview

This project delivers a **Financial Risk Metrics Dashboard** using **Power BI**, integrating data from an **on-premises SQL Server** via **Power BI Dataflow** and a **Data Gateway**. The dashboard visualizes key loan-related metrics, providing insights into loan disbursement trends, default rates, and risk profiles based on borrower demographics.

---

## 🔌 Data Connection & Transformation Workflow

1. **On-Premises Data Gateway**: Installed and configured in Standard Mode to securely bridge Power BI Service with the on-premises SQL Server.
2. **SQL Server Database**: A `loan` database created in SSMS and populated via flat file import.
3. **Power BI Dataflow (Gen1)**: 
   - Connected to SQL Server via Gateway.
   - Transformed and loaded loan data.
4. **Power BI Desktop**: Connected to the Dataflow, performed additional data modeling, DAX calculations, and report building.

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

## 📌 Expected Outcomes

- Centralized, reusable Dataflow architecture.
- Power BI dashboards to analyze loan default trends, applicant financial health, and financial risks.
- Simplified report refresh and scalability for enterprise scenarios.

---

## 📸 Live Report

(https://app.powerbi.com/view?r=eyJrIjoiYzgxODNiZjYtZjdlYS00M2EzLWEyNzUtOGQ0NGQxOTkwMTI5IiwidCI6IjE0YzAyY2YxLWE4ZjYtNGI3My1iMmNjLTQ0YTM0MjE5N2FiZiJ9)

---

## 🛠️ Tech Stack & Tools

- **Power BI Service (Cloud)**
- **Power BI Dataflows (Gen1)**
- **On-Premises Data Gateway (Standard Mode)**
- **SQL Server Management Studio (SSMS)**
- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
