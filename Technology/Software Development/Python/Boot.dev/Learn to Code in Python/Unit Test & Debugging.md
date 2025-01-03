---
tags:
  - Python
  - Debugging
  - Testing
  - Unit
mastered: false
created: 2024-12-16T17:21:00
updated: 2025-01-03T07:19
---

# What is an unit test?

A unit test is an automated program that tests a small "unit" of code (usually just a function or two).

## Why do an unit test?

There are many reasons to do a unit test, but here are some of the more notable reasons:

- **Improved Code Reliability**

    - Unit tests verify that your functions and methods perform correctly for a range of inputs.

    - By testing individual units of code, you can catch bugs early in development.

- **Facilitates Refactoring**

    - With unit tests in place, we can confidently refactor or update our code, knowing that the tests will catch any regressions or errors introduced during the process.

- **Easier Debugging**

    - When a unit test fails, it often points directly to the faulty function or method, making it easier to identify and fix the problem.

- **Encourages Better Code Design**

    - Writing tests forces us to think about how our code is structured and used, which can lead to cleaner, more modular code that's easier to test and maintain.

## A basic example of a unit test

```python
import unittest

# testing function
def add_numbers(a, b):
  return a + b

class TestMathOperations(unittest.TestCase):
  def test_add_numbers(self):
    self.assertEqual(add_numbers(1, 2), 3)
    self.assertEqual(add_numbers(-1, 1), 0)
    self.assertEqual(add_numbers(0, 0), 0)

if __name__ == "__main__":
  unittest.main()
```

# What is debugging?

Debugging simply put is the process of identifying, analyzing, and fixing errors or "bugs" in our Python code. Bugs can manifest as syntax errors, runtime errors, or logic errors.

## Benefits of debugging

- Ensures code behaves as expected and adheres to the intended logic

## Types of errors

1. **Syntax Errors:** Issues with the structure of the code (e.g., missing colons or parentheses).

2. **Runtime Errors:** Errors that occur during execution (e.g., division by zero, accessing undefined variables).

3. **Logic Errors:** The code runs without crashing but produces incorrect results.

