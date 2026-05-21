---
title: Chap-4
date: 2026-05-19
author: Your Name
cell_count: 5
score: 5
---

```python
total = sum(num for num in range(1, 101) if num % 2 == 0)

print(f"The sum of all even numbers from 1 to 100 is: {total}")
```

    The sum of all even numbers from 1 to 100 is: 2550
    


```python
num1 = int(input("Enter the first number (dividend): "))
num2 = int(input("Enter the second number (divisor): "))
quot = num1 // num2
rem = num1 % num2
print(f"Quotient: {quot}")
print(f"Remainder: {rem}")
```

    Enter the first number (dividend):  34
    Enter the second number (divisor):  4
    

    Quotient: 8
    Remainder: 2
    


```python
cel = float(input("Enter temperature in Celsius: "))
fah = float((cel * 9/5) + 32)
kel = float(cel + 273.15)
print(f"Fahrenheit: {fah:}F")
print(f"Kelvin: {kel:}K")
```

    Enter temperature in Celsius:  98
    

    Fahrenheit: 208.4F
    Kelvin: 371.15K
    


```python
import math
num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: "))
gcd = math.gcd(num1, num2)
lcm = abs(num1 * num2) // gcd
print(f"GCD of {num1} and {num2} is: {gcd}")
print(f"LCM of {num1} and {num2} is: {lcm}")
```

    Enter the first number:  67
    Enter the second number:  54
    

    GCD of 67 and 54 is: 1
    LCM of 67 and 54 is: 3618
    


```python

```


---
**Score: 5**