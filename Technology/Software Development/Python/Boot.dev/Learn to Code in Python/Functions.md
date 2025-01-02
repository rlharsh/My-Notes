---
type: SoftwareNote
title: Functions
modificationDate: 2024-12-06 08:56
tags:
  - Python
  - Functions
mastered: false
created: 2025-01-01T17:21
updated: 2025-01-02T12:54
---

# What are functions in Python

Functions allow us to *reuse* and *organize* code. For example, say we have some code that calculates the area of a circle:

```python
radius = 5
area = 3.10 * radius * radius
```

The above code works! The problem is that when we want to calculate the area of other circles, each with its own radius. We will want to reuse the above code to calculate further areas of circles, that is where #Functions come in. By using a function we can *pass* a variable to the function (the `radius` in this case) and retrieve our expected value, as follows:

```python
def area_of_circle(radius):
  pi = 3.14
  result = pi * radius * radius
  return result
```

In the above code you'll notice the `def` keyword. The `def` keyword defines a function within Python.

# Multiple Parameters

Functions can have multiple parameters. For example, this `subtract` function accepts 2 parameters: `a` and `b`.

```python
def subtract(a, b):
  result = a - b
  return result
```

- The name of a parameter doesn't matter when it comes to which values will be assigned to which parameter. It's **position** that matters.

- The first parameter will become the first value that's passed in, the second parameter is the second value that's passed in, ad so on.

# Where to declare functions

In Python it is important to remember that code executes in *order* *from top to bottom*, so a variable needs to be created before it can be used. That means that if you define a function, you can't call that function until *after* the definition.

For example, the following code doesn't work:

```python
print(my_name)
my_name = 'Lane Wagner'
```

It needs to be as follows:

```python
my_name = 'Lane Wagner'
print(my_name)
```

# Returning empty

When there is no return value specified in a function, it will automatically return `None` (see [NoneType Variables](RonaldsSoftwareNotes/NoneType%20Variables.md)). For example, maybe it's a function that prints some text to the console, but doesn't explicitly return a value. The following code snippet returns the value, `None`:

```python
def my_func():
  print("I do nothing")
  return
```

# Multiple return values

Functions are quite capable of returning more than one value by separating them with commas.

```python
def can_iceblast(wizard_level, start_mana):
  damage = wizard_level * 2
  new_mana = start_mana - 10
  return damage, new_mana # return two values
```

## Receiving multiple values

When calling a function that returns multiple values, you can assign them to multiple variables.

```python
dmg, mana = cast_iceblast(5, 100)
print(f"Damage: {dmg}, Remaining Mana: {mana}")
# Damage: 10, Remaining Mana: 90
```

When we call our `cast_iceblast` function, it returns two values. The first value is assigned to `dmg`, and the second value is assigned to `mana`. As with function inputs, it's the *order* of the values that matters, not the variable names. We could just as easily called the variables `one` and `two`:

```python
one, two = cast_iceblast(5, 100)
print(f"Damage: {one}, Remaining Mana: {two}")
# Damage: 10, Remaining Mana: 90
```

# Parameters vs arguments

- Parameters are the names used for inputs when *defining* a function.

- Arguments are the values of the inputs supplied when a function is *called*.

The reiterate, **arguments are the actual values** that go into the function such as `42.0`, `"the dark knight"`, or `True`. **Parameters are the names** we use in the function definition to refer to those values, which at the time of writing the function, can be whatever we like.

```python
# a and b are parameters
def add(a, b):
  return a + b

# 5 and 6 are arguments
sum = add(5, 6)
```

# Default values

In Python you can specify a default value for a function argument. This is quite nice when a function has arguments that are "optional".

A default value is created by using the assignment (`=`) operator in the function signature:

```python
def get_greeting(email, name='there'):
  print("Hello", name, "welcome! You've registered your email:", email)
```

```python
get_greeting("lane@example.com", "Lane")
# Hello Lane welcome! You've registered your email: lane@example.com
```

```python
get_greeting("lane@example.com")
# Hello there welcome! You've registered your email: lane@example.com
```

In the above example if the second parameter is omitted, the default `"there"` value will be used in its place.

**IMPORTANT:** In order for this structure to work, optional arguments (the ones with defaults) must come *after* all required arguments.

