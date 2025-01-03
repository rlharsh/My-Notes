---
type: SoftwareNote
title: NULL Values
modificationDate: 2024-12-06 18:51
tags:
  - SQL
  - Values
mastered: false
created: 2025-01-03T13:03
updated: 2025-01-03T07:07
---

# What are NULL Values

A missing or unknown value is known as a `NULL` value in SQL. In the real-world databases often have empty, or missing fields.

## Filtering with NULL

The following examples demonstrate how to properly use the `NULL` keyword within SQL.

Example returning only values that are `NULL`

```sql
WHERE birthdate IS NULL;
```

Example returning only values that are `NULL`

```sql
SELECT COUNT(*) AS no_birthdates
FROM people
WHERE birthdate IS NULL;
```

Example returning only values that are not `NULL`

```sql
WHERE birthdate IS NOT NULL;
```


