# Loops
## 1. While Loops
a.  
```python
# Take a non-negative and non-zero integer
n0 = int(input("Enter a positive integer: "))

steps = 0

while n0 != 1:
    if n0 % 2 == 0:        # if number is even
        n0 = n0 // 2
    else:                  # if number is odd
        n0 = 3 * n0 + 1
    
    print(n0)
    steps += 1

print("steps =", steps)
```
b.  
```python
while True:
    print("This loop will run forever...")
```
```python
count = 0

while count < 5:
    print("Looping...")
    count += 1
```
