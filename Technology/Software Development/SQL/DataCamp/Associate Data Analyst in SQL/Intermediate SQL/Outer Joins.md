---
tags:
  - SQL
  - Joining
mastered: false
created: 2025-01-03T07:20
updated: 2025-01-03T11:30
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

```sql
SELECT
	p1.country,
	prime_minister,
	president
FROM prime_ministers AS p1
RIGHT JOIN presidents AS p2
USING(country);
```

# Examples
```sql
SELECT 
    c1.name AS city, 
    code, 
    c2.name AS country,
    region, 
    city_proper_pop
FROM cities AS c1
-- Join right table (with alias)
LEFT JOIN countries AS c2
ON c1.country_code = c2.code
ORDER BY code DESC;
```

# Full Joins
A `FULL JOIN` combines a `LEFT JOIN` and a `RIGHT JOIN` (as seen in the image below). A `FULL JOIN` will return all data, irrespective of whether they have a match in the other table being joined.
![[Pasted image 20250103112744.png]]
```sql
SELECT left_table.id AS L_id,
	   right_table.id AS R_id,
	   left_table.val AS L_val,
	   right_table.val AS R_val
FROM left_table
FULL JOIN right_table
USING (id);
```
