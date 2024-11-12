---
layout: default  
permalink: /guides/f-string 
title: Python f-Strings Guide  
---

# Python f-Strings Guide

Python f-strings (formatted string literals) were introduced in Python 3.6 as a more readable and concise way to format strings. An f-string is prefixed with `f` or `F` and allows expressions inside curly braces `{}` that are evaluated at runtime.

---

## Basic Syntax

To use an f-string, place an `f` or `F` in front of your string literal and include expressions in `{}` within the string.

```python
name = "Alice"
greeting = f"Hello, {name}!"
print(greeting)  # Outputs: Hello, Alice!
```

---

## Expression Evaluation

You can insert any valid Python expression inside `{}`. This includes math operations, function calls, and even ternary operations.

```python
a = 10
b = 5
result = f"The sum of {a} and {b} is {a + b}."
print(result)  # Outputs: The sum of 10 and 5 is 15.
```

---

## Formatting Numbers

f-strings support formatting numbers for readability, precision, and padding.

- **Decimals**: Use `.nf` to format a float to `n` decimal places.
- **Commas**: Add `,` to include commas as thousands separators.
- **Percentage**: Use `%` to format as a percentage.

```python
value = 1234.56789
formatted = f"{value:.2f}"       # 2 decimal places: 1234.57
print(formatted)
formatted = f"{value:,.2f}"      # Thousands separator: 1,234.57
print(formatted)
formatted = f"{value:.1%}"       # Percentage format: 123456.8%
print(formatted)
```

---

## Padding and Alignment

Align text within a specified width using `:<`, `:>`, or `:^` for left, right, and center alignment, respectively.

```python
name = "Alice"
alignment = f"|{name:<10}|"      # Left align within 10 spaces
print(alignment)                 # Outputs: |Alice     |
alignment = f"|{name:>10}|"      # Right align within 10 spaces
print(alignment)                 # Outputs: |     Alice|
alignment = f"|{name:^10}|"      # Center align within 10 spaces
print(alignment)                 # Outputs: |  Alice   |
```

---

## Embedding Dictionaries and Lists

You can access values from dictionaries or lists within an f-string.

```python
person = {"name": "Alice", "age": 30}
greeting = f"{person['name']} is {person['age']} years old."
print(greeting)  # Outputs: Alice is 30 years old.

numbers = [1, 2, 3, 4]
message = f"The first number is {numbers[0]}"
print(message)  # Outputs: The first number is 1
```

---

## Using Functions and Method Calls

You can call functions or methods directly within an f-string.

```python
name = "Alice"
formatted = f"{name.upper()}!"   # Calls .upper() on name
print(formatted)                 # Outputs: ALICE!

def greet(name):
    return f"Hello, {name}!"

greeting = f"{greet('Bob')}"     # Calls greet() function
print(greeting)                  # Outputs: Hello, Bob!
```

---

## f-Strings with Escape Characters

To include literal braces `{}` in an f-string, double them `{{` and `}}`.

```python
text = f"{{This will be displayed as text inside braces}}"
print(text)  # Outputs: {This will be displayed as text inside braces}
```

---

## Multi-line f-Strings

To create a multi-line f-string, use triple quotes `"""` or `'''`.

```python
name = "Alice"
age = 30
bio = f"""Name: {name}
Age: {age}
Status: Active"""
print(bio)
```

---

## Examples with Formatting Options

- **Date Formatting**:

    ```python
    import datetime
    today = datetime.date.today()
    date_str = f"Today is {today:%B %d, %Y}"
    print(date_str)  # Outputs, e.g.: Today is October 31, 2024
    ```

- **Hexadecimal, Binary, and Octal**:

    ```python
    num = 255
    print(f"Hex: {num:#x}")      # Hexadecimal with prefix
    print(f"Binary: {num:#b}")   # Binary with prefix
    print(f"Octal: {num:#o}")    # Octal with prefix
    ```

---

### Summary of f-String Formatting Options

| Format Specifier | Description                         | Example                  |
|------------------|-------------------------------------|--------------------------|
| `:.nf`           | Decimal places                     | `{value:.2f}`            |
| `:,`             | Thousands separator                | `{value:,}`              |
| `%`              | Percentage                         | `{value:.1%}`            |
| `:<`, `:>`, `:^` | Alignment: left, right, center     | `{name:<10}`, `{name:>10}`, `{name:^10}` |
| `#x`, `#b`, `#o` | Hex, binary, octal with prefix     | `{num:#x}`, `{num:#b}`   |

---

**Additional Resources**  
For further details, check out the [Python 3 f-strings documentation](https://docs.python.org/3/reference/lexical_analysis.html#f-strings).

