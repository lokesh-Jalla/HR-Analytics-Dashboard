# Experience & Utility DAX Measures

### Total Job Roles

```DAX
Total Job Roles =
DISTINCTCOUNT(FactEmployee[JobRole])
```

### Total Departments

```DAX
Total Departments =
DISTINCTCOUNT(FactEmployee[Department])
```

### Total Education Fields

```DAX
Total Education Fields =
DISTINCTCOUNT(FactEmployee[EducationField])
```

---

# Overtime Workforce Metrics

### Employees Working Overtime %

```DAX
Employees Working Overtime % =
DIVIDE(
    [Overtime Employees],
    [Total Employees],
    0
)
```

### Employees Not Working Overtime %

```DAX
Employees Not Working Overtime % =
DIVIDE(
    [Non Overtime Employees],
    [Total Employees],
    0
)
```

---

# Experience Metrics

### Average Years With Current Manager

```DAX
Average Years With Current Manager =
AVERAGE(FactEmployee[YearsWithCurrManager])
```

### Average Years Since Last Promotion

```DAX
Average Years Since Last Promotion =
AVERAGE(FactEmployee[YearsSinceLastPromotion])
```

---

# Training & Performance Metrics

### Average Training Times

```DAX
Average Training Times =
AVERAGE(FactEmployee[TrainingTimesLastYear])
```

### Average Performance Rating

```DAX
Average Performance Rating =
AVERAGE(FactEmployee[PerformanceRating])
```

---

# Employee Utility Metrics

### Average Distance From Home

```DAX
Average Distance From Home =
AVERAGE(FactEmployee[DistanceFromHome])
```

---

## Measure Summary

| Category                       | Measures                                                               |
| ------------------------------ | ---------------------------------------------------------------------- |
| Organization Overview Metrics  | Total Job Roles, Total Departments, Total Education Fields             |
| Overtime Workforce Metrics     | Employees Working Overtime %, Employees Not Working Overtime %         |
| Experience Metrics             | Average Years With Current Manager, Average Years Since Last Promotion |
| Training & Performance Metrics | Average Training Times, Average Performance Rating                     |
| Employee Utility Metrics       | Average Distance From Home                                             |
