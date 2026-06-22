---
title: Chap-3(A)
date: 2026-05-21
author: Your Name
cell_count: 6
score: 5
---

```python
num = 0
if (num < 0):
    print("negative")
elif (num > 0):
    print("positive")
else:
    print("zero")
```

    zero
    


```python
age = 15
if(age > 13 < 19):
    print("teenager")
else:
    print("not a teenager")
    
```

    teenager
    


```python
num1 = 15
num2 = 15
if(num1>num2):
    print("greater")
elif(num1<num2):
    print("lesser")
else:
    print("equal")
```

    equal
    


```python
score = 45
if (score >= 50):
    print("Pass")
else:
    print("Fail")
    
```

    Fail
    


```python
time = float(input("Enter the time (0-23): "))
if 5 <= time < 12:
    print("Morning")
elif 12 <= time < 18:
    print("Afternoon")
elif (18 <= time <= 23) or (0 <= time < 5):
    print("Evening")
else:
    print("Invalid hour!")

```

    Enter the time (0-23):  25
    

    Invalid hour!
    


```python

```


---
**Score: 5**