---
type: SoftwareNote
title: SQL Keywords
modificationDate: 2024-12-05 17:09
tags:
  - SQL
  - keywords
mastered: false
created: 2025-01-03T13:03
updated: 2025-01-03T07:08
---

#keywords

## COUNT

- `COUNT()` - Counts the number of records with a value in a field.

    ```sql
    SELECT COUNT(birthdate) AS count_birthdates
    FROM people;
    ```

    If you want to use `COUNT()` to count multiple fields, you need to separate each field by a comma, as follows:

    ```sql
    SELECT COUNT(name) AS count_names, COUNT(birthdate) AS count_birthdates
    FROM people;
    ```

    **Using * with** `Count()`

    - `COUNT(field_name)` - counts values in a field

    - `COUNT(*)` - counts records in a table

    ```sql
    SELECT COUNT(*) AS total_records
    FROM people;
    ```

    **Using DISTINCT with** `COUNT()`

    There may be times where are results may contain duplicates, and in these instances we can use the `DISTINCT` keyword alongside `COUNT()` as follows:

    ```sql
    SELECT COUNT(DISTINCT birthdate) AS count_distinct_birthdates
    FROM people;
    ```

# WHERE

- `WHERE()` - Compares against a conditional value

```sql
SELECT *
FROM customers
WHERE age > 18;
```

**Where with stirngs**

The `WHERE()` clause can be used with strings, as follows:

```sql
WHERE country = 'Japan';
```

In the above code you will notice the single-quotation mark, this is **very important.**

| `<` - Returns results where the number is less than.         | `WHERE release_year < 1960`    |
| :----------------------------------------------------------- | :----------------------------- |
| `>` - Returns results where the number is greater than.      | `WHERE release_year > 1960`    |
| `=` - Returns results where the number is exactly equal too. | `WHERE release_year = 1960`    |
| `<>` - Returns results where the number is not equal too.    | `WHERE release_year <> 1960` ​ |
