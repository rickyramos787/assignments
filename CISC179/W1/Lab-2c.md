# Python Variables
## Variable Memory Usage
```python
var1 = 10
print(hex(id(var1)))
var1 = 100
print(hex(id(var1)))
```
Python does not change the value 10 into 100. Instead, it creates (or reuses) a separate integer object for 100. ```var1``` is reassigned to point to that new object. The original object (10) remains in memory.
If nothing else is referencing 10, then Python will eventually remove it from memory. Two addresses appear because 10 and 100 are two different objects. Reassignment changes what the variable points to, not the object itself.
## Memory Map
| Address in hexadecimal | Char |
| ---------------------- | ---- |
| 0x10af0b398            |  H   |
| 0x10af0b908            |  e   |
| 0x10af0ba58            |  l   |
| 0x10af0ba58            |  l   |
| 0x10af0bae8            |  o   |
| 0x10af0b668            |  W   |
| 0x10af0bae8            |  o   |
| 0x10af0bb78            |  r   |
| 0x10af0ba58            |  l   |
| 0x10af0b8d8            |  d   |
## Problem-solving
  -  "dogcat"
  -  "the dog chases the cat"
  -  "dogdogdogdog"
```python
  x = 50
  x = x + 1
```
## Troubleshooting
    a. Valid: Variable names can be lowercase letters.
    b. Valid: Variables can start with an underscore.
    c. Invalid: Variable names cannot start with !. They must start with a letter or underscore.
    d. Valid: This overrides the built-in print() function. After this, you can't use print() normally.
    e. Invalid: False is a reserved keyword for Boolean constant in Python. You cannot assign to it.
## Challenges
  - Understanding how memory addresses change during reassignment
  - Learning how Python reuses small integers
  - Remembering valid variable naming rules
  - Understanding how string concatenation works
  - Avoiding overwriting built-in functions
