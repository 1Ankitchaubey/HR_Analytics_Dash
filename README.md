# HR Analytics Power BI Dashboard

An interactive **HR Analytics dashboard built in Microsoft Power BI** for analyzing employee workforce, attrition, salary, job roles, satisfaction, demographics, and experience.

> **Portfolio note:** This repository is a learning and enhancement version based on an existing HR Analytics project. The original creator is credited below. The repository documentation has been rewritten and organized for portfolio use.

## 📌 Project Overview

The dashboard is designed to help HR teams answer questions such as:

- How many employees are active and how many have left?
- Which departments show higher attrition?
- How does attrition vary by salary slab?
- Which job roles and satisfaction levels are associated with attrition?
- Which age groups have higher attrition?
- How does attrition differ by gender and experience?
- Which departments have the largest workforce?

## 🎯 Objectives

- Analyze overall employee workforce data
- Monitor attrition count and attrition rate
- Compare attrition across departments
- Analyze salary-slab patterns
- Analyze job role and satisfaction
- Study age-group and gender patterns
- Analyze experience-related attrition
- Support data-driven HR retention decisions

## 🛠️ Tools & Technologies

- **Microsoft Power BI**
- **Power Query** – data preparation and transformation
- **DAX** – KPI and analytical calculations
- **CSV/Excel data**
- **Data Visualization**
- **Exploratory Data Analysis**

## 📊 Current Dashboard Components

The supplied PBIX contains a dashboard page with:

- Total Employees KPI
- Active Employees KPI
- Attrition Count KPI
- Attrition Rate KPI
- Average Age KPI
- Average Experience/Tenure KPI
- Attrition by Department
- Attrition by Salary Slab
- Job Role & Satisfaction matrix
- Age Group Distribution
- Attrition by Gender
- Attrition Trend by Experience
- Department-wise Employee Count
- Department slicer
- Age Group slicer

## 🔎 Dataset Snapshot

The supplied dataset contains **1,480 employee records** and **37 columns**.

Calculated from the supplied dataset:

| Metric | Value |
|---|---:|
| Total records | 1,480 |
| Attrition | 241 |
| Active employees | 1,239 |
| Overall attrition rate | 16.28% |
| Average age | 36.94 |
| Average total experience | 11.28 years |

**Important:** The dashboard screenshot currently shows an **Age Group filter selection**, so the KPI values visible in the screenshot should not be interpreted as the unfiltered dataset totals.

## 💡 Dataset-Level Insights

Based on the supplied dataset:

- **Human Resources** has the highest department-level attrition rate among the listed departments (26.8%), followed by **Sales** (25.2%).
- The **18–25** age group has the highest attrition rate (36.6%).
- The **10+ LPA** salary slab has the highest attrition rate (19.2%) in this dataset.
- Overall attrition in the supplied dataset is **16.28%**.

These are descriptive findings from this dataset and should not be treated as causal conclusions.

## 📈 Planned Portfolio Enhancements

The next analytical version can add:

1. Retention Rate KPI
2. Active Employee KPI based on a transparent DAX definition
3. Age Group calculated column/logic
4. Salary Slab validation
5. Department/Job Role attrition-rate measures
6. Additional slicers for Gender, Job Role, OverTime and Business Travel
7. Tooltip pages for deeper analysis
8. A dedicated **Executive Summary** page
9. A dedicated **Attrition Drivers** page
10. Data-cleaning documentation in Power Query

See [`POWER_BI_ENHANCEMENT_GUIDE.md`](POWER_BI_ENHANCEMENT_GUIDE.md) for the exact suggested DAX and visual changes.

## 🖼️ Dashboard Preview

![HR Analytics Dashboard](Dashboard/HR_Analytics_Dashboard.png.png)

## 📁 Project Structure

```text
HR-Analytics-PowerBI-Dashboard/
│
├── README.md
├── POWER_BI_ENHANCEMENT_GUIDE.md
│
├── PowerBI/
│   └── HR_Analytics_Dashboard.pbix.pbix
│
├── Dashboard/
│   └── HR_Analytics_Dashboard.png.png
│
├── Dataset/
│   └── HR_Analytics_Dataset.xlsx.csv
│
└── Documentation/
    └── HR_Analytics_Project_Documentation.pdf
```


## 👨‍💻 Portfolio Usage

For a resume/portfolio, describe the project accurately. Do **not** claim that all planned enhancements were implemented until they have actually been added to the PBIX.

Suggested resume wording after completing the enhancements:

> **HR Analytics Power BI Dashboard** — Built and enhanced an interactive HR analytics dashboard using Power BI, Power Query and DAX to analyze employee attrition, salary, department, job role, satisfaction, demographics and experience, with KPI-driven reporting and business insights.

## 📄 License / Attribution

Before publishing or distributing modified versions, review the original repository's license and attribution requirements. If no license is provided, keep the original creator credit and treat the source as a reference rather than assuming broad redistribution rights.
