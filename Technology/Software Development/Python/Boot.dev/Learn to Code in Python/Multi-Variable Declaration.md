---
tags:
  - Python
  - Variables
mastered: false
created: 2024-12-05T17:21:00
updated: 2025-01-03T07:16
---

# Multi-Variable Declaration

We can save space when creating many new variables by declaring them on the same line:

```python
sword_name, sword_damage, sword_length = "Excalibur", 10, 200
```

Which is the same as:

```python
sword_name = "Excalibur"
sword_damage = 10
sword_length = 200
```

Any number of variables can be declared on the same line, and variables declared on the same line *should* be related to one another in some way so that the code will remain easy to understand.

