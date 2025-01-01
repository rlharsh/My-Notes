---
type: SoftwareNote
title: Tuples
modificationDate: 2024-12-16 13:20
tags:
  - Python
mastered: false
created: 2025-01-01T17:21
updated: 2025-01-01T11:31
---

# What are Tuples?

Tuples are collections of data that are ordered and unchangeable. You can think of a tuple as a #Lists with a fixed size. Tuples are created with round brackets: `()`.

```python
my_tuple = ("this is a tuple", 45, True)
```

While it is typically considered bad practice to store items of different types in #Lists, it's not a problem with #Tuples. Because they have a fixed size, it's easy to keep track of which indexes store which types of data.

- Tuples are often used to store very small groups (like 2 or 3 items) of data.

- There is a special case for creating single-item tuples. You must include a comma so that Python knows it's a tuple and not a regular parentheses:

```python
dog = ("Fido",)
```

## Unpacking a Tuple

You can easily assign the values of a tuple to variables using unpacking.

```python
dog = ("Fido", 4)
dog_name, dog_age = dog
```

When you return multiple values from a function, you're actually returning a tuple.


