---
tags:
  - Python
  - None
mastered: false
created: 2024-12-05T17:21:00
updated: 2025-01-03T07:17
---

# What is a NoneType variable?

Not all variables have a value. We can make an "empty" variable by setting it to `None`. `None` is a special value in python that represents the absence of a value. It is *not* the same as zero, False, or an empty string.

```python
my_mental_acuity = None
```

The value of `my_mental_acuity` in the above code example will continue to be `None` until we use the assignment operator, `=`, to give it a value.

## None is NOT a string

NoneType is *not* the same as a string with a value of "None":

```python
my_none = None # this is a None-Type
my_none = "None" # this is string with the value "None"
```

# Why would you use a NoneType?

One of the most common use cases for using the NoneType is that you haven't yet chosen a value for a variable.

An example of a use case for the NoneType is if we were implementing logic that checked age from a user (which hasn't yet been given to our program) we could perform an operation until the age is populated:

```python
age = None

age = int(input("What's your name? "))

if (age is None):
  # Do not continue
```



[Built-in Constants](Weblinks/Built-in%20Constants.md)

