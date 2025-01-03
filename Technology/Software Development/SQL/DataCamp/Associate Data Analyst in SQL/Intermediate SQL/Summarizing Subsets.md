---
type: SoftwareNote
title: Summarizing Subsets
modificationDate: 2024-12-07 15:26
tags:
  - SQL
  - Summarizing
mastered: false
created: 2025-01-03T13:03
updated: 2025-01-03T07:08
---

# Combining with the WHERE clause

We can combine [Summarizing Data: Aggregate Functions](RonaldsSoftwareNotes/Summarizing%20Data%20Aggregate%20Functions.md) with the `WHERE` clause to gain further insights from our data. 

- The `WHERE` clause executes before the `SELECT` statement.

```sql
SELECT AVG(budget) AS avg_budget
FROM films
WHERE release_year >= 2010;
```

```sql
SELECT MIN(budget) AS min_budget
FROM films
WHERE release_year = 2010;
```


