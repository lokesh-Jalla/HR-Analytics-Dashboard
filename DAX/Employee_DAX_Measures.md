# Employee Attrition Dashboard - DAX Measures

## Workforce Metrics

```DAX
-- Total Employees
Total Employees =
COUNTROWS(FactEmployee)

-- Active Employees
Active Employees =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[Attrition] = FALSE()
)

-- Attrition Count
Attrition Count =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[Attrition] = TRUE()
)

-- Attrition Rate
Attrition Rate =
DIVIDE(
    [Attrition Count],
    [Total Employees],
    0
)
```

---

## Employee Demographics

```DAX
-- Average Age
Average Age =
AVERAGE(FactEmployee[Age])

-- Average Experience
Average Experience =
AVERAGE(FactEmployee[TotalWorkingYears])

-- Average Years at Company
Average Years at Company =
AVERAGE(FactEmployee[YearsAtCompany])
```

---

## Employee Satisfaction Metrics

```DAX
-- Average Environment Satisfaction
Average Environment Satisfaction =
AVERAGE(FactEmployee[EnvironmentSatisfaction])

-- Average Job Satisfaction
Average Job Satisfaction =
AVERAGE(FactEmployee[JobSatisfaction])

-- Average Work-Life Balance
Average Work Life Balance =
AVERAGE(FactEmployee[WorkLifeBalance])
```