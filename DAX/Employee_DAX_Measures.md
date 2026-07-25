# Employee DAX Measures

### Total Employees

```DAX
Total Employees =
COUNTROWS(FactEmployee)
```

### Active Employees

```DAX
Active Employees =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[Attrition] = FALSE()
)
```

### Attrition Count

```DAX
Attrition Count =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[Attrition] = TRUE()
)
```

### Attrition Rate

```DAX
Attrition Rate =
DIVIDE(
    [Attrition Count],
    [Total Employees],
    0
)
```

---

# Employee Demographics

### Average Age

```DAX
Average Age =
AVERAGE(FactEmployee[Age])
```

### Average Experience

```DAX
Average Experience =
AVERAGE(FactEmployee[TotalWorkingYears])
```

### Average Years at Company

```DAX
Average Years at Company =
AVERAGE(FactEmployee[YearsAtCompany])
```

---

# Employee Satisfaction Metrics

### Average Environment Satisfaction

```DAX
Average Environment Satisfaction =
AVERAGE(FactEmployee[EnvironmentSatisfaction])
```

### Average Job Satisfaction

```DAX
Average Job Satisfaction =
AVERAGE(FactEmployee[JobSatisfaction])
```

### Average Work-Life Balance

```DAX
Average Work Life Balance =
AVERAGE(FactEmployee[WorkLifeBalance])
```

---

## Measure Summary

| Category                      | Measures                                                                              |
| ----------------------------- | ------------------------------------------------------------------------------------- |
| Workforce Metrics             | Total Employees, Active Employees, Attrition Count, Attrition Rate                    |
| Employee Demographics         | Average Age, Average Experience, Average Years at Company                             |
| Employee Satisfaction Metrics | Average Environment Satisfaction, Average Job Satisfaction, Average Work Life Balance |
