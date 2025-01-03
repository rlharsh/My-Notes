---
tags:
  - SQL
  - JOIN
mastered: 
created: 2025-01-03T12:45
updated: 2025-01-03T14:13
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

## INTERSECT
`INTERSECT` takes two tables as input, and returns only the records that exist in both tables.
![[Pasted image 20250103141039.png]]
### Syntax
```sql
SELECT
	id,
	val
FROM left_table
INTERSECT
SELECT
	id,
	val
FROM right_table;
```

### Example
```sql
SELECT
	country as intersect_country
FROM prime_ministers
INTERSECT
SELECT country
FROM presidents;
```
