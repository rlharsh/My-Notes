---
tags:
  - Python
  - Inheritance
mastered: false
created: 2025-01-03T09:07
updated: 2025-01-03T09:27
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
		self.num_udders = num_udders
```
## When should we use inheritance?
Inheritance should only be used when all instances of a child class are also instances of the parent class.
When a child class inherits from a parent, it inherits *everything*. If we only want to share some functionality, inheritance is probably not the best answer.
## Inheritance Hierarchy
There is no limit as to how deeply we can nest an inheritance tree. For example, a `Cat` can inherit from an `Animal` that inherits from `LivingThing`. 

We should **never** think to ourselves:
>[!info]
>"Well *most* wizards are elves... so I'll just have wizard inherit from elf".

A good child is a strict subset of its parent class.
An example of thiws with private properties. A child class cannot simply access a 