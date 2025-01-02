---
tags:
  - Python
  - Encapsulation
mastered: 
created: 2025-01-01T14:51
updated: 2025-01-01T18:32
---
# Encapsulation
#Encapsulation is the practice of hiding complexity inside of a "black box" so that it's easier to focus on the problem at hand.

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
