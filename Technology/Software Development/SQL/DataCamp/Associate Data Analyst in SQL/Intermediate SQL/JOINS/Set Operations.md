---
tags:
  - SQL
  - JOIN
mastered: 
created: 2025-01-03T12:45
updated: 2025-01-03T12:49
---
# Set theory for SQL Joins
SQL has three main set operations:
- `UNION`
- `INTERSECT`
- `EXCEPT
The Venn diagram below visualizes the differences between them:
![[Pasted image 20250103124742.png]]
## UNION
`UNION` takes two tables as input, and returns all records from both tables:
![[Pasted image 20250103124904.png]]
## UNION ALL
`UNION ALL` will in