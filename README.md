# 📊 Tableau Dashboards

[![Tableau](https://img.shields.io/badge/Tableau-Desktop-blue?logo=tableau)](https://www.tableau.com/)

> Two interactive Tableau dashboards — a sales KPI scorecard with trend analysis and an HR workforce demographics explorer — built to practise Tableau's linked-filter, drill-down, and calculated field capabilities.

---

## 📋 Dashboards

### 💰 1. Sales KPI Dashboard
*(SALES.twbx)*

A multi-page sales analytics view with KPI scorecards, year-over-year comparison, and product / region breakdowns.

**Page 1 — Overview**

![Sales Page 1](https://raw.githubusercontent.com/rubenfm77/TABLEAU/main/P1.jpg)

**Page 2 — Detail**

![Sales Page 2](https://raw.githubusercontent.com/rubenfm77/TABLEAU/main/P2.jpg)

**What it covers:**
- Revenue and unit KPIs with period-over-period comparison
- Product category and sub-category breakdown
- Regional sales map with drill-down
- Monthly trend with seasonality reference lines

---

### 👥 2. HR Workforce Demographics Dashboard
*(HR Dashboard.twbx)*

An interactive view of workforce composition — headcount, attrition, department split, age distribution, and gender balance — designed for HR and management audiences.

![HR Dashboard](https://raw.githubusercontent.com/rubenfm77/TABLEAU/main/HR1.jpg)

**What it covers:**
- Total headcount with department filter
- Attrition rate by department and role
- Age band distribution
- Gender and marital status breakdown
- Tenure distribution (years at company)

---

## 🎯 Conclusions

**💰 Sales Dashboard: seasonality and product concentration**

The sales dashboard confirms the same patterns visible in the SQL and Power BI analyses built on similar datasets: **December is the peak month and February the trough**, with a consistent seasonal arc across years. Product concentration in the top category (bikes) is pronounced — the long tail of accessory and clothing SKUs contributes a small share of revenue but a disproportionate share of inventory complexity.

Year-over-year comparison shows strong Q4 performance but weak Q1 starts — a budgeting calibration problem rather than a structural revenue issue. The Tableau linked bar + line chart makes the deviation from average immediately visible at a glance, which is where the tool adds real value over static reports.

**👥 HR Dashboard: role-level granularity is where retention becomes actionable**

Aggregated attrition rates at the department level can obscure large within-department variation. The Tableau HR dashboard's linked filtering makes it easy to drill from "Sales department has 20% attrition" to "Sales Executives specifically have 30% attrition, while Sales Managers have 5%." This role-level granularity is where retention programmes become actionable — you don't run a single intervention for a whole department; you target the specific roles where the signal is concentrated.

The age distribution filter confirms that younger employees (under 30) dominate early attrition, consistent with the IBM HR ML analysis — but the Tableau view adds a visual dimension that static tables miss: the age-attrition curve is not monotonically declining. There is a secondary peak around the 40–45 age band, likely related to career-plateau and compensation-ceiling effects in mid-seniority roles.

**Tableau vs Power BI for this type of work**

Tableau's mark-level linking (clicking a bar highlights all related marks across all views) makes exploratory analysis faster than Power BI for datasets where the analyst doesn't yet know which cut matters. Power BI is stronger for production dashboards with complex DAX measures and tight data model requirements. For EDA and presentation, Tableau's drag-and-drop speed and visual polish are an advantage.

---

## 🛠️ Tech Stack

| Tool | Use |
|---|---|
| **Tableau Desktop** | Dashboard authoring and calculated fields |
| **Tableau packaged workbooks (.twbx)** | Self-contained files with embedded data |
| **Calculated fields** | KPI deltas, attrition rate, age bands |
