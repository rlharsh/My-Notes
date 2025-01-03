---
tags:
  - Python
  - Abstraction
mastered: false
created: 2025-01-03T07:26
updated: 2025-01-03T07:33
---
# Abstraction
Abstraction helps us to handle complexity by hiding unnecessary details.
## Abstraction vs encapsulation
- Abstraction is about *creating a simple interface for complex behavior*. It focuses on what's exposed.
- Encapsulation is about *hiding* internal state. It focuses on tucking implementation details away so no one depends on them.
Abstraction is more about reducing complexity, #Encapsulation is more about maintaining the integrity of system internals.
## Are we encapsulating or abstracting?
Both. We are almost always doing both. Here's an example of using the `random` library to generate a random number:
```python
import random

attack_damage = random.randrange(5)
print(attack_damage)
```
In the above code example we generate a random number within the range of `0-5`. The developers of the `random` library have *abstracted* the complexity away and *encapsulated* it within the simple `randrange` function.

When writing libraries for use by other developers, getting the abstractions right is *crucial* because changing them later can be disastrous. 