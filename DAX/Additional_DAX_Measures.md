# Employee Performance & Retention DAX Measures

### Average Job Involvement

```DAX
Avg Job Involvement =
AVERAGE(FactEmployee[JobInvolvement])
```

### Job Satisfaction %

```DAX
Job Satisfaction % =
DIVIDE(
    AVERAGE(FactEmployee[JobSatisfaction]),
    4,
    0
)
```

---

# Career Growth Metrics

### Average Promotion Gap

```DAX
Avg Promotion Gap =
AVERAGE(FactEmployee[YearsSinceLastPromotion])
```

### Average Years at Company

```DAX
Avg Years at Company =
AVERAGE(FactEmployee[YearsAtCompany])
```

---

# Employee Exit Metrics

### Average Exit Age

```DAX
Avg. Exit Age =
CALCULATE(
    AVERAGE(FactEmployee[Age]),
    FactEmployee[Attrition] = TRUE()
)
```

### Average Exit Income

```DAX
Avg. Exit Income =
CALCULATE(
    AVERAGE(FactEmployee[Monthly Income]),
    FactEmployee[Attrition] = TRUE()
)
```

---

# Overtime Metrics

### Overtime %

```DAX
Overtime % =
DIVIDE(
    CALCULATE(
        COUNTROWS(FactEmployee),
        FactEmployee[OverTime] = TRUE()
    ),
    COUNTROWS(FactEmployee),
    0
)
```

### Overtime Employees %

```DAX
Overtime Employees % =
DIVIDE(
    CALCULATE(
        COUNTROWS(FactEmployee),
        FactEmployee[OverTime] = TRUE()
    ),
    COUNTROWS(FactEmployee),
    0
)
```

---

# Performance Metrics

### Maximum Performance Rating

```DAX
Maximum Performance Rating = 5
```

---

# Retention Metrics

### Retention Rate

```DAX
Retention Rate =
1 - [Attrition Rate]
```

---

## Measure Summary

| Category                    | Measures                                        |
| --------------------------- | ----------------------------------------------- |
| Employee Engagement Metrics | Average Job Involvement, Job Satisfaction %     |
| Career Growth Metrics       | Average Promotion Gap, Average Years at Company |
| Employee Exit Metrics       | Average Exit Age, Average Exit Income           |
| Overtime Metrics            | Overtime %, Overtime Employees %                |
| Performance Metrics         | Maximum Performance Rating                      |
| Retention Metrics           | Retention Rate                                  |
