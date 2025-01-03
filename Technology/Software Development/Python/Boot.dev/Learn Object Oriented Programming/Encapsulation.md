---
tags:
  - Python
  - Encapsulation
mastered: false
created: 2024-12-27T14:51:00
updated: 2025-01-03T07:12
---
# Encapsulation
#Encapsulation is the practice of hiding complexity inside of a "black box" so that it's easier to focus on the problem at hand.

> [!info]
> To be clear, it does *not* make code more secure in a cryptographic or cyber-security sense.
> 
> **Encapsulation is about organization, not security**

The most basic example of encapsulation is a function. The caller of a function doesn't need to worry too much about what happens inside, they just need to understand the inputs and the outputs.

```python
acceleration = calc_acceleration(initial_speed, final_speed, time)
```
To use the `calc_acceleration` function, we don't need to think about every individual line of code inside of the function. We just need to know that if we give it the inputs:
- `initial_speed`
- `final_speed`
- `time`
Then it will give us the correct `acceleration` as an output.

## Public
By default, all properties and methods in a class are *public*. That means that you can access them with the `.` operator:
```python
wall.height = 10
print(wall.height)
# 10
```

## Private
[Private](https://docs.python.org/3/tutorial/classes.html#tut-private) data members are how we encapsulate logic and data within a class. To make a property private, you need only prefix it with two underscores `__`.
```python
class Wall:
	def __init__(self, armor, magic_resistance):
		self.__armor = armor
		self.__magic_resistance = magic_resistance

	def get_defense(self):
		return self.__armor + self.__magic_resistance

front_wall = Wall(10, 20)

# Error
# print(front_wall.__armor)

print(front_wall.get_defense())
#30
```

# Examples
**Wizard Class**
```python
class Wizard:
	def __init__(self, name, stamina, intelligence):
		self.__stamina = stamina
		self.__intelligence = intelligence

		self.name = name
		self.health = stamina * 100
		self.mana = intelligence * 10
```
