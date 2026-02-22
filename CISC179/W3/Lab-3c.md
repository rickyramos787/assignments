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
```
d.
```python
my_list_ten = [1, 2, 3, 3, 4, 5, 5, 6, 7, 1]

# Memory addresses
my_list_ten_mem = [id(item) for item in my_list_ten]

print(my_list_ten_mem)
```
```python
print(len(set(my_list_ten_mem)))  # unique memory addresses
```
e.
```python
del my_list_ten
```
f.
```python
my_new_list = [1, 2, 3, 3, 4, 5, 5, 6, 7, 1]

my_new_list_mem = [id(item) for item in my_new_list]

print(my_new_list_mem)
```
g.
```python
import copy

x = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

y = copy.deepcopy(x)

y[0][0] = 99

print("x:", x)
print("y:", y)
```
h.
```python
numbers = [x if x % 2 == 0 else -x for x in range(10)]
print(numbers)
```
i.
```python
statement = "To be, or not to be, this is the question"

spaces = len([char for char in statement if char == " "])

print(spaces)
```
j.
```python
nums = [3, 1, 4, 1, 5]

nums.append(9)
nums.extend([2, 6])
nums.insert(0, 10)
nums.pop()
nums.reverse()

print(nums)
```
## Challenges
- Understanding how list multiplication works with nested lists was tricky at first.

- Comparing memory addresses using id() helped me understand how Python stores small integers.

- Learning the difference between shallow copy and deep copy required extra research.

- Remembering correct list slicing syntax took some practice.

- Making sure all code runs without errors before submitting to GitHub required debugging.
