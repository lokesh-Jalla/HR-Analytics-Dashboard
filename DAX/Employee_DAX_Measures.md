# Employee Attrition Dashboard - DAX Measures

## Employee Retention Metrics

### Employee Retention Rate

```DAX
Employee Retention Rate =
DIVIDE(
    [Active Employees],
    [Total Employees],
    0
)
```

### Overall Attrition %

```DAX
Overall Attrition % =
DIVIDE(
    [Attrition Count],
    [Total Employees],
    0
)
```

---

# Gender-Based Attrition Metrics

### Female Attrition

```DAX
Female Attrition =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[Gender] = "Female",
    FactEmployee[Attrition] = TRUE()
)
```

### Male Attrition

```DAX
Male Attrition =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[Gender] = "Male",
    FactEmployee[Attrition] = TRUE()
)
```

---

# Overtime Workforce Metrics

### Overtime Employees

```DAX
Overtime Employees =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[OverTime] = TRUE()
)
```

### Non Overtime Employees

```DAX
Non Overtime Employees =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[OverTime] = FALSE()
)
```

---

# Overtime Attrition Metrics

### Overtime Attrition

```DAX
Overtime Attrition =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[OverTime] = TRUE(),
    FactEmployee[Attrition] = TRUE()
)
```

### Overtime Attrition Rate

```DAX
Overtime Attrition Rate =
DIVIDE(
    [Overtime Attrition],
    [Overtime Employees],
    0
)
```

### Non Overtime Attrition

```DAX
Non Overtime Attrition =
CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[OverTime] = FALSE(),
    FactEmployee[Attrition] = TRUE()
)
```

### Non Overtime Attrition Rate

```DAX
Non Overtime Attrition Rate =
DIVIDE(
    [Non Overtime Attrition],
    [Non Overtime Employees],
    0
)
```
