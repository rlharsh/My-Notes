---
type: SoftwareNote
title: Dictionaries
modificationDate: 2024-12-16 15:51
tags:
  - Python
mastered: false
created: 2025-01-01T17:21
updated: 2025-01-01T11:31
---

# What is a dictionary?

A #Dictionary in Python is used to store data in `key` -> `value` pairs.

- Dictionaries are a great way to store groups of information.

```python
# use curly braces
# add key-value pairs
car = {
  "brand": "Tesla",
  "model": "3",
  "year": 2019
}
```

In the above dictionary example the `car` variable is assigned to a dictionary `{}` containing the keys `brand`, `model`, and `year`.

## Duplicate Keys

Since dictionaries rely on unique keys, you can't have two of the same key in the same dictionary. If you attempt to use the same key twice, the first value will simply be overwritten.

## Accessing Dictionary Values

In order to us to access dictionary values we simply need to use `[]` brackets and the value we are attempting to locate:

```python
car = {
  "make": "tesla",
  "model": "3"
}
print(car["make"])
# Prints tesla
```

## Setting Dictionary Values

In order to set dictionary values we simply need to use the `[]` brackets and the value we are attempting to write:

```python
planets = {}
planets["Earth"] = True
planets["Pluto"] = False
print(planets["Pluto"])
# Prints False
```

## Deleting Dictionary Values

In order to delete dictionary values we can make use of the `del` keyword (#del).

```python
names_dict = {
  "jack": "bronson",
  "jill": "mcarty",
  "joe": "denver"
}

del names_dict["joe"]
```

## Checking if key exists

In order to check if a key exists in a #Dictionary we can make use of the `in` keyword (#in).

```python
cars = {
  "ford": "f150",
  "tesla": "3"
}

print("ford" in cars)
# Prints: True

print("gmc" in cars)
# Prints: False
```

## Iterating over a dictionary

You can iterate over a dictionary using the same no-index syntax that is used to iterate over values within a #Lists.

```python
fruit_sizes = {
  "apple": "small",
  "banana": "large",
  "grape": "tiny"
}

for name in fruit_sizes:
  size = fruit_sizes[name]
  print(f"name: {name}, size: {size}")
```

