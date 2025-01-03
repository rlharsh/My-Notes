---
type: SoftwareNote
title: Query Execution
modificationDate: 2024-12-05 16:58
tags:
  - SQL
  - Queries
mastered: false
created: 2025-01-03T13:03
updated: 2025-01-03T07:07
---

# What is SQL Execution?

SQL Execution is the order in which an SQL query is executed. It is important to remember that SQL code **is not** processed in the order which it is written. Knowing processing order is important when debugging and *aliasing*fields from tables.

For instance:

```sql
SELECT name
FROM people
LIMIT 10;
```

Below shows the order of execution for the code example listed above.

1. `FROM people`

2. `SELECT name`

3. `LIMIT 10;`



```sql
SELECT item
FROM coats
WHERE color = 'green'
LIMIT 5;
```

Below shows the order of execution for the code example listed above.

1. `FROM coats`

2. `WHERE color = 'green'`

3. `SELECT item`

4. `LIMIT 5;`


