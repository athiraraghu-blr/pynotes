---
title: Chap-4
date: 2026-06-22
author: Your Name
cell_count: 21
score: 20
summary: Python Notes — chap 4 notebook with Python examples and exercises.
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
text = input("Enter a sentence: ")
vowels = sum(1 for c in text if c.lower() in 'aeiou')
digits = sum(1 for c in text if c.isdigit())
spaces = sum(1 for c in text if c.isspace())
consonants = sum(1 for c in text if c.isalpha()) - vowels
print(f"Vowels: {vowels}")
print(f"Consonants: {consonants}")
print(f"Digits: {digits}")
print(f"Spaces: {spaces}")
```

    Enter a sentence:  hello myself athira r dob 14-12-2000
    

    Vowels: 7
    Consonants: 14
    Digits: 8
    Spaces: 5
    


```python
text = input("Enter a sentence: ")
words = text.split(" ")
reversed_words = [word[::-1] for word in words]
result = " ".join(reversed_words)
print(f"Result: {result}")
```

    Enter a sentence:  how are you jupyter
    

    Result: woh era uoy retypuj
    


```python
text = input("Enter a sentence: ")
letters = {char.lower() for char in text if char.isalpha()}
if len(letters) == 26:
    print("The string is a pangram.")
else:
    print("The string is NOT a pangram.")
```

    Enter a sentence:  The quick brown fox jumps over the lazy dog
    

    The string is a pangram.
    


```python
text = input("Enter the main string: ")
old_word = input("Enter the word to replace: ")
new_word = input("Enter the new word: ")
words = text.split(" ")
modified_words = [new_word if word == old_word else word for word in words]
result = " ".join(modified_words)
print(f"Result: {result}")
```

    Enter the main string:  hello yuva
    Enter the word to replace:  yuva
    Enter the new word:  priya
    

    Result: hello priya
    


```python
items = [1, 3, 2, 1, 4, 3, 2, 5, 1]
seen = set()
unique_items = []
for item in items:
    if item not in seen:
        unique_items.append(item)
        seen.add(item)
print(f"Original list: {items}")
print(f"Result list:   {unique_items}")
```

    Original list: [1, 3, 2, 1, 4, 3, 2, 5, 1]
    Result list:   [1, 3, 2, 4, 5]
    


```python
def flatten_list(nested_list):
    flat_list = []
    for item in nested_list:
        if isinstance(item, list):
            flat_list.extend(flatten_list(item))
        else:
            flat_list.append(item)
    return flat_list
nested = [1, [2, 3], [4, [5, 6]], 7, [8]]
result = flatten_list(nested)
print(f"Original nested list: {nested}")
print(f"Flattened list:       {result}")
```

    Original nested list: [1, [2, 3], [4, [5, 6]], 7, [8]]
    Flattened list:       [1, 2, 3, 4, 5, 6, 7, 8]
    


```python
numbers = [12, 35, 1, 10, 34, 1, 35]
unique_nums = list(set(numbers))
if len(unique_nums) < 2:
    print("List must have at least two unique elements.")
else:
    largest = second_largest = float('-inf')
    smallest = second_smallest = float('inf')
    for num in unique_nums:
        if num > largest:
            second_largest = largest
            largest = num
        elif num > second_largest:
            second_largest = num
        if num < smallest:
            second_smallest = smallest
            smallest = num
        elif num < second_smallest:
            second_smallest = num

    print(f"Original list:   {numbers}")
    print(f"Second largest:  {second_largest}")
    print(f"Second smallest: {second_smallest}")
```

    Original list:   [12, 35, 1, 10, 34, 1, 35]
    Second largest:  34
    Second smallest: 10
    


```python
numbers = [10, 20, 30, 40, 50]
k = int(input("Enter the number of positions to rotate (k): "))
n = len(numbers)
k = k % n
rotated_list = numbers[-k:] + numbers[:-k]
print(f"Original list: {numbers}")
print(f"Rotated list:  {rotated_list}")
```

    Enter the number of positions to rotate (k):  10
    

    Original list: [10, 20, 30, 40, 50]
    Rotated list:  [10, 20, 30, 40, 50]
    


```python
data = (10, 20, 30, 40, 50)
a, b, c, d, e = data
for index, value in enumerate((a, b, c, d, e)):
    print(f"Index {index}: {value}")
```

    Index 0: 10
    Index 1: 20
    Index 2: 30
    Index 3: 40
    Index 4: 50
    


```python
students = [("Alice", 85), ("Bob", 92), ("Charlie", 78), ("Diana", 95)]
students.sort(key=lambda x: x[1], reverse=True)
for name, mark in students:
    print(f"{name}: {mark}")
```

    Diana: 95
    Bob: 92
    Alice: 85
    Charlie: 78
    


```python
data = ('apple', 'banana', 'apple', 'cherry', 'banana', 'apple')
result = {item: data.count(item) for item in data}
print(result)
```

    {'apple': 3, 'banana': 2, 'cherry': 1}
    


```python
A = {101, 102, 103, 104}
B = {103, 104, 105, 106}
print(A & B)
print(B - A)  
print(A - B)  
```

    {104, 103}
    {105, 106}
    {101, 102}
    


```python
A = {1, 2, 3}
B = {1, 2, 3, 4, 5}
print(A.issubset(B))    
print(B.issuperset(A))   
```

    True
    True
    


```python
words = ["group", "freeze", "yatch", "freeze", "depth", "hope", "yatch", "hope", "greet", "group"]
frequency = {}
for word in words:
    if word in frequency:
        frequency[word] += 1
    else:
        frequency[word] = 1
print(frequency)
print(f"Number of unique words: {len(frequency)}")
```

    {'group': 2, 'freeze': 2, 'yatch': 2, 'depth': 1, 'hope': 2, 'greet': 1}
    Number of unique words: 6
    


```python
dict1 = {"a": 2, "b": 3, "c": 4}
dict2 = {"c": 3, "d": 4, "e": 5}

merged = dict1 | dict2
print(merged)
```

    {'a': 2, 'b': 3, 'c': 3, 'd': 4, 'e': 5}
    


```python
student_marks = {
    "Alice": 85,
    "Bob": 95,
    "Charlie": 78,
    "Diana": 95,
    "Ethan": 88
}
highest_mark = max(student_marks.values())
top_students = [name for name, mark in student_marks.items() if mark == highest_mark]
print(f"Total students evaluated: {len(student_marks)}")
print(f"Highest Mark: {highest_mark}")
print(f"Top Student(s): {', '.join(top_students)}")
```

    Total students evaluated: 5
    Highest Mark: 95
    Top Student(s): Bob, Diana
    


```python

```


---
**Score: 20**