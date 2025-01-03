---
tags:
  - SQL
  - JOIN
mastered: 
created: 2025-01-03T12:02
updated: 2025-01-03T12:10
---
# Self Joins
Self joins are used to compare values from part of a table to other values from within the same table.
- Self joins **do not** have dedicated syntax as other joins do.
- Aliasing is required for a self join.
## Example Syntax
```sql
SELECT
	p1.country AS country1,
	p2.country AS country2
FROM prime_ministers AS p1
INNER JOIN prime_ministers AS p2
ON p1.continent = p2.continent
LIMIT 10;
```

A more well formed SQL query for a Self Join would be as follows:
```sql
SELECT
	p1.country AS country1,
	p2.country AS country2,
	p1.continent
FROM prime_ministers AS p1
INNER JOIN prime_ministers AS p2
ON p1.continent = p2.continent
	AND p1.country <> p2.country;
```

