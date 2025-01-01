---
type: SoftwareNote
title: Sets
modificationDate: 2024-12-19 17:20
tags:
  - Python
mastered: false
created: 2025-01-01T17:21
updated: 2025-01-01T11:31
---

# What are sets?

Sets are *like* #Lists, but they are *unordered* and they guarantee *uniqueness*. Only *ONE* of each value can be in a set.

```python
fruits = {'apple', 'banana', 'graph'}
print(type(fruits))
# Prints: <class 'set'>

print(fruits)
# Prints: {'banana', 'grape', 'apple'}
```

## Adding values to a set

You can add values to a set as follows:

```python
fruits = {'apple', 'banana', 'grape'}
fruits.add('pear')
print(fruits)
# Prints: {'banana', 'grape', 'pear', 'apple'}
```

## Creating an empty set

Because the empty bracket `{}` syntax creates an empty dictionary, to create an *empty* set, you need to use the `set()` function.

```python
fruits = set()
fruits.add('pear')
print(fruits)
# Prints: {'pear'}
```

## Iterating a set

**NOTE:** When iterating over values within a set, it should be noted that order is not guaranteed.

```python
fruits = {'apple', 'banana', 'grape'}
for fruit in fruits:
  print(fruit)
  # Prints:
  # banana
  # grape
  # apple
```

## Converting set to a list

```python
def remove_duplicates(spells):
  return list(set(spells))
```

The above code will take in a set (in this case known as `spells`) and convert it to a #Lists, with the duplicates removed. This can also be achieved *via* iteration:
​

```python
def remove_duplicates(spells):
    spells_learned = []
    for spell in spells:
        if spell not in spells_learned:
            spells_learned.append(spell)
    return spells_learned
```

## Removing Values

```python
fruits = {'apple', 'banana', 'grape'}
fruits.remove('apple')
print(fruits)
# Prints: {'banana', 'grape'}
```

## List Differences

Complete the `find_missing_ids` function. It accepts two lists as input, and returns a new list of all the ids present in the first list but not the second. Make sure to remove any duplicates.

```python
def find_missing_ids(first_ids, second_ids):
    s1 = set(first_ids)
    s2 = set(second_ids)
    return list(s1 - s2)
```


