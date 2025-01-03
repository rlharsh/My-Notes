---
tags:
  - Python
  - Errors
  - Exceptions
mastered: false
created: 2024-12-16T17:21:00
updated: 2025-01-03T07:14
---

# Exceptions

Even if our code has the right syntax, it may still cause an error when an attempt is made to execute it. Errors detected during execution are called "exceptions" and can be handled gracefully by your code. We can even raise our own exceptions when bad things happen within our code.

Python uses a try-except pattern for handling errors.

```python
try:
  10 / 0
except Exception:
  print("can't divide by zero")
```

In the above example, as in all Python code the `try` block is executed until an exception is raised or completes, whichever happens first. The `except` block is only executed if an exception is raised in the `try` block.

If we want to access the data from the exception, we use the following syntax:

```python
try:
  10 / 0
except Exception as e:
  print(e)

# prints "division by zero"
```

## The difference between "bugs" and errors

**Bugs are anything unexpected**

- An example of a bug would be: "the program crashes when someone types something in chat'. 

- The only solution to a bug is to fix the code.

- Bugs are **always bad**.

**Errors are something that are planned for/expected**

- An example of a bug would be: "internet connection lost".

- Errors are raised as exceptions intentionally by the developer.

- Errors return an error (which can be handled)

## Raising Exceptions

Raising exceptions manually can be accomplished as follows:

```python
def craft_sword(metal_bar):
    if metal_bar == "bronze":
        return "bronze sword"
    if metal_bar == "iron":
        return "iron sword"
    if metal_bar == "steel":
        return "steel sword"
    raise Exception("invalid metal bar")
```

The above code will raise if the player attempts to craft a sword out of anything other than `bronze`, `iron`, or `steel`. This is not a bug, as it was intended to raise this error.

## Don't catch your own exceptions

As a rule of thumb, you do not want to catch exceptions you raise within the same function block, for example:

```python
# don't do this
def craft_sword(metal_bar):
    try:
        if metal_bar == "bronze":
            return "bronze sword"
        if metal_bar == "iron":
            return "iron sword"
        if metal_bar == "steel":
            return "steel sword"
        raise Exception("invalid metal bar")
    except Exception as e:
        print(f"An error occurred: {e}")
```

Instead, the caller should handle any potential error by wrapping the function call within a try/except block.

```python
# do this
try:
    craft_sword("gold bar")
except Exception as e:
    print(e)
```

## Types of exceptions

Some exceptions are specific, like `ZeroDivisionError` or `IndexError`, and some are more general, like the base `Exception`.

```python
try:
    10/0
except ZeroDivisionError:
    print("0 division")
except Exception as e:
    print(e)

try:
    nums = [0, 1]
    print(nums[2])
except IndexError:
    print("index error")
except Exception as e:
    print(e)
```

The above code would print:

```text
0 division
index error
```

### Specific exceptions come first

When we handle exceptions, it's important to catch **the most specific ones first**, because Python stops checking once it finds a matching exception handler. If you catch a more general Exception first, any specific errors will never get handled individually.

```python
try:
  nums = [0, 1]
  print(nums[2])
except Exception:
  print("An error occurred")
except IndexError:
  print("Index error")
```

In the case of the above code, the general exception will catch before the `IndexError` can be reached, and the message "Index error" will never be printed. 

**Always handle the most specific exception first!**

## Alias exception messages

As seen in the example you can also access the error using `as`, like this:

```python
except Exception as e:
  print(e)
```


