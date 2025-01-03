---
tags:
  - Python
  - Variables
mastered: false
created: 2025-12-01T17:21:00
updated: 2025-01-03T07:19
---

# What are variables?

- Variables are how we *store* data as our program runs.

- Variables are called "variables" because they can hold any value and that value can change (it varies).

# How to utilize variables.

A "variable" is a name that we give to a value. For example, we can make a new variable named `my_height` and set it to `100`:

```python
my_height = 100
```

Or we can define a variable called `my_name` and set it to the text string `"Lane"`:

```python
my_name = "Lane"
```

# Using variables

Once we have a variable, we can access its value by using its given name. For example, this will print `100` to the console:

```python
print(my_height)
```

And this will print `Lane`:

```python
print(my_name)
```

## Changing Variables

The following example sets a value called `acceleration` to `10`, and in the next line it changes the value to `20`:

```python
acceleration = 10
acceleration = 20
print(acceleration)
```

The line `acceleration = 20` *reassigns* the value of `acceleration` to `20`. It *overwrites* whatever was being held in the `acceleration` variable before