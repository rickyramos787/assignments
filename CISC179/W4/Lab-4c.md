# Functions in Python
## 1. Create a Unit Conversion Program Using Functions
a.
Conversion factor (US gallons)
	•	mpg = kpl × (3.785411784 / 1.609344)
	•	kpl = mpg × (1.609344 / 3.785411784)

So:
	•	1 kpl ≈ 2.352145833 mpg
	•	1 mpg ≈ 0.425143707 kpl
```python
KM_PER_MILE = 1.609344
L_PER_US_GAL = 3.785411784

def kpl_to_mpg(kpl: float) -> float:
    return kpl * (L_PER_US_GAL / KM_PER_MILE)

def mpg_to_kpl(mpg: float) -> float:
    return mpg * (KM_PER_MILE / L_PER_US_GAL)

def parse_numbers(raw: str):
    """
    Accepts multiple values separated by spaces or commas.
    Rejects non-numeric input.
    """
    parts = raw.replace(",", " ").split()
    if not parts:
        raise ValueError("No values entered.")
    nums = []
    for p in parts:
        nums.append(float(p))  # raises ValueError if not a number
    return nums

def convert_many(direction: str, *values: float):
    """
    direction: 'kpl_to_mpg' or 'mpg_to_kpl'
    values: any number of numeric inputs
    """
    results = []
    for v in values:
        if v < 0:
            raise ValueError("Values must be non-negative.")
        if direction == "kpl_to_mpg":
            results.append(kpl_to_mpg(v))
        elif direction == "mpg_to_kpl":
            results.append(mpg_to_kpl(v))
        else:
            raise ValueError("Invalid direction.")
    return results

def main():
    print("Fuel Economy Converter: kpl ⇄ mpg")
    print("Type multiple values separated by spaces or commas.\n")

    while True:
        choice = input("Convert (1) kpl → mpg or (2) mpg → kpl? (q to quit): ").strip().lower()
        if choice == "q":
            print("Goodbye!")
            return
        if choice not in ("1", "2"):
            print("Error: please enter 1, 2, or q.\n")
            continue

        raw_vals = input("Enter value(s): ").strip()
        try:
            nums = parse_numbers(raw_vals)
            direction = "kpl_to_mpg" if choice == "1" else "mpg_to_kpl"
            converted = convert_many(direction, *nums)

            if choice == "1":
                for original, new in zip(nums, converted):
                    print(f"{original} kpl = {new:.3f} mpg")
            else:
                for original, new in zip(nums, converted):
                    print(f"{original} mpg = {new:.3f} kpl")

            print()
        except ValueError:
            print("Error: invalid input detected. Please enter numbers only (example: 12 14.5 20).\n")

if __name__ == "__main__":
    main()
```
b.
```python
def print_reverse(*args):
    for item in reversed(args):
        print(item)

print_reverse(1, 2, 3, "hello", True)
```
c.
```python
import copy

def safe_nested(nested):
    clone = copy.deepcopy(nested)
    clone[0].append("X")
    return clone
```
d.
```python

