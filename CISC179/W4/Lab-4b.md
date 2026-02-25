# Dictionary in Python
## 1. Creating and Accessing Dictionary
a.
```python
# 1a) Car info dictionary with 10 elements (updated)

car_info = {
    "make": "Honda",
    "model": "Civic",
    "year": 2017,
    "color": "Gray",
    "mileage": 100000,
    "transmission": "CVT",
    "fuel_type": "Gasoline",
    "vin": "2HGFC2F69HH123456",
    "doors": 4,
    "owner": "Ricky"
}

print(car_info)
print("Number of elements:", len(car_info))
```
b.
```python
# 1b) Take user inputs and add them to a dictionary called my_user_dict

my_user_dict = {}
count = 0

choice = "Y"

while choice == "Y" or choice == "y":
    key = input("Enter a key (example: SSN or Name): ")
    value = input("Enter the value: ")

    my_user_dict[key] = value
    count = count + 1

    choice = input("Do you want to continue (Y/N): ")
```
c.

print("\nFinal dictionary:")
print(my_user_dict)
print("Total keys entered:", count)
