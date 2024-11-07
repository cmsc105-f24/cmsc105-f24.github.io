---
layout: default  
permalink: /guides/file 
title: File I/O Guide  
---

# File I/O Guide

Python provides several built-in functions to work with files, making it easy to read from and write to files on your system. Here’s a summary of key file operations in Python.

- **`open(file, mode)`**:
   - **Description**: Opens a file and returns a file object. This is the first step in working with a file.
   - **Parameters**:  
     - `file`: The name of the file (including path if needed).
     - `mode`: Specifies the mode in which to open the file.
       - `'r'`: Read (default). Opens a file for reading.
       - `'w'`: Write. Creates a new file or overwrites if the file exists.
       - `'a'`: Append. Adds to the end of the file if it exists.
       - `'r+'`: Read and write.
   - **Example**:
     ```python
     file = open("example.txt", "r")  # Opens a file in read mode
     print(file.read())  # Reads file content
     file.close()  # Closes the file
     ```

- **`read(size)`**:
   - **Description**: Reads up to `size` bytes from the file. If size is not specified, reads the entire file.
   - **Parameters**:  
     - `size` (optional): The number of bytes to read. Reads the entire file if not specified.
   - **Example**:
     ```python
     with open("example.txt", "r") as file:
         content = file.read(10)  # Reads the first 10 characters
         print(content)
     ```

- **`readline()`**:
   - **Description**: Reads a single line from the file.
   - **Example**:
     ```python
     with open("example.txt", "r") as file:
         first_line = file.readline()
         print(first_line)  # Outputs the first line
     ```

- **`readlines()`**:
   - **Description**: Reads all lines in a file and returns them as a list.
   - **Example**:
     ```python
     with open("example.txt", "r") as file:
         lines = file.readlines()
         print(lines)  # Outputs a list of lines
     ```

- **`write(data)`**:
   - **Description**: Writes data to a file. If the file is opened in write mode (`'w'`), it will overwrite existing content.
   - **Parameters**:  
     - `data`: The string to write to the file.
   - **Example**:
     ```python
     with open("example.txt", "w") as file:
         file.write("Hello, world!")
     ```

- **`writelines(lines)`**:
   - **Description**: Writes a list of strings to a file.
   - **Parameters**:  
     - `lines`: A list of strings to write.
   - **Example**:
     ```python
     with open("example.txt", "w") as file:
         lines = ["Line 1
", "Line 2
", "Line 3
"]
         file.writelines(lines)
     ```

- **`close()`**:
   - **Description**: Closes the file. Always close files to free up system resources.
   - **Example**:
     ```python
     file = open("example.txt", "r")
     print(file.read())
     file.close()
     ```

- **`with` statement**:
   - **Description**: A context manager that automatically closes the file after the block of code runs, making code cleaner and safer.
   - **Example**:
     ```python
     with open("example.txt", "r") as file:
         content = file.read()
         print(content)
     # File is automatically closed after this block
     ```

- **File Modes Summary**:
   - `'r'`: Read only.
   - `'w'`: Write only (overwrites if file exists).
   - `'a'`: Append only.
   - `'r+'`: Read and write.


