---
type: SoftwareNote
title: SQL Formatting
modificationDate: 2024-12-05 16:38
tags:
  - SQL
  - Formatting
mastered: false
created: 2025-01-03T13:03
updated: 2025-01-03T07:07
---

# Formatting in SQL

SQL is a generous language as it pertains to formatting. New lines, capitalization & indentation are not required in SQL.

Take for instance the following code:

```sql
select title, release_year, country from films limit 3
```

The above code will run absolutely fine, and you will encounter no errors when running the given SQL query. However, with a little formatting we can ensure that our code maintains readability, and follows standards set forth Simon Honeywell.

```sql
SELECT 
  title,
  release_year,
  country
FROM films
LIMIT 3;
```

## Non-standard field names

- `release year` instead of `release_year`

- Put non-standard field names in double-quotes

## Why do we format?

SQL should be formatted properly for many reasons, and these reasons include:

- Easier collaboration with peers (being able to quickly identify blocks of code)

- Clean and reliable (easier to read, and interpret).

- Looks professional (conveys a sense of professionalism in coding techniques).



[SQL style guide by Simon Holywell](Weblinks/SQL%20style%20guide%20by%20Simon%20Holywell.md)

