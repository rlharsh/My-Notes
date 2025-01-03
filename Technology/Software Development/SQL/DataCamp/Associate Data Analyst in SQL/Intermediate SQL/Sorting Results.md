---
tags:
  - SQL
  - Sorting
mastered: false
created: 2024-12-10T13:03:00
updated: 2025-01-03T07:11
---

# ORDER BY

## What is ORDER BY

`ORDER BY` is a keyword used to sort results of one or more fields.

- `ORDER BY` is written after the `FROM` statement.

- Sorts in ascending order by default.

- Sorts in descending with keyword `DESC`.

- You can sort by different order for each `ORDER BY`.

- `ORDER BY` will always be written after `GROUP BY`, when used in conjunction.

## Usage

```sql
SELECT title, budget
FROM films
ORDER BY budget;
```

## Usage in conjuction with WHERE

```sql
SELECT title, budget
FROM films
WHERE budget IS NOT NULL
ORDER BY budget DESC;
```

## Using multiple ORDER BY

```sql
SELECT title, wins, imdb_score
FROM best_movies
ORDER BY wins DESC, imdb_score DESC;
```

# GROUP BY

## What is GROUP BY?

`GROUP BY` groups rows with the same values in specified columns, enabling aggregate functions to compute results for each group.

- SQL will return an error if we try to `SELECT` a field that is not in our `GROUP BY` clause. You **must** add an aggregate function around the value.

## Usage

```sql
SELECT certification, COUNT(title) AS title_count
FROM films
GROUP BY certification;
```

## Error Handling

```sql
SELECT certification, title
FROM films
GROUP BY certification;
```

The above code will result in an error. See below to see the proper working code:

```sql
SELECT
  certification,
  COUNT(title) AS count_title
FROM films
GROUP BY certification;
```

## GROUP BY Multiple Fields

```sql
SELECT certification, language, COUNT(title) AS title_count
FROM films
GROUP BY certification, language;
```

## GROUP BY with ORDER BY

```sql
SELECT
  certification,
  COUNT(title) AS title_count
FROM films
GROUP BY certification
ORDER BY title_count DESC:
```

```sql
SELECT
    release_year,
    COUNT(DISTINCT language) AS max_languages
FROM films
GROUP BY release_year
ORDER BY max_languages DESC;
```

# HAVING

- Filters grouped records.

```sql
SELECT
  release_year,
  COUNT(title) AS title_count
FROM films
GROUP BY release_year
WHERE COUNT(title) > 10;
```

The above code is invalid. However if we introduce the `HAVING` keyword, the code works as you would expect it too:

```sql
SELECT
  release_year,
  COUNT(title) AS title_count
FROM films
GROUP BY release_year
HAVING COUNT(title) > 10;
```

The above code is the correct way to introduce the `HAVING` keyword into our SQL code.


