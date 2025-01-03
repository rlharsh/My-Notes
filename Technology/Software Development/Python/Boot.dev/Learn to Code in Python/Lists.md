---
tags:
  - Python
  - Lists
mastered: false
created: 2024-12-13T17:21:00
updated: 2025-01-03T07:15
---

# What are Lists?

List are a natural way to organize and store data. Other languages refer to `lists` as `arrays`.

## Using Lists

Declaring a list in Python is done by using square brackets, with commas separating each item:

```python
inventory = ["Iron Breastplate", "Healing Potion", "Leather Scrps"]
```

Lists can contain items of any data type, in the example above we have a `List` of #Strings.

## Declaring Lists

When declaring lists sometimes it can be hard to read if all items are on the same line of code. We can declare the list using multiple lines if we want to:

```python
flower_types =[
  "daffodil",
  "rose",
  "chrysanthemum"
]
```

**NOTE:** This is just a styling change. The code will run correctly either way.

## Indexing into Lists

In a list, we can access specific items within the list by selecting the desired index.

**NOTE:** Indexes start at `0`. 

The syntax is as follows:

```python
best_languages = ["JavaScript", "Go", "Rust", "Python", "C"]
print(best_languages[1])
# prints "Go", because index 1 was provided
```

## List length

We can retrieve the length of a list using the `len()` function.

```python
fruits = ["apple", "banana", "pear"]
length = len(fruits)
# 3
```

The length (e.g., `len()`) of the list is equal to the number of items present.

**NOTE:** Don't be fooled by the fact that the length is not equal to the index of the last element, in fact, it will always be one greater.

## Updating a list

We can change an item that exists at a given index in the following way:

```python
inventory = ["Leather", "Iron Ore", "Healing Potion"]
inventory[0] = "Leather Armor"
# inventory: ['Leather Armor', 'Iron Ore', 'Healing Potion']
```

## Appending a list

It's quite common to create an empty list then fill it with values using a loop. For this we can make use of the `.append()` method:

```python
cards = []
cards.append("nvidia")
cards.append("amd")
# the cards list is now ['nvidia', 'amd']
```

## Pop Values

`.pop()` is the opposite of `.append()`. Pop removes the last element from a list and returns it for use. For example:

```python
vegetables = ["broccoli", "cabbage", "kale", "tomato"]
last_vegetable = vegetables.pop()
# vegetables = ['broccoli', 'cabbage', 'kale']
# last_vegetable = 'tomato'
```

**NOTE:** While `.pop()` typically removes the last item of a list, it can also be used to remove an item at a specific index. For example, `vegetables.pop(1)` would remove `cabbage` from the list. This can be useful when you need to remove items from other positions in your list.

## Iterate using for (No-index Syntax)

We can directly iterate over items within a list without worrying about index numbers (provided we don't need access to it). To accomplish this we can use the following syntax:

```python
trees = ['oak', 'pine', 'maple']
for tree in trees:
  print(tree)
```

## Finding the Maximum value

Python has a built-in `float()` function which can create a numeric floating point value of negative infinity. Because *every value* will be greater than negative infinity, we can use it to help us accomplish our goal of finding the max value.

```python
negative_infinity = float("-inf")
positive_infinity = float("inf")
```

## Slicing Lists

Python makes it quite easy to slice lists to work only with the sections you care about. One way to accomplish this is to use the simple slicing operator, which is just a colon `:`.

By using this operator, you can specify where to start and end the slice, and how to step through the original list. 

The syntax is as follows:

```python
my_list[ start : stop : step ]
```

For example:

```python
scores = [50, 70, 30, 20, 90, 10, 50]
# Display list
print(scores[1:5:2])
# Prints [70, 20]
```

### Omitting sections

You can also omit various sections ("start", "stop", or "step"). For example, `numbers[:3]` means "get all items from the start up to (but not including) index 3". `numbers[3:]` means "get all items from index 3 to the end".

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
numbers[:3] # Gives[0, 1, 2]
numbers[3:] # Gives[3, 4, 5, 6, 7, 8, 9]
```

### Using only the "step" section

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
numbers[::2] # Gives [0, 2, 4, 6, 8]
```

### Negative Indices

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
numbers[-3:] # Gives [7, 8, 9]
```

## Concatenate Lists

Concatenating two list (combining them together) is easy in Python, just use the `+` operator.

```python
total = [1, 2, 3] + [4, 5, 6]
print(total)
# Prints: [1, 2, 3, 4, 5, 6]
```

## Contains

Checking whether a value exists in a list is also easy in Python, simply use the `in` keyword.

```python
fruits = ["apple", "orange", "banana"]
print("banana" in fruits)
# Prints: True
```

## Deleting items in a List

Python has a built-in keyword `del` that deletes items from objects. In the case of a list, you can delete specific indexes or entire slices.

```python
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9]

# delete the fourth item
del nums[3]
prints(nums)
# Output: [1, 2, 3, 5, 6, 7, 8, 9]

# delete the second item up to (but not including) the fourth item
del nums[1:3]
print(nums)
# Output: [1, 4, 5, 6, 7, 8, 9]

# delete all elements
del nums[:]
print(nums)
# Output: []
```

