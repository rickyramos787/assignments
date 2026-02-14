# Python Variables
## Variable Memory Usage
```python
var1 = 10
print(hex(id(var1)))
var1 = 100
print(hex(id(var1)))
```
Python does not change the value 10 into 100. Instead, it creates (or reuses) a separate integer object for 100. ```var1``` is reassigned to point to that new object. The original object (10) remains in memory.
