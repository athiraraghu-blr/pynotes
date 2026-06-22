---
title: Chap-2(B)
date: 2026-06-22
author: Your Name
cell_count: 6
score: 5
summary: Python Notes — chap 2(b) notebook with Python examples and exercises.
---

```python
age = int(input("Enter your age: "))
print(f"you are {age} years old.")
```

    Enter your age:  25
    

    you are 25 years old.
    


```python
num = input("Enter two numbers: ").split()
a = int(num[0])
b = int(num[1])
print(a+b)
```

    Enter two numbers:  14 11
    

    25
    


```python
flow = 7.9
int_to_float = int(flow)

print(int_to_float)
```

    7
    


```python
x = 2
y = 8
print(x**y)
```

    256
    


```python
num = int(input("Enter a number: "))
if num % 2 == 0:
    print("Even")
else:
    print("Odd")
```

    Enter a number:  23
    

    Odd
    


```python

```


---
**Score: 5**