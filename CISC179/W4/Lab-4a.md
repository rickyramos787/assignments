# Tuples in Python
## 1. Exercising Tuples
a.
```python
my_tuple = (
    input("Enter value 1: "),
    input("Enter value 2: "),
    input("Enter value 3: "),
    input("Enter value 4: "),
    input("Enter value 5: ")
)

print("my_tuple =", my_tuple)
```
b.
```python
my_tuple = (1, 2, 3)
# my_tuple[0] = 10   # This will raise an error (TypeError)
print("Tuples are immutable, so individual elements cannot be reassigned.")
```
c.
```python
my_tuple = (1, 2, 3, 4, 3, 2, 1, 2, 3, 5, 4, 3, 2, 1)

for num in set(my_tuple):
    print(f"{num} appears {my_tuple.count(num)} time(s)")
```
d.
```python
my_tuple_c = (1, 2, 3, 4, 3, 2, 1, 2, 3, 5, 4, 3, 2, 1)
my_tuple_d = my_tuple_c + my_tuple_c

print("Part c tuple:", my_tuple_c)
print("Part d tuple:", my_tuple_d)

print("Length of part c:", len(my_tuple_c))
print("Length of part d:", len(my_tuple_d))

print("Are they equal?", my_tuple_c == my_tuple_d)
print("Are they the same object?", my_tuple_c is my_tuple_d)
```
e.
	•	x.append(1) is illegal because tuples do not have an append() method. append() is for lists, not tuples.
	•	x[1] = "hello" is illegal because tuples are immutable, so you cannot change an item after creation.
	•	del x[2] is illegal because you cannot delete a single element from a tuple.

## 2. Packing and Unpacking Tuples
a.

