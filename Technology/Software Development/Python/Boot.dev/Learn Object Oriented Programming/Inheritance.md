---
tags:
  - Python
  - Inheritance
mastered: false
created: 2025-01-03T09:07
updated: 2025-01-03T09:17
---
# Inheritance
Non-OOP languages such as #Go and #Rust allow for encapsulation and abstraction features as nearly *every* language does. Inheritance, on the other hand, tends to be unique to class-based languages such as #Python, #Java, and #Ruby.
## What is inheritance?
Inheritance allows one class, the "child" class, to *inherit* the properties and methods of another class, the "parent" class.
### Syntax
```python
class Animal:
	# parent "Animal" class

class Cow(Animal):
	# child class "Cow" inherits "Animal"
```
The `Cow` class above can reuse the `Animal` class's constructor with the `super()` method, `super()` allows the child class to call methods and constructors from its parent class, in this case, `__init__()`:
```python
class Animal:
	def __init__(self, num_legs):
		self.num_legs = num_legs

class Cow(Animal):
	def __init__(self, num_udders):
		super().__init(4)
		self.num_udders = num
```