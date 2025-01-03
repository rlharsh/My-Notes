---
type: SoftwareNote
title: Filtering with Multiple Criteria
modificationDate: 2024-12-05 17:29
tags:
  - SQL
  - Filtering
mastered: false
created: 2025-01-03T13:03
updated: 2025-01-03T07:07
---

# Filtering with Multiple Criteria

There will be many times when we will want to filter our results set by multiple criteria. Luckily SQL comes with the following #keywords to help us accomplish this:

## Keywords

### OR

- `OR` - #sql_or 

    Use `OR` when you need to satisfy at least one condition.

    ```sql
    SELECT *
    FROM coats
    WHERE color = 'yellow' OR length = 'short';
    ```

### AND

- `AND` - #sql_and 

    Use `AND` if we need to satisfy all criteria.

    ```sql
    SELECT *
    FROM coats
    WHERE color = 'yellow' AND length = 'short';
    ```

### BETWEEN

- `BETWEEN` - #sql_between 

    Use `BETWEEN` when you need to check for values within a specified range.

    ```sql
    SELECT *
    FROM coats
    WHERE buttons BETWEEN 1 AND 5;
    ```

### AND, OR

```sql
SELECT title
FROM films
WHERE (release_year = 1994 OR release_year = 1995)
  AND (certification = 'PG' OR certification = 'R');
```

