# Real Estate Collection & Financial Risk Intelligence Dashboard

## Project Overview

An enterprise-grade Power BI dashboard designed to analyze real estate sales, installment collections, outstanding balances, and financial exposure across multiple projects.

The dashboard provides management with a unified view of sales performance, collection performance, project completion, cash exposure, and bank exposure.

---

## Business Problem

Real estate developers need to monitor installment-based sales and collections across multiple projects and payment channels.

The main challenges addressed by this project are:

- Tracking sold units across projects
- Monitoring collected and outstanding installment amounts
- Identifying due but unpaid installments
- Comparing Cash and Bank collections
- Analyzing bank-wise financial exposure
- Monitoring project completion
- Analyzing collection performance over time
- Providing a centralized management view across all projects

---

## Project Objectives

The dashboard aims to:

- Monitor total units and sold units
- Measure sales percentage
- Track invoiced amounts
- Track collected amounts
- Monitor outstanding balances
- Analyze collection rates
- Compare Cash vs Bank collections
- Analyze bank-wise exposure
- Monitor project completion
- Analyze collection trends by date
- Provide project-level financial insights

---

## Data Model

The project follows a dimensional modeling approach using:

### Fact Table

- `fact`

Contains sales and installment-level transactional data.

### Dimension Tables

- `DimCustomer`
- `DimUnit`
- `DimDate`

The model follows a star-schema structure with relationships between dimensions and the central fact table.

---

## Data Transformation

Data preparation was performed using Power Query.

Main transformation steps included:

- Removing unnecessary source rows
- Standardizing column names and data types
- Unpivoting installment columns
- Creating installment states
- Combining the eight project datasets
- Standardizing project names
- Adding adopted total units
- Creating customer and unit dimensions
- Creating a dedicated date dimension
- Handling null installment values
- Preparing the final analytical model

### Installment States

The installment lifecycle is classified into:

- `PAID`
- `DUE - NOT PAID`
- `NOT DUE`

---

## DAX Business Logic

Key measures include:

- Sold Count
- Sold %
- No of Units
- Project Completion %
- Issued Invoices
- Collected Invoices
- Outstanding Invoices
- Collection Rate
- Outstanding %
- Invoiced Amount
- Collected Amount
- Outstanding Amount
- Bank Collected Amount
- Bank Outstanding
- Bank Invoiced Amount
- Bank Sold Units
- Bank Sold %

---

## Dashboard Architecture

The report contains:

### Executive Pages

- Home
- Global Summary
- Collection By Date Summary

### Project Analysis

The dashboard contains detailed analysis for 8 real estate projects.

Each project includes:

- Overall
- Cash
- Bank
- Bank-Wise

This provides a structured project-level financial analysis.

---

## Key Analytical Areas

### Sales Performance

Analysis of:

- Total units
- Sold units
- Sales percentage
- Unit prices

### Collection Performance

Analysis of:

- Invoiced amounts
- Collected amounts
- Outstanding amounts
- Collection rate

### Financial Exposure

Analysis of:

- Cash outstanding
- Bank outstanding
- Bank-wise exposure

### Time Analysis

Analysis of:

- Historical records
- New records
- Collections by date
- Outstanding balances over time

### Project Performance

Analysis of:

- Project completion
- Sold units
- Collection performance
- Financial exposure

---

## Technologies Used

- Power BI
- Power Query
- DAX
- Excel
- Dimensional Data Modeling
- Data Visualization

---

## Dashboard Structure

```text
Real Estate Collection & Financial Risk Dashboard
│
├── Home
├── Global Summary
├── Collection By Date Summary
│
├── Project 1
│   ├── Overall
│   ├── Cash
│   ├── Bank
│   └── Bank-Wise
│
├── Project 2
│   ├── Overall
│   ├── Cash
│   ├── Bank
│   └── Bank-Wise
│
└── ... 8 Projects
