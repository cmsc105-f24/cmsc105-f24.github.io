---
layout: default
permalink: /guides/string
title: String Methods Guide
---


# String Methods Guide

Here are a few useful string methods that work on string objects in Python. For a full list of string methods refer to the Python reference here: [Python Reference String](https://www.w3schools.com/python/python_ref_string.asp)


1. **`count()`**:
   - **Description**: Returns the number of times a specified value occurs in a string.
   - **Example**:
     ```python
     text = "hello world"
     count = text.count("l")
     print(count)  # Outputs: 3
     ```
2. **`find()`**:
   - **Description**: Searches the string for a specified value and returns the position of where it was found. If the value is not found, it returns -1.
   - **Example**:
     ```python
     text = "hello world"
     position = text.find("world")
     print(position)  # Outputs: 6
     ```
3. **`isalpha()`**:
   - **Description**: Returns True if all characters in the string are alphabetic (i.e., letters of the alphabet) and there is at least one character; otherwise, False.
   - **Example**:
     ```python
     text = "Hello"
     result = text.isalpha()
     print(result)  # Outputs: True
     ```
4. **`isnumeric()`**:
   - **Description**: Returns True if all characters in the string are numeric characters, and there is at least one character; otherwise, False.
   - **Example**:
     ```python
     number = "12345"
     result = number.isnumeric()
     print(result)  # Outputs: True
     ```
5. **`lower()`**:
   - **Description**: Converts all uppercase characters in a string to lowercase.
   - **Example**:
     ```python
     text = "HELLO WORLD"
     lower_text = text.lower()
     print(lower_text)  # Outputs: "hello world"
     ```
6. **`strip()`**:
   - **Description**: Returns a trimmed version of the string, removing both leading and trailing whitespace (and other characters, if specified).
   - **Example**:
     ```python
     text = "   hello world   "
     stripped_text = text.strip()
     print(stripped_text)  # Outputs: "hello world"
     ```
7. **`upper()`**:
   - **Description**: Converts all lowercase characters in a string to uppercase.
   - **Example**:
     ```python
     text = "hello world"
     upper_text = text.upper()
     print(upper_text)  # Outputs: "HELLO WORLD"
     ```