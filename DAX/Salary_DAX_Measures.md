# Salary DAX Measures

### Average Salary

```DAX
Average Salary =
AVERAGE(FactEmployee[Monthly Income])
```

### Average Annual Salary

```DAX
Average Annual Salary =
AVERAGE(FactEmployee[Monthly Income]) * 12
```

### Total Salary Expense

```DAX
Total Salary Expense =
SUM(FactEmployee[Monthly Income])
```

---

# Salary Statistics

### Maximum Salary

```DAX
Maximum Salary =
MAX(FactEmployee[Monthly Income])
```

### Minimum Salary

```DAX
Minimum Salary =
MIN(FactEmployee[Monthly Income])
```

### Median Salary

```DAX
Median Salary =
MEDIAN(FactEmployee[Monthly Income])
```

### Salary Range

```DAX
Salary Range =
[Maximum Salary] - [Minimum Salary]
```

---

# Employee Pay Rate Metrics

### Average Daily Rate

```DAX
Average Daily Rate =
AVERAGE(FactEmployee[DailyRate])
```

### Average Hourly Rate

```DAX
Average Hourly Rate =
AVERAGE(FactEmployee[HourlyRate])
```

### Average Monthly Rate

```DAX
Average Monthly Rate =
AVERAGE(FactEmployee[MonthlyRate])
```

---

## Measure Summary

| Category | Measures |
|----------|----------|
| Salary Overview Metrics | Average Salary, Average Annual Salary, Total Salary Expense |
| Salary Statistics | Maximum Salary, Minimum Salary, Median Salary, Salary Range |
| Employee Pay Rate Metrics | Average Daily Rate, Average Hourly Rate, Average Monthly Rate |