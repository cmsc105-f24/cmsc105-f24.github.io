---
layout: default  
permalink: /guides/random  
title: Random Library Guide  
---

# Python Random Library Guide  

The Python `random` module provides tools for generating random numbers, selecting random elements, and more. This guide covers the most commonly used functions.

For more information, check the [Python `random` documentation](https://docs.python.org/3/library/random.html).

---

## **1. `random()`**  

- **Description**: Generates a random floating-point number between 0.0 (inclusive) and 1.0 (exclusive). 
 
- **Example**:  
```python
import random
print(random.random())  # Outputs a number like 0.45238
```

---

## **2. `randint(a, b)`**  

- **Description**: Returns a random integer between `a` and `b` (both inclusive).  
- **Example**:  
```python
import random
print(random.randint(1, 10))  # Outputs an integer between 1 and 10
```

---

## **3. `choice(seq)`**  

- **Description**: Returns a random element from a non-empty sequence (e.g., list, string, tuple).  
- **Example**:  
```python
import random
items = ["apple", "banana", "cherry"]
print(random.choice(items))  # Outputs a random item from the list
```

---

## **4. `choices(seq, k)`**  

- **Description**: Returns a list of `k` random elements from the sequence, with replacement.  
- **Example**:  
```python
import random
items = ["apple", "banana", "cherry"]
print(random.choices(items, k=3))  # Outputs something like ['banana', 'apple', 'cherry']
```

---

## **5. `shuffle(seq)`**  

- **Description**: Shuffles a sequence in place (mutates the original sequence).  
- **Example**:  
```python
import random
items = ["apple", "banana", "cherry"]
random.shuffle(items)
print(items)  # Outputs a shuffled version of the list
```

---

## **6. `sample(seq, k)`**  

- **Description**: Returns a list of `k` unique elements randomly chosen from the sequence, without replacement.  
- **Example**:  
```python
import random
items = ["apple", "banana", "cherry", "date"]
print(random.sample(items, k=2))  # Outputs something like ['cherry', 'banana']
```

---

## **7. `uniform(a, b)`**  

- **Description**: Returns a random floating-point number between `a` and `b`.  
- **Example**:  
```python
import random
print(random.uniform(1.5, 3.5))  # Outputs a float like 2.473
```

---

## **8. `randrange(start, stop, step)`**  

- **Description**: Returns a randomly selected element from the range `[start, stop)` with the given step.  
- **Example**:  
```python
import random
print(random.randrange(1, 10, 2))  # Outputs a random odd number between 1 and 9
```

---

## **9. `seed(value)`**  

- **Description**: Initializes the random number generator to make results reproducible.  
- **Example**:  
```python
import random
random.seed(42)
print(random.random())  # Same output every time the script is run
```

---

## **10. Generating Random Booleans**  

- **Description**: You can simulate random boolean values using `choice`.  
- **Example**:  
```python
import random
print(random.choice([True, False]))  # Outputs True or False randomly
```

---
