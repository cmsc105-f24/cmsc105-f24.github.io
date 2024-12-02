---
layout: default
permalink: /lecture/q4
---

# Quiz Review 

## Background 
The quiz will be based on the topics covered in weeks 11 through 14. There are 2 programming problems to help you prepare for Quiz 4. You are allowed to use the Thonny IDE. You may also use the guides provided on the course web page: [https://cmsc105-f24.github.io/guides](https://cmsc105-f24.github.io/guides)


## Practice Problem 1 

You are tasked with creating a Python program to process a data file. The file, named `sales_data.txt`, contains information about daily sales in the following format:

**sales_data.txt**
```
2024-01-01,100.50
2024-01-02,200.75
2024-01-03,150.00
2024-01-04,175.25
2024-01-05,300.00
```

Each line contains a date and a sales amount separated by a comma.

The `sales_data.txt` file can be downloaded using this link: [sales_data.txt](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/sales_data.txt)


**Remember** to save the file in the same folder as your program.


Write a program to:

* Read the contents of the `sales_data.txt` file.
* Calculate and print the total sales.
* Calculate and print the average sales amount.
* Find and print the date with the highest sales.
* Save a new file called `summary_sales.txt` with the following information:
    * Total sales.
    * Average sales amount.
    * Date with the highest sales.

**Sample output:**
```
Total Sales: $926.50
Average Sales: $185.30
Highest Sales: $300.00 on 2024-01-05
```

The contents of `summary_sales.txt` should be:

**summary_sales.txt**
```
Total Sales: $926.50
Average Sales: $185.30
Highest Sales: $300.00 on 2024-01-05
```




## Practice Problem 2 (50 points)

Create a `Book` class with the following private data fields: `title`, `author`, `isbn`, `price`, `num_pages`, and the following methods:
* A constructor (`__init__`) with the arguments `title`, `author`, `isbn`, `price`, `num_pages`. Please note that all fields except `price` and `num_pages` are strings. The `price` is of type `float`, and `num_pages` is of type `int`.
* Get and set methods for the price field only.
* `printDetails()` method that prints the `title`, `author`, `isbn`, `price`, and `num_pages`.
* `isAffordable()` method that returns `True` if the price is less than $20, and `False` otherwise.

<br />

Draw the **UML diagram** for the `Book` class.

<br />

Write test code that prompts the user to enter the `title`, `author`, `isbn`, `price`, and `num_pages`. Initiate an object of the `Book` class, print the details, and display whether the book is affordable.

<br />

**Sample run:**
```
Enter book title: Python Programming
Enter author: John Doe
Enter ISBN: 978-1234567890
Enter price: 19.99
Enter number of pages: 350

Book Details:

Title: Python Programming
Author: John Doe
ISBN: 978-1234567890
Price: $19.99
Number of Pages: 350

Is this book affordable? Yes
```



