---
layout: default
permalink: /guides/pymath
title: Python Math Guide
---


# Python Built-In Math Functions

Here are a few useful math functions that are built into the Python programming language. (No need to `include math`).


1. **`abs()`**:
   - **Description**: Returns the absolute value of a specified number. The absolute value of a number is the number without its sign.
   - **Example**:
     ```python
     number = -20
     absolute_value = abs(number)
     print(absolute_value)  # Outputs: 20
     ```
2. **`pow()`**:
   - **Description**: Returns the value of a number raised to the power of another number. It is equivalent to using the exponentiation operator `**`.
   - **Example**:
     ```python
     base = 2
     exp = 3
     result = pow(base, exp)
     print(result)  # Outputs: 8
     ```
3. **`round()`**:
   - **Description**: Rounds a floating-point number to a specified number of decimal places or to the nearest integer if no number of decimal places is specified.
   - **Example**:
     ```python
     number = 3.14159
     rounded_number = round(number, 2)
     print(rounded_number)  # Outputs: 3.14
     ```
4. **`max()`**:
   - **Description**: Returns the largest of the input values.
   - **Example**:
     ```python
     numbers = [1, 5, 10, 20]
     max_value = max(numbers)
     print(max_value)  # Outputs: 20
     ```
5. **`min()`**:
   - **Description**: Returns the smallest of the input values.
   - **Example**:
     ```python
     numbers = [1, 5, 10, 20]
     min_value = min(numbers)
     print(min_value)  # Outputs: 1
     ```
6. **`sum()`**:
   - **Description**: Returns the sum of a list or tuple.
   - **Example**:
     ```python
     numbers = [1, 2, 3, 4, 5]
     total = sum(numbers)
     print(total)  # Outputs: 15
     ```
