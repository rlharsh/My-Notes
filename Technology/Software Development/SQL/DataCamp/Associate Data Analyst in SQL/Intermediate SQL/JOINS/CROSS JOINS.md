---
tags:
  - SQL
  - JOIN
  - CROSS
mastered: 
created: 2025-01-03T11:43
updated: 2025-01-03T12:00
---
# CROSS JOIN
`CROSS JOINS` are slightly different than other joins (such as [[INNER JOIN]] & [[OUTER JOIN]]): they create all possible combinations of two tables.
## Syntax
```sql
SELECT id1, id2
FROM table1
CROSS JOIN table 2
```

```sql
SELECT
	prime_minister,
	president
FROM prime_ministers AS p1
CROSS JOIN presidents AS p2
WHERE p1.continent IN ('Asia')
	AND p2.continent IN ('South America');
```

