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

print("\nFinal dictionary:")
print(my_user_dict)
print("Total keys entered:", count)
```
c.
```python
# 1c) Validate tuple pairs and check duplicate keys (no functions / no exceptions)

pairs = [
    ("Name", "Sarah Connor"),
    ("Date of birth", "1 Jan 1985"),
    ("Address", "1000 Black Mountain"),
    ("Name", "Jim Hawkins")  # duplicate key example
]

result_dict = {}
i = 0

while i < len(pairs):
    item = pairs[i]

    # ---- Check 1: item must be a tuple with exactly 2 values ----
    if type(item) != tuple or len(item) != 2:
        print("\nInvalid pair found at index", i, ":", item)
        print("It must be a tuple like: ('Key', 'Value')")

        new_key = input("Enter a corrected key: ")
        new_value = input("Enter a corrected value: ")
        pairs[i] = (new_key, new_value)
        # re-check same index again (don't move i)
        continue

    key = item[0]
    value = item[1]

    # ---- Check 2: key must be a string (simple “valid key” rule) ----
    if type(key) != str:
        print("\nInvalid key type at index", i, ":", key)
        print("Key should be a string (example: 'Name').")

        new_key = input("Enter a corrected key (string): ")
        pairs[i] = (new_key, value)
        continue

    # ---- Check 3: duplicate key check ----
    if key in result_dict:
        print("\nDuplicate key found:", key)
        print("Existing value:", result_dict[key])
        print("New value:", value)
        print("Please change the key to something unique.")

        new_key = input("Enter a new unique key: ")
        pairs[i] = (new_key, value)
        continue

    # If all checks pass, add to dictionary
    result_dict[key] = value
    i = i + 1

print("\nFinal dictionary:")
print(result_dict)
```
d.
```python
