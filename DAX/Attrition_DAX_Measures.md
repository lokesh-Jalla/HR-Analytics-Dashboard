1. Employee Retention Rate =
   DIVIDE(
   [Active Employees],
   [Total Employees],
   0
   )

2. Female Attrition =
   CALCULATE(
   COUNTROWS(FactEmployee),
   FactEmployee[Gender] = "Female",
   FactEmployee[Attrition] = TRUE()
   )

3. Male Attrition =
   CALCULATE(
   COUNTROWS(FactEmployee),
   FactEmployee[Gender] = "Male",
   FactEmployee[Attrition] = TRUE()
   )

4. Non Overtime Attrition =
   CALCULATE(
   COUNTROWS(FactEmployee),
   FactEmployee[OverTime] = FALSE(),
   FactEmployee[Attrition] = TRUE()
   )

5. Non Overtime Attrition Rate =
   DIVIDE(
   [Non Overtime Attrition],
   [Non Overtime Employees],
   0
   )

6. Non Overtime Employees =
   CALCULATE(
   COUNTROWS(FactEmployee),
   FactEmployee[OverTime] = FALSE()
   )

7. Overall Attrition % =
   DIVIDE(
   [Attrition Count],
   [Total Employees],
   0
   )

8. Overtime Attrition =
   CALCULATE(
   COUNTROWS(FactEmployee),
   FactEmployee[OverTime] = TRUE(),
   FactEmployee[Attrition] = TRUE()
   )

9. Overtime Attrition Rate =
   DIVIDE(
   [Overtime Attrition],
   [Overtime Employees],
   0
   )

10. Overtime Employees =
    CALCULATE(
    COUNTROWS(FactEmployee),
    FactEmployee[OverTime] = TRUE()
    )
