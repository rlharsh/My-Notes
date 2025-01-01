---
created: 2024-12-10T17:21:00
updated: 2025-01-01T11:34
tags:
  - Python
  - "#Bitwise"
  - "#Operators"
mastered: false
---

# What are Bitwise Operators?

Bitwise operators are similar to logical operators, but instead of operating on Boolean values, they apply the same logic to all the bits in a value by column. For instance, say you had the numbers `5` and `7` represented in binary. You could perform a bitwise "and" operation and the result would be `5`.

- `0101` is 5

- `0111` is 7

# The & Operator

```python
0101
&
0111
=
0101
```

A `1` in binary is the same as `True`, while `0` is `False`. So really a bitwise operation is just a bunch of logical operations that are completed in tandem by column.

```python
0 & 0 = 0
1 & 1 = 1
1 & 0 = 0
```

Amersand `&` is the bitwise "and" operator in Python. "And" is the *name* of the bitwise operation, while ampersand `&` is the *symbol* for that operation. For example, `5 & 7 = 5`, while `5 & 2 = 0`.

- `0101` is 5

- `0010` is 2

```python
0101
& 
0010
=
0000
```

# The | Operator

The `|`, is the bitwise "or" operator, and is similar to the bitwise "and" operator in that it works on binary rather than boolean values. However, the bitwise "or" operator "or"'s the bits together. Here is an example:

- `0101` is 5

- `0111` is 7

```python
0101
|
0111
=
0111
```

A `1` in binary is the same as `True`, while `0` is `False`. So a bitwise operation is just a bunch of logical operations that are completed in tandem. When two binary numbers are "or"ed together, the result has a `1` in any place where *either* of the input numbers has a `1` in that place.

`|` is the bitwise "or" operator in Python. `5 | 7 = 7` and `5 | 2 = 7` as well!

- `0101` is 5

- `0010` is 2

```python
0101
|
0010
= 
0111
```

