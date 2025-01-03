---
tags:
  - Python
  - Numbers
  - Operations
mastered: false
created: 2024-12-10T17:21:00
updated: 2025-01-03T07:17
---

# What are numbers in Python?

- In Python, numbers without a decimal point are called `Integers` - just like they are in mathematics.

- Integers are simply whole numbers, positive or negative. For example, `3` and `-3` are both examples of integers.

## Performing calculations

As you may expect you can perform mathematical calculations on Numbers:

```python
2 + 1 # addition
2 - 1 # subtraction
2 * 2 # multiplication
3 / 2 # division
```

### An important note on division

Sometimes if there is a remainder left over (quotient) it will produce a `float`.

### A detailed example

```python
def calculate_damage(sword, arrow, spear, dagger, fireball):
    total_damage = sword + arrow + spear + dagger + fireball
    average_damage = total_damage / 5
    return total_damage, average_damage
```

The code demonstrated above returns a mathematical calculation which is derived by first `adding` the total amount passed by all of the parameters, then calculating the quotient by `dividing` the `total_damage` by the number of passed parameters.

# Exponents

Python has built-in support for exponents - something most other languages would require a `math` library for.

```python
print(2 ** 3) # 2 * 2 * 2
```

# Plus Equals

Python makes reassignment quite simple when doing math. In other languages, such as JavaScript or Go, there is a `++` syntax for incrementing a number variable by 1. In Python, we instead use the `+=` in-place operator instead.

**NOTE: You cannot use the PLUS EQUALS (or any other variant in a return statement).**

```python
star_rating = 4
star_rating += 1
# star_rating is now 5
```

### Other operations

```python
star_rating -= 1
# star_rating is now 3

star_rating *= 2
# star_rating is now 8

star_rating /= 2
# star_rating is now 2.0
```

# Scientific Notation

In Python we can add the letter `e` or `E` followed by a positive or negative integer to specify that we are using scientific notation.

```python
print(16e3)
# Prints 16000.0

print(7.1e-2)
# prints 0.071
```

## Readability Concerns

Python allows us to represent large numbers in the decimal format using underscors as the delimiter instead of commas.

```python
num = 16_000
print(num)
# Prints 16000

num = 16_000_000
print(num)
# Prints 16000000
```


