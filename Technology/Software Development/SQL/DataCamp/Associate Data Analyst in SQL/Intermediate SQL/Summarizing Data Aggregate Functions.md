---
tags:
  - SQL
  - Summarizing
mastered: false
created: 2024-12-07T13:03:00
updated: 2025-01-03T07:11
---

# What is an aggregate function?

An aggregate function performs a calculation on several values and returns a single value.

- Aggregate functions come after the `SELECT`

- We operate on the field with aggregate functions.

- `AVG()` `SUM()` are the only 2 aggregate functions that cannot be used with non-numeric types.

- It is best practice to use an #alias when summarizing data.

# AVG()

Returns the average from a field.

```sql
SELECT AVG(budget)
```

# SUM()

Returns the sum of all of the field.

```sql
SELECT SUM(budget)
```

# MIN()

Returns the minimum from within the field.

- Will return the Lowest <-> Highest

    - In the case of alphabetical, it would return a-z.

    - Would return the earliest date.

```sql
SELECT MIN(budget)
```

# MAX()

Returns the maximum from the field.

- Will return the Highest <-> Lowest

    - In the case of alphabetical, it would return z-a.

    - Would return the latest date.

```sql
SELECT MAX(budget)
```

# COUNT()

```sql

```


