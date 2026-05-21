---
title: Chap-3(C)
date: 2026-05-19
author: Your Name
cell_count: 4
score: 0
---

```python
secret_number = 7
guess = None
while guess != secret_number:
    guess = int(input("Guess the secret number: "))
    if guess != secret_number:
        print("Wrong guess! Try again.")
print("Correct! You guessed the secret number.")
```

    Guess the secret number:  3
    

    Wrong guess! Try again.
    

    Guess the secret number:  4
    

    Wrong guess! Try again.
    

    Guess the secret number:  7
    

    Correct! You guessed the secret number.
    


```python
number = 10

while number > 0:
    print(number)
    number -= 1
```

    10
    9
    8
    7
    6
    5
    4
    3
    2
    1
    


```python
number = int(input("Enter a positive integer: "))
factorial = 1
current = number
while current > 1:
    factorial *= current 
    current -= 1         
print(f"The factorial of {number} is {factorial}")
```

    Enter a positive integer:  5
    

    The factorial of 5 is 120
    


```python

```


---
**Score: 0**