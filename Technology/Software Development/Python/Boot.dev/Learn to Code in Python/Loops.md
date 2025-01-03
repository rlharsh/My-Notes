---
tags:
  - Python
  - Loops
mastered: false
created: 2024-12-13T17:21:00
updated: 2025-01-03T07:16
---

# What are loops?

Loops allow us as programmers to do the same operation multiple times without having to write it explicitly each time.

For instance, if you wanted to print the numbers 0-9, you could do this:

```python
for i in range(0, 10):
  print(i)
```

**Note:** Indentation matters in a loop.

## Steps in range

The `range()` has an additional parameter which is known as the `step`, meaning that it directly affects the amount that `n` is increased per loop. For example:

```python
for i in range(0, 10, 2):
  print(i)
```

The above code will increment `i` each loop (e.g., step) by `2`, making the output:

```python
0
2
4
6
8
```

### Negative steps

You can also use the step to count backwards, as follows:

```python
for i in range(0, 3, -1):
  print(i)
```

The above code will countdown from `3`.

## While

Python has another type of loop, the `while` loop. It's a loop that continues `while` a condition remains `True`. The syntax is quite simple:

```python
while 1:
  print("1 evaluates to True")
```

The above code has been hardcoded to continue forever (because `1` will always evaluate to `True`).

Of course the above example is not suggested in real-world development, because there is no situation where you'd actually want a loop to run infinitely. The code below demonstrates a more practical solution for running a loop in a more controlled manner:

```python
num = 0
while num < 3:
  num += 1
  print(num)
```

The above code will terminate once `num` is greater than `3`.

## A more complex example:

```python
def regenerate(current_health, max_health, enemy_distance):
    while enemy_distance > 3:
        if current_health + 1 <= max_health:
            current_health += 1
        enemy_distance -= 2
    return current_health
```

The above code will add `1` to `current_health`, but only if `current_health + 1 < max_health`.

Every step the `enemy_distance` reduces by a value of `2`, and once the `enemy_distance` is less than `3` the player stops generating health, and the function returns the total `current_health`.

