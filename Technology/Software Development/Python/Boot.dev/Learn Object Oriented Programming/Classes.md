---
tags:
  - Python
  - Classes
mastered: false
created: 2024-12-27T17:39:00
updated: 2025-01-03T07:12
---

# Classes

A class is a special type of value in an object-oriented programming language like Python. It's similar to a dictionary in that it usually stores other types inside itself.

```python
# Defines a new class called "Soldier"
class Soldier:
  health = 5
  armor = 3
  damage = 2

soldier = Soldier()
print(soldier.health)
```

Just like a string, integer or float, a class is a *type*, but instead of being a built-in type, classes are custom types that we define.

An object is just an instance of a class type. For example:

```python
health = 50
# health is an instance of an integer type
aragorn = Soldier()
# aragorn is an instance of the Soldier type (class)
```


