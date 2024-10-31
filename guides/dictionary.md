---
layout: default  
permalink: /guides/dictionary  
title: Dictionary Methods Guide  
---

# Dictionary Methods Guide

Here are a few useful methods that work on dictionary objects in Python. For a full list of dictionary methods, refer to the Python reference here: [Python Reference Dictionary](https://www.w3schools.com/python/python_ref_dictionary.asp).

- **Create an empty dictionary**
    ```python
    dict1 = {}
    ```

- **Create a dictionary with key value pairs**
    ```python
    # Create a new dictionary with facts about the planet Mercury.
    mercury = {
        "name": "Mercury",
        "distance_from_sun_in_AU": 0.39,
        "rotational_period_in_earth_days": 58.6,
        "diameter_in_kilometers": 4879,
        "mass_in_kilograms": 3.3e23,
        "number_of_moons": 0
        }

    # Print individual values by using the key.
    print(mercury["name"])
    print(mercury["distance_from_sun_in_AU"])
    ```

- **`get(key)`**:
   - **Description**: Returns the value for the specified key if the key is in the dictionary.
   - **Parameters**:  
     - `key`: The key whose value you want to retrieve.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     age = person.get("age")
     print(age)  # Outputs: 25
     ```

- **`keys()`**:
   - **Description**: Returns a view object containing the keys of the dictionary.
   - **Parameters**: This method does not take any parameters.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     print(person.keys())  # Outputs: dict_keys(['name', 'age'])
     ```

- **`values()`**:
   - **Description**: Returns a view object containing the values of the dictionary.
   - **Parameters**: This method does not take any parameters.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     print(person.values())  # Outputs: dict_values(['Alice', 25])
     ```

- **`items()`**:
   - **Description**: Returns a view object containing key-value pairs (tuples) of the dictionary.
   - **Parameters**: This method does not take any parameters.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     print(person.items())  # Outputs: dict_items([('name', 'Alice'), ('age', 25)])
     ```

- **`pop(key)`**:
   - **Description**: Removes the specified key and returns its value.
   - **Parameters**:  
     - `key`: The key to remove.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     age = person.pop("age")
     print(age)  # Outputs: 25
     print(person)  # Outputs: {'name': 'Alice'}
     ```

- **`popitem()`**:
   - **Description**: Removes and returns the last inserted key-value pair as a tuple. Raises a `KeyError` if the dictionary is empty.
   - **Parameters**: This method does not take any parameters.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     item = person.popitem()
     print(item)  # Outputs: ('age', 25)
     print(person)  # Outputs: {'name': 'Alice'}
     ```

- **`update(other)`**:
   - **Description**: Updates the dictionary with key-value pairs from another dictionary or an iterable of key-value pairs.
   - **Parameters**:  
     - `other`: A dictionary or iterable of key-value pairs to update the dictionary.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     new_info = {"age": 26, "city": "New York"}
     person.update(new_info)
     print(person)  # Outputs: {'name': 'Alice', 'age': 26, 'city': 'New York'}
     ```

- **`clear()`**:
   - **Description**: Removes all elements from the dictionary, leaving it empty.
   - **Parameters**: This method does not take any parameters.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     person.clear()
     print(person)  # Outputs: {}
     ```

- **`copy()`**:
   - **Description**: Returns a shallow copy of the dictionary.
   - **Parameters**: This method does not take any parameters.
   - **Example**:
     ```python
     person = {"name": "Alice", "age": 25}
     person_copy = person.copy()
     print(person_copy)  # Outputs: {'name': 'Alice', 'age': 25}
     ```

- **`fromkeys(iterable, value)`**:
   - **Description**: Creates a new dictionary with keys from an iterable and all values set to the specified value.
   - **Parameters**:  
     - `iterable`: An iterable specifying the keys of the new dictionary.
     - `value` (optional): The value for all keys. Defaults to `None`.
   - **Example**:
     ```python
     keys = ["name", "age", "city"]
     default_dict = dict.fromkeys(keys, "Unknown")
     print(default_dict)  # Outputs: {'name': 'Unknown', 'age': 'Unknown', 'city': 'Unknown'}
     ```

