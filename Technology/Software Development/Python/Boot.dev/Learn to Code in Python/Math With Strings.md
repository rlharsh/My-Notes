---
type: SoftwareNote
title: Math With Strings
modificationDate: 2024-12-05 16:01
tags:
  - Python
mastered: false
created: 2025-01-01T17:21
updated: 2025-01-01T11:31
---

# Math With Strings

When working with strings the `+` operator performs a "concatenation", which is a way of saying "joining two strings". Generally speaking, it's better to use string interpolation with [F-strings in Python](RonaldsSoftwareNotes/F-strings%20in%20Python.md) over `+` concatenation.

```python
first_name = "Lane "
last_name = "Wagner"
full_name = fisrt_name + last_name
print(full_name)
# prints "Lane Wagner"
```

`full_name` now holds the value "Lane Wagner".
