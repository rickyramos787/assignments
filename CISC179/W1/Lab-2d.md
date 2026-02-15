# User input using input() function
## 1. User Input
a.
```python
#Convert kilograms into pounds
kg = float(input("Enter your kg value: "))
pounds = kg * 2.2
print("Weight in pounds: ", pounds)
```
b.
```python
#Credit card interest calculator
netBalance = float(input("Enter net balance: "))
payment = float(input("Enter payment made: "))
d1 = int(input("Enter number of days in billing cycle (d1): "))
d2 = int(input("Enter number of days payment was made before end of cycle (d2): "))
interestRatePerMonth = float(input("Enter monthly interest rate: "))
averageDailyBalance = ((netBalance * d1) - (payment * d2)) / d1
interest = averageDailyBalance * interestRatePerMonth
print("Average Daily Balance:", averageDailyBalance)
print("Interest:", interest)
```
c.
```python
import math
# Get speeds
x = float(input("Enter speed of Car A (mph): "))
y = float(input("Enter speed of Car B (mph): "))
# Get time
hours = int(input("Enter hours: "))
minutes = int(input("Enter minutes: "))
# Convert time to hours
t = hours + (minutes / 60)
# Distances traveled
distanceA = x * t
distanceB = y * t
# Shortest distance between cars
distance = math.sqrt(distanceA**2 + distanceB**2)
print("Distance between cars:", distance)
```
## 2. Troubleshooting
    a.  Valid: Variable names can contain letters.
    b.  Valid: Variable names can begin with an underscore.
    c.  Invalid: Variable names cannot begin with !. Python only allows letters, numbers, and underscores.
    d.  Valid: You are overwriting Python's built-in print() function.
    e.  Invalid: False is a reserved Boolean keyword in Python. It cannot be reassigned. 

## Challenges
  -  The most challenging part of this exercise was understanding how to properly
convert user input into the correct data type (float or int). I also had to
carefully apply the formulas for the average daily balance and distance formula.
Another challenge was remembering that some words like False are reserved
keywords and cannot be used as variable names.
