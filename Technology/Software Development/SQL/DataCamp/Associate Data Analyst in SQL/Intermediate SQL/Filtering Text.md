---
tags:
  - SQL
  - Filtering
  - Text
mastered: false
created: 2024-12-06T13:03:00
updated: 2025-01-03T07:09
---

# LIKE

The `LIKE` clause can be used in conjunction with the #sql_where `WHERE` clause to search for a pattern in a field.

With `LIKE` there are two wildcards:

- `%` - Will match zero, one, or many characters

```sql
WHERE name LIKE 'Ade%';
```

- `_` - Will match a single character

```sql
WHERE name LIKE 'EV_';
```

# NOT LIKE

The `NOT LIKE` clause can be used to find data that does not match the specified pattern, such as:

```sql
WHERE name NOT LIKE 'A.%';
```

# IN

The `IN` operator allows us to specify multiple values in a `WHERE` clause, making it easier and quicker to set numerous `OR` conditions.

```sql
WHERE release_year IN (1920, 1930, 1940)
```

```sql
WHERE country IN ('Germany', 'France')
```

# Wildcard position

**You can use the wildcards** `%` **and** `_` **at any position within a query.**

