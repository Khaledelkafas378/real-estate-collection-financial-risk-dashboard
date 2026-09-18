# Real Estate Collection & Financial Risk Intelligence Dashboard

## Project Overview

An enterprise-style Power BI dashboard designed to analyze real-estate sales, installment collections, outstanding balances, banking exposure, and project performance across 8 real-estate projects.

The solution transforms raw installment data into an interactive financial intelligence dashboard that enables management to monitor collection performance, outstanding exposure, sales activity, and project-level financial performance.

---

## Business Problem

Real-estate developers manage large volumes of sales and installment data across multiple projects, customers, units, payment schedules, and financial channels.

Without a centralized analytical solution, it can be difficult to:

- Monitor collection performance
- Track outstanding installments
- Separate cash and bank exposure
- Analyze collection trends over time
- Compare project performance
- Identify due but unpaid installments

This project addresses these challenges through a centralized Power BI analytical solution.

---

## Project Objectives

The dashboard was designed to:

- Monitor total units and sold units
- Analyze sales performance across projects
- Track invoiced and collected amounts
- Measure outstanding balances
- Analyze Cash vs Bank exposure
- Monitor collection performance over time
- Analyze bank-level financial exposure
- Track project completion
- Support project-level financial analysis

---

## Projects Covered

The dashboard covers 8 real-estate projects:

1. One Kattameya Compound
2. Zahra North Coast
3. Degla Landmark
4. Skyline Katamya Compound
5. Degla Palms 6 October Compound
6. Lake Front 6
7. Crystal Plaza Maadi Compound
8. Rihana / Rayhanna Avenue

---

## Data Transformation

The raw project data was transformed using Power Query.

Main transformation steps included:

- Removing control rows
- Unpivoting installment columns
- Standardizing installment records
- Creating `Installment State`
- Adding `Project Name`
- Combining the 8 project datasets
- Creating dimension tables
- Adding adopted total units
- Preparing the data for analytical modeling

### Installment Lifecycle

Each installment is classified into one of three states:

| State | Meaning |
|---|---|
| PAID | Installment has been paid |
| DUE - NOT PAID | Installment is due but has not been paid |
| NOT DUE | Installment is not currently due |

This classification is used as the foundation for collection and outstanding calculations.

---

## Data Model

The project uses a dimensional data model centered around a fact table.

### Main Tables

- `fact`
- `DimCustomer`
- `DimUnit`
- `DimDate`

### Model Structure

```text
             DimCustomer
                  |
                  |
DimDate ------ fact ------ DimUnit
