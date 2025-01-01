---
type: SoftwareNote
title: Logical Operators
modificationDate: 2024-12-10 09:53
tags:
  - Python
mastered: false
created: 2025-01-01T17:21
updated: 2025-01-01T17:21
---

# What are logical operators?

- Logical operators deal with #BooleanValues, `True` and `False`.

- The logical `and` operator requires that *both* inputs are `True` to return `True`.

- The logical `or` operator requires that at *least* *one* input is `True` to return `True`.

```python
True and True == True
True and False == False
False and False == False

True or True == True
True or False == True
False or False == False
```

## Python Syntax

```python
print(True and True)
# prints True

print (True or False)
# prints True
```

## Nesting with parentheses

We can nest logical expressions using parentheses.

```python
print((True or False) and False)
```

### Evaluating the expression

`(True or False)` will evaluate to `True`:

```python
print(True and False)
```

`True and False` evaluates to `False`:

```python
print(false)
```

So, `print((True or False) and False)` prints "False" to the console.

# The Not Operator

The `not` operator reverses the results. It returns `False` if the input was `True` and vice-versa.

```python
print(not True)
# Prints: False

print(not False)
# Prints: True
```

