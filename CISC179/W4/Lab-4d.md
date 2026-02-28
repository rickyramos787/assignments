# Child Vaccination Chart
```python
# Lab 4d: Child vaccination chart
# Main nested dictionary must be named `patient`

patient = {}

def insert():
    global patient

    first_name = input("Enter patient's first name: ").strip()
    last_name = input("Enter patient's last name: ").strip()

    record_num = input("Enter patient record number (ex: R001): ").strip()

    while record_num in patient:
        print("That record number already exists. Try a different one.")
        record_num = input("Enter patient record number (ex: R002): ").strip()

    vaccines = ["HepB", "RV", "DTaP", "Hib", "PCV13", "IPV", "IIV4", "MMR", "VAR", "HepA"]

    patient[record_num] = {
        "first": first_name,
        "last": last_name,
        "vaccines": {}
    }

    annual_vaccines = ["IIV4", "MMR", "VAR", "HepA"]

    for v in vaccines:
        if v in annual_vaccines:
            patient[record_num]["vaccines"][v] = "Annual"
        else:
            month = int(input(f"Enter the month administered for {v} (integer): "))
            patient[record_num]["vaccines"][v] = month

    print(f"\n✅ Added record {record_num} for {first_name} {last_name}.\n")

# Run once (call insert() again later to add another patient)
insert()

print("Current patient dictionary:")
print(patient)

insert()

print("Current patient dictionary:")
print(patient)
```
