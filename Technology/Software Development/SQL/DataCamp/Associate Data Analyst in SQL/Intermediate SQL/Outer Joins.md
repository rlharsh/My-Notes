---
tags:
  - SQL
  - Joining
mastered: false
created: 2025-01-03T07:20
updated: 2025-01-03T11:11
---
# LEFT and RIGHT JOINs
![[Pasted image 20250103110457.png]]
A LEFT #JOIN will return all records in the left table, and those records in the right table that match on the joining field provided.
![[Pasted image 20250103110632.png]]
## LEFT JOIN Syntax
```sql
SELECT
	p1.country,
	prime_minister,
	president
FROM prime_ministers AS p1
LEFT JOIN presidents AS p2
USING(country);
```

>[!info]
>`LEFT JOIN` can also be written as `LEFT OUTER JOIN`.

## RIGHT JOIN
`RIGHT JOIN` is much less common than `LEFT JOIN`.
![[Pasted image 20250103110950.png]]
### RIGHT JOIN SYNTAX
```sql
SELECT *
FROM left_table
RIGHT JOIN right_table
ON left_table.id = right_table.id
```

>[!info]
>`RIGHT JOIN` can also be written as `RIGHT OUTER JOIN`.
