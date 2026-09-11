# Power BI Enhancement Guide

This file is the implementation plan for converting the supplied dashboard into a stronger personal portfolio project.

## 1. First: Make a backup

Keep the original PBIX untouched. Work on a copy in Power BI Desktop.

## 2. Recommended KPI measures

The supplied PBIX model references a table named `HR_Analytics-4`. If your Power BI model shows a different table name, replace it accordingly.

```DAX
Total Employees =
COUNTROWS('HR_Analytics-4')
```

```DAX
Attrition Count =
CALCULATE(
    COUNTROWS('HR_Analytics-4'),
    'HR_Analytics-4'[Attrition] = "Yes"
)
```

```DAX
Active Employees =
CALCULATE(
    COUNTROWS('HR_Analytics-4'),
    'HR_Analytics-4'[Attrition] = "No"
)
```

```DAX
Attrition Rate =
DIVIDE(
    [Attrition Count],
    [Total Employees],
    0
)
```

```DAX
Retention Rate =
DIVIDE(
    [Active Employees],
    [Total Employees],
    0
)
```

```DAX
Average Age =
AVERAGE('HR_Analytics-4'[Age])
```

```DAX
Average Total Experience =
AVERAGE('HR_Analytics-4'[TotalExperience(Years)])
```

Format `Attrition Rate` and `Retention Rate` as Percentage.

## 3. Recommended new slicers

Add slicers for:

- Gender
- Job Role
- OverTime
- Business Travel
- Marital Status
- Education Field

Keep Department and Age Group slicers.

## 4. Recommended new visuals

### Visual A — Attrition Rate by Department
- Axis: Department
- Value: Attrition Rate
- Sort descending

### Visual B — Attrition Rate by Job Role
- Axis: JobRole
- Value: Attrition Rate
- Sort descending

### Visual C — Attrition by OverTime
Use a clustered column/bar chart:
- Axis: OverTime
- Values: Attrition Count / Total Employees as appropriate

### Visual D — Retention vs Attrition
Use a donut or stacked bar:
- Attrition = Yes/No
- Employee count

### Visual E — Tenure Analysis
Use `YearsatCompany` or `TotalExperience(Years)` with Attrition Count/Rate.

## 5. Data quality checks

In Power Query:

1. Check data types.
2. Check duplicate EmpID values.
3. Check null/blank values.
4. Validate Attrition values are only Yes/No.
5. Validate Gender, Department and SalarySlab categories.
6. Remove accidental blank rows.
7. Rename unclear columns only when it does not break existing model references.
8. Document every transformation.

## 6. Important issue found in the current preview

The supplied dashboard screenshot has an AgeGroup selection active. Therefore the KPI values shown in that screenshot represent the selected filter context rather than necessarily the full dataset.

After enhancement:
- Clear all slicers before taking the main dashboard screenshot.
- Add a visible subtitle such as `All Employees | No Filters Applied`.
- Take separate screenshots for filtered analysis if needed.

## 7. Portfolio-quality improvement

Create two report pages:

### Page 1 — Executive Summary
- Total Employees
- Active Employees
- Attrition Count
- Attrition Rate
- Retention Rate
- Attrition by Department
- Attrition by Job Role
- Attrition by Salary Slab

### Page 2 — Attrition Drivers
- Age Group
- Gender
- OverTime
- Job Satisfaction
- Environment Satisfaction
- Years at Company
- Business Travel

## 8. Interview explanation

A concise explanation:

> I used Power BI to build an interactive HR analytics dashboard. I prepared and validated the employee dataset, used Power Query for data preparation, created DAX measures for employee and attrition KPIs, and designed visuals to analyze attrition by department, salary, job role, demographics and experience. I also added slicers so HR users can interactively investigate workforce patterns.

Do not claim transformations or measures that you have not actually implemented.
