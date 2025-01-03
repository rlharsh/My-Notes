---
tags:
  - Python
  - Comments
mastered: false
created: 2024-12-05T17:21:00
updated: 2025-01-03T07:13
---

# What are comments?

Comments are lines that are *ignored* by the Python interpreter. By adding comments to your code, you can clearly communication, what a function or operation intends to do.

# Types of comments.

There are several lines of comments in Python, such as single-line comments and multi-line comments (aka docstrings).

## Single-line comments

A single `#`makes the rest of the line a comment:

```python
# speed describes how fast the player
# moves in meters per second
speed = 2
```

## Multi-line comments (aka docstrings)

You can use triple quotes to start and end multi-line comments as well:

```python
"""
  the code found below
  will print 'Hello, World!' to the console
"""
print("Hello, World!")
```

Multi-line comments are useful if you don't want to add the # to the start of each line when writing paragraphs of comments.

