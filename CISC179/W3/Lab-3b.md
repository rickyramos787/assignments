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
c.
```python
while True:
    # Take two integers
    num1 = int(input("Enter first integer: "))
    num2 = int(input("Enter second integer: "))

    # Ask user for operation
    print("Choose operation:")
    print("1 - Addition")
    print("2 - Subtraction")
    print("3 - Multiplication")
    print("4 - Division")

    choice = input("Enter choice (1/2/3/4): ")

    if choice == "1":
        print("Result:", num1 + num2)
    elif choice == "2":
        print("Result:", num1 - num2)
    elif choice == "3":
        print("Result:", num1 * num2)
    elif choice == "4":
        if num2 != 0:
            print("Result:", num1 / num2)
        else:
            print("Error: Cannot divide by zero.")
    else:
        print("Invalid choice.")

    # Ask to continue
    again = input("Do you want to continue? (Y/N): ")

    if again != "Y" and again != "y":
        print("Have a good day")
        break
```
## For Loops
a.
```python
text = input("Enter a sentence: ")

text = text.lower()   # ignore uppercase/lowercase

total_letters = 0
letter_counts = {}

for ch in text:
    if ch.isalpha():           # only count letters
        total_letters += 1
        
        if ch in letter_counts:
            letter_counts[ch] += 1
        else:
            letter_counts[ch] = 1
    else:
        continue               # ignore spaces and punctuation

print("Total number of alphabets:", total_letters)
print("Total number of distinct alphabets:", len(letter_counts))

for letter in letter_counts:
    print(letter, "=", letter_counts[letter])
```
## Challenges
    -    One challenge I faced was understanding how to properly structure a while loop without creating an infinite loop. I had to make sure the condition would eventually become false.

    -    Another challenge was keeping track of the variable updates in the Collatz sequence. It was easy to forget to update the step counter or reassign n0 correctly.

    -    I also found it tricky to ignore punctuation and uppercase letters when counting characters. I had to carefully check each character and convert everything to lowercase.

    -    Making sure the total of all distinct letter counts matched the total alphabet count required extra debugging and testing.

    -    Finally, I had to pay close attention to indentation, since Python is very sensitive to spacing and it caused errors when misaligned.
