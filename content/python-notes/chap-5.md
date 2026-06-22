---
title: Chap-5
date: 2026-06-22
author: Your Name
cell_count: 24
score: 20
summary: Python Notes — chap 5 notebook with Python examples and exercises.
---

```python
def greet():
    print("Hello, Python!")
greet()
```

    Hello, Python!
    


```python
def square(number):
    print(number ** 2)
user_input = input("Enter a number: ")
converted_number = int(user_input)
square(converted_number)
```

    Enter a number:  45
    

    2025
    


```python
def add(a, b):
    return a + b
result = add(8,5)
print(result)  
```

    13
    


```python
def greet_user(name="Guest"):
    print(f"Hello, {name}!")
greet_user()
greet_user("Alex")

```

    Hello, Guest!
    Hello, Alex!
    


```python
def student_info(name, age):
    print(f"Student Name: {name}")
    print(f"Student Age: {age}")
student_info(age=21, name="Sam")
```

    Student Name: Sam
    Student Age: 21
    


```python
def sum_numbers(*args):
    return sum(args)
print(sum_numbers())
print(sum_numbers(5, 10, 15))
print(sum_numbers(1.5, 2.5, -3.0, 4.0))
```

    0
    30
    5.0
    


```python
def display_profile(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")
display_profile(name="Jordan", role="Developer", location="Boston")
```

    name: Jordan
    role: Developer
    location: Boston
    


```python
def complete_profile(*args, **kwargs):
    print("Positional arguments:")
    for item in args:
        print(f"- {item}")
    print("\nKeyword arguments:")
    for key, value in kwargs.items():
        print(f"- {key}: {value}")
complete_profile(
    "Photography", "Hiking", name="Taylor", age=28, city="Seattle"
)
```

    Positional arguments:
    - Photography
    - Hiking
    
    Keyword arguments:
    - name: Taylor
    - age: 28
    - city: Seattle
    


```python
cube = lambda x: x**3
print(cube(3))
print(cube(5))
```

    27
    125
    


```python
def cube(x):
    return x**3
print(cube(3))
print(cube(5))
```

    27
    125
    


```python
x = 100  
def local_scope_demo():
    x = 10  
    print(f"Inside function (local): {x}")
local_scope_demo()
print(f"Outside function (global): {x}")
```

    Inside function (local): 10
    Outside function (global): 100
    


```python
counter = 0  
def increment_counter():
    global counter  
    counter += 1
increment_counter()
increment_counter()
increment_counter()
print(f"Final counter value: {counter}")
```

    Final counter value: 3
    


```python
def outer_function():
    message = "Hello from the enclosing scope!"  
    def inner_function():
        print(message)
    inner_function()
outer_function()
```

    Hello from the enclosing scope!
    


```python
def outer_function():
    counter = 0 
    def inner_function():
        nonlocal counter  
        counter += 1
        print(f"Current count: {counter}")
    inner_function()
    inner_function()
outer_function()
```

    Current count: 1
    Current count: 2
    


```python
built_in_example = len
x = "Global Scope"
def outer_function():
    x = "Enclosing Scope"
    def inner_function():
        x = "Local Scope"
        print(f"1. Inside inner_function (looks at Local): {x}")
        print(
            f"4. Inside inner_function (using Built-in len): Length of Local is {built_in_example(x)}"
        )
    inner_function()
    print(f"2. Inside outer_function (looks at Enclosing): {x}")
outer_function()
print(f"3. Outside all functions (looks at Global): {x}")
```

    1. Inside inner_function (looks at Local): Local Scope
    4. Inside inner_function (using Built-in len): Length of Local is 11
    2. Inside outer_function (looks at Enclosing): Enclosing Scope
    3. Outside all functions (looks at Global): Global Scope
    


```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)
print(f"0! = {factorial(0)}")
print(f"1! = {factorial(1)}")
print(f"5! = {factorial(5)}")
print(f"7! = {factorial(7)}")
```

    0! = 1
    1! = 1
    5! = 120
    7! = 5040
    


```python
def fibonacci(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    return fibonacci(n - 1) + fibonacci(n - 2)
for i in range(8):
    print(f"n = {i}: {fibonacci(i)}")
```

    n = 0: 0
    n = 1: 1
    n = 2: 1
    n = 3: 2
    n = 4: 3
    n = 5: 5
    n = 6: 8
    n = 7: 13
    


```python
def sum_n(n):
    if n <= 1:
        return 1
    return n + sum_n(n - 1)
n = 10
recursive_result = sum_n(n)
formula_result = int(n * (n + 1) / 2)
print(f"Recursive sum_n({n}): {recursive_result}")
print(f"Formula result ({n}*({n}+1)/2): {formula_result}")
print(f"Match verified: {recursive_result == formula_result}")
```

    Recursive sum_n(10): 55
    Formula result (10*(10+1)/2): 55
    Match verified: True
    


```python
def reverse_string(s):
    if len(s) <= 1:
        return s
    return s[-1] + reverse_string(s[:-1])
print(f"Original: 'Python'      -> Reversed: '{reverse_string('Python')}'")
print(f"Original: 'Hello World' -> Reversed: '{reverse_string('Hello World')}'")
```

    Original: 'Python'      -> Reversed: 'nohtyP'
    Original: 'Hello World' -> Reversed: 'dlroW olleH'
    


```python
import time
from functools import lru_cache
def fibonacci(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    return fibonacci(n - 1) + fibonacci(n - 2)
@lru_cache(maxsize=None)
def fibonacci_cached(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    return fibonacci_cached(n - 1) + fibonacci_cached(n - 2)
n_value = 35
start_time = time.perf_counter()
result_un_cached = fibonacci(n_value)
end_time = time.perf_counter()
time_un_cached = end_time - start_time
start_time = time.perf_counter()
result_cached = fibonacci_cached(n_value)
end_time = time.perf_counter()
time_cached = end_time - start_time
print(f"Without memoization: Result = {result_un_cached}, Time = {time_un_cached:.5f} seconds")
print(f"With memoization:    Result = {result_cached}, Time = {time_cached:.5f} seconds")
print(f"Speedup factor:      {time_un_cached / time_cached:.1f}x faster")
```

    Without memoization: Result = 9227465, Time = 8.48784 seconds
    With memoization:    Result = 9227465, Time = 0.00052 seconds
    Speedup factor:      16216.7x faster
    


```python
import math
print(f"Square root of 144: {math.sqrt(144)}")
print(f"Value of pi: {math.pi}")
print(f"Ceiling of 4.3: {math.ceil(4.3)}")
```

    Square root of 144: 12.0
    Value of pi: 3.141592653589793
    Ceiling of 4.3: 5
    


```python
from math import factorial, gcd
print(f"Factorial of 6: {factorial(6)}")
print(f"GCD of 48 and 18: {gcd(48, 18)}")
```

    Factorial of 6: 720
    GCD of 48 and 18: 6
    


```python
import random
print("Five random integers between 1 and 100:")
for _ in range(5):
    random_number = random.randint(1, 100)
    print(random_number)
```

    Five random integers between 1 and 100:
    83
    53
    67
    89
    79
    


```python

```


---
**Score: 20**