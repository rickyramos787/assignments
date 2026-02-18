# Decision Statements
## 1. Comparison Operators
32 = spacebar 
33 = !
34 = "
35 = #
36 = $
37 = %
38 = &
39 = '
40 = (
41 = )
42 = *
43 = +
44 = ,
45 = -
46 = .
47 = /
48 = 0
49 = 1
50 = 2
51 = 3
52 = 4
53 = 5
54 = 6
55 = 7
56 = 8
57 = 9
58 = :
59 = ;
60 = <
61 = =
62 = >
63 = ?
64 = @
65 = A
66 = B
67 = C
68 = D
69 = E
70 = F
71 = G
72 = H
73 = I
74 = J
75 = K
76 = L
77 = M
78 = N
79 = O
80 = P
81 = Q
82 = R
83 = S
84 = T
85 = U
86 = V
87 = W
88 = X
89 = Y
90 = Z
91 = [
92 = \
93 = ]
94 = ^
95 = _
96 = `
97 = a
98 = b
99 = c
100 = d
101 = e
102 = f
103 = g
104 = h
105 = i
106 = j
107 = k
108 = l
109 = m
110 = n
111 = o
112 = p
113 = q
114 = r
115 = s
116 = t
117 = u
118 = v
119 = w
120 = x
121 = y
122 = z
123 = {
124 = |
125 = }
126 = ~
## 5. Problem-Solving
  a.  
  ```python
  # Largest of three integers

a = int(input("Enter first integer: "))
b = int(input("Enter second integer: "))
c = int(input("Enter third integer: "))

largest = a

if b > largest:
    largest = b

if c > largest:
    largest = c

print("The largest integer is:", largest)  b.  
```
  b.  
  ```python
num = int(input("Enter an integer: "))

#############################
# Approach 1: Modulus (%)
#############################
if num % 2 == 0:
    print("Approach 1:", "even")
else:
    print("Approach 1:", "odd")

#############################
# Approach 2: Integer division check
# (If dividing by 2 and multiplying back gives same number → even)
#############################
if (num // 2) * 2 == num:
    print("Approach 2:", "even")
else:
    print("Approach 2:", "odd")

#############################
# Approach 3: Bitwise AND (&)
# (Last bit 0 = even, last bit 1 = odd)
#############################
if (num & 1) == 0:
    print("Approach 3:", "even")
else:
    print("Approach 3:", "odd")
```
  c.  
  ```python
# Grade scheme for CISC 179

percent = int(input("Enter your percentage (integer): "))

if percent > 90:
    print("Grade: A")
    print("Description: Work of genuinely superior quality.")
elif 80 <= percent <= 89:
    print("Grade: B")
    print("Description: Passing performance falls approximately in the upper distribution of passing grades.")
elif 71 <= percent <= 79:
    print("Grade: C")
    print("Description: Passing performance falls approximately in the center of the distribution of all passing grades.")
elif 65 <= percent <= 70:
    print("Grade: D")
    print("Description: Passing performance falls approximately in the lower distribution of passing grades.")
else:
    print("Grade: F")
    print("Description: Failing performance that does not satisfy the basic requirements of the course and needs to be improved in significant ways.")
```
  d.  
  ```python
# Truth table for and/or/not

op = input("Enter a logical operator (and, or, not): ").strip().lower()

if op == "and":
    print("A     B     A and B")
    for A in [False, True]:
        for B in [False, True]:
            print(A, " ", B, " ", A and B)

elif op == "or":
    print("A     B     A or B")
    for A in [False, True]:
        for B in [False, True]:
            print(A, " ", B, " ", A or B)

elif op == "not":
    print("A     not A")
    for A in [False, True]:
        print(A, " ", (not A))

else:
    print("Invalid operator. Please enter: and, or, not")
```
  e.  
  ```python
# Even or odd using ONLY bitwise AND

num = int(input("Enter an integer: "))

if (num & 1) == 0:
    print("The number is even.")
else:
    print("The number is odd.")
```
## 6. Code Revision
```python
# Code Revision

# Get user input
name = input("What's your name? ")
time = int(input("What time is it (HHMM, e.g., 0930, 1545)? "))

if hours < 0 or hours > 23 or minutes < 0 or minutes > 59:
    print("Invalid time. Please enter time in HHMM format (0000 to 2359).")
else:
    # Nested decision structure:
    if time < 1200:
        # Morning
        print("Hi " + name + ", good morning!")
    else:
        # Not morning → could be afternoon or evening
        if time < 1800:
            # Afternoon
            print("Hi " + name + ", good afternoon!")
        else:
            # Evening (1800 or later)
            print("Hi " + name + ", good evening!")

    # Always say goodbye at the end (only if time was valid)
    print("Good Bye")
```
## Output Verification
```python
one
two
```
## Challenges

  -  Understanding how Python compares different data types (int, float, and string) was challenging at first, especially seeing that 1 == 1.0 evaluates to True.

  -  Distinguishing between separate `if` statements and `if-elif-else` chains required careful attention, since they do not behave the same way.

  -  Working with logical operators (`and`, `or`, `not`) required thinking carefully about truth tables and how conditions are evaluated.

  -  Using the bitwise AND operator (`&`) to determine whether a number is even or odd was initially confusing because it involves understanding binary representation.

  -  Making sure indentation and syntax were correct was important, since Python is sensitive to formatting.

  -  Testing different inputs helped identify logical mistakes and reinforced how decision statements control program flow.
