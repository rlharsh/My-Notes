---
tags:
  - SQL
  - JOIN
mastered: 
created: 2025-01-03T12:45
updated: 2025-01-03T12:56
---
# Set theory for SQL Joins
SQL has three main set operations:
- `UNION`
- `INTERSECT`
- `EXCEPT

>[!info]
>Set operations **DO NOT** require a field to join on.


The Venn diagram below visualizes the differences between them:
![[Pasted image 20250103124742.png]]
## UNION
`UNION` takes two tables as input, and returns all records from both tables:
![[Pasted image 20250103124904.png]]
### Example
```sql
SELECT *
FROM left_table
UNION 
SELECT *
FROM right_table;
```
## UNION ALL
`UNION ALL` will include duplicate records.
### Example
```sql
SELECT *
FROM left_table
UNION ALL
SELECT *
FROM right_table;
```
