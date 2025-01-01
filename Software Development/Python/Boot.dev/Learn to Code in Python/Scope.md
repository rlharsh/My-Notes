---
type: SoftwareNote
title: Scope
modificationDate: 2024-12-06 09:49
tags:
  - Python
mastered: false
created: 2025-01-01T17:21
updated: 2025-01-01T11:31
---

# What is scope

In Python scope refers to *where* a variable or function name is available to be used. For example, when we create variables in a function (such as by giving names to our parameters), that data is *not* available outside of that function.

```python
def subtract(x, y):
  return x - y
result = subtract(5, 3)
print(x)
# ERROR! "name 'x' is not defined"
```

In the above code when the `subtract` function is called, we assign 5 to the variable `x` but `x` only exists in the code *within* the `subtract` function.

# Types of scope

In Python there are several scope definitions, two of the most prominent being:

## Global Scope

```python
x = 5

def my_function():
  print(x)

my_function()
```

In the above code example `x` has been declared above all of the other code in the file, meaning that `x` will be accessible everywhere within the program. This makes `x` global scoped, and universally accessible.

## Function Scope

```python
x = 5
def f():
  y = 10

print(y) # Error, as y is within the function scop of f()
```

In the above code example `x` remains within the global scope, and the function `f()` is also within the global scope. However, `y` which has been declared within function `f()` is within the function scope, as it is only accessible within this function.

