---
type: SoftwareNote
title: Rounding results
modificationDate: 2024-12-07 15:32
tags:
  - SQL
  - Rounding
mastered: false
created: 2025-01-03T13:03
updated: 2025-01-03T07:07
---

# What is ROUND?

`ROUND `is a function that we can use to round our results to a specified decimal.

## Using ROUND

**USAGE:** `ROUND(number_to_round, decimal_places)`

- The `decimal_places` parameter is option, so you can leave it out if you want to get the nearest whole number.

```sql
SELECT ROUND(AVG(budget), 2) AS avg_budget
```

## Using negative numbers

You can call `ROUND` with a negative number in the `decimal_places` parameter to round to the left of the decimal point instead of the right.

```sql
SELECT ROUND(AVG(budget), -5) AS avg_budget
FROM films
WHERE release_year >= 2010;
```


