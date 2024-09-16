---
layout: default
permalink: /guides/math
title: Math Module Functions Guide
---


# Math Module Functions Guide

Here are a few useful math functions that are included in the math module. You must use `include math` and `math.` to access these functions. For a full list of math functions refer to the Python reference here: [Math Module](https://www.w3schools.com/python/module_math.asp)



1. **`math.sqrt()`**:
   - **Description**: Returns the square root of a specified number.
   - **Example**:
     ```python
     import math
     result = math.sqrt(16)
     print(result)  # Outputs: 4.0
     ```
2. **`math.pow()`**:
   - **Description**: Similar to the built-in `pow()`, but specifically for floating-point numbers.
   - **Example**:
     ```python
     import math
     result = math.pow(2, 3)
     print(result)  # Outputs: 8.0
     ```
3. **`math.exp()`**:
   - **Description**: Returns \( e \) raised to the power of the provided number, where \( e \) is the base of natural logarithms.
   - **Example**:
     ```python
     import math
     result = math.exp(1)
     print(result)  # Outputs: 2.718281828459045
     ```
4. **`math.log()`**:
   - **Description**: Calculates the natural logarithm of a specified number. Optionally, a base can be specified.
   - **Example**:
     ```python
     import math
     result = math.log(10)
     print(result)  # Outputs: 2.302585092994046
     ```
5. **`math.factorial()`**:
   - **Description**: Returns the factorial of a number.
   - **Example**:
     ```python
     import math
     result = math.factorial(5)
     print(result)  # Outputs: 120
     ```
6. **`math.sin()`**:
   - **Description**: Returns the sine of a number given in radians.
   - **Example**:
     ```python
     import math
     result = math.sin(math.pi / 2)
     print(result)  # Outputs: 1.0
     ```
7. **`math.cos()`**:
   - **Description**: Returns the cosine of a number given in radians.
   - **Example**:
     ```python
     import math
     result = math.cos(0)
     print(result)  # Outputs: 1.0
     ```
8. **`math.tan()`**:
   - **Description**: Returns the tangent of a number given in radians.
   - **Example**:
     ```python
     import math
     result = math.tan(math.pi / 4)
     print(result)  # Outputs: 1.0
     ```
9. **`math.radians()`**:
   - **Description**: Converts an angle from degrees to radians.
   - **Example**:
     ```python
     import math
     result = math.radians(180)
     print(result)  # Outputs: 3.141592653589793
     ```
10. **`math.degrees()`**:
    - **Description**: Converts an angle from radians to degrees.
    - **Example**:
      ```python
      import math
      result = math.degrees(math.pi)
      print(result)  # Outputs: 180.0
      ```