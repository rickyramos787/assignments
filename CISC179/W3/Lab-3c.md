# Lists in Python
## 1. Lists
a.
```python
# Generate list of 100 integers
my_list = list(range(100))

# Verify data type
print(type(my_list))

# Apply four list methods
my_list.append(100)
my_list.insert(0, -1)
my_list.remove(50)
my_list.sort()

print(my_list[:10])  # show first 10 elements
```
b.
```python
my_list = list(range(10))

# Move last three to front
my_list = my_list[-3:] + my_list[:-3]

print(my_list)
```
c.
```python
print(len([[1,2]] * 3))

