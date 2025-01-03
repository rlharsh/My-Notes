---
tags:
  - SQL
  - Joining
mastered: false
created: 2024-12-19T13:03:00
updated: 2025-01-03T11:04
---
# What is INNER JOIN?

`INNER JOIN` makes up one of the two most common #SqlJoins. As seen in the picture below, two tables named "left_table" and "right_tabloe" are shown. Matching values of "id" in both tables are shown in the same color. In both tables, the `id` filed is the key.

[image](Images/image.md)

In SQL you can join on a key field, or any other field. The `INNER JOIN` shown looks for records in both tables with the same values in the key field, id.

[image](Images/image%20(1).md)

## Example of INNER JOIN

```sql
SELECT prime_ministers.country, prime_ministers.continent, prime_minister, president
FROM presidents
INNER JOIN prime_ministers
ON presidents.country = prime_ministers.country;
```

**IMPORTANT:** The `table.column_name` format must be used when selecting columns that exist in both tables to avoid a SQL error.

## Aliases with JOINS

You can use aliases with #SqlJoins, as follows:

```sql
SELECT p2.country, p2.continent, prime_minister, president
FROM presidents AS p1
INNER JOIN prime_ministers AS p2
ON p1.country = p2.country;
```

**IMPORTANT:** You will noticed that the aliased name is given on line 3, the `INNER JOIN` `AS p2`.

**IMPORTANT:** You can also alias the main table on the `FROM AS alias`.

# Using USING

We can also use the `USING` shortcut (provided that both columns are named identically, as follows:

```sql
SELECT p2.country, p2.continent, prime_minister, president
FROM presidents AS p1
INNER JOIN prime_ministers AS p2
USING(country);
```

# Multiple Joins

In SQL multiple joins can be combined and run in a single query

```sql
SELECT *
FROM left_table
INNER JOIN right_table
ON left_table.id = right_table.id
INNER JOIN another_table
ON left_table.id = another_table.id;
```

**IMPORTANT:** Depending on the use case, `left_table` or `right_table` can be used in the `ON` clause.

```sql
SELECT
  p1.country, p1.continent,
  president, prime_minister
FROM prime_ministers AS p1
INNER JOIN presidents AS p2
USING(country);
```

Below is the final SQL query after chaining a second `INNER JOIN`:

```sql
SELECT
  p1.country, p1.continent,
  president, prim_minister,
  pm_start
FROM prime_ministers AS p1
INNER JOIN presidents AS p2
USING(country)
INNER JOIN prime_minister_terms as p3
USING(prime_minister);
```

# Joining on multiple keys

We can further limit the rectors returned by supplying an additional field to join on by adding the `AND` keyword to our `ON` clause, as seen in the example below:

```sql
SELECT *
FROM left_table
INNER JOIN right_table
ON left_table.id = right_table.id
  AND left_table.date = right_table.date;
```


