---
layout: default  
permalink: lab/14  
---

# Lab 14: Coding Lab: Choose your own adventure

__Points Possible:__ 100  

__Due:__ Thursday, December 12th  

In this lab, you will use your knowledge of Python to solve programming challenges.

**Submission:**  
Submit a Python file for each of the programs, along with any output images saved during execution.

---

### Pair programming

Pair programming is a software development technique in which two programmers work together at one computer. One, the **driver**, writes code while the other, the **navigator**, reviews each line of code as it is typed in. **The two programmers switch roles frequently.**

* This is a **group assignment**, but you should each **turn in your code individually**. 
* Groups will be assigned at the beginning of lab.
* **Rules for groups work:**
    * Do not divide and conquer, i.e., do not assign each person an exercise to work on individually.
    * **Work together** on **each** exercise and share responsibilities, each person should have a chance to write code.


## Instructions:

Solve any **TWO** of the following problems.

---

### **1. Grade Calculator**

Write a program that calculates the final grade for a student based on their scores in different categories. Use a dictionary to store category weights (e.g., homework, exams, participation). Your program should:
- Ask the user to input scores for each category.
- Calculate the weighted average and print the final grade as a percentage.
$$
\text{Final Grade} = \sum (\text{Category Weight} \times \text{Category Score})
$$


**Weights:**
```Python
category_weights = {"homework": 0.4, "exams": 0.5, "participation": 0.1}
```

**Example Input:**
```
Please enter the homework score: 85
Please enter the exam score: 90
Please enter the participation score: 100
```

**Example Output:**
```
Final Grade: 89.5%
```

Save the program as `grade_calc.py` and attach it to the Blackboard lab assignment.

---

### **2. Simple Banking System**

Write a program to simulate a basic banking system using a dictionary to store account balances. The program should:
1. Allow users to create accounts.
2. Allow users to deposit or withdraw money.
3. Print account details.

**Example Interaction:**
```
1. Create Account
2. Deposit
3. Withdraw
4. View Account
5. Exit
Choose an option: 1
Enter account name: Alice
Choose an option: 2
Enter account name: Alice
Enter deposit amount: 100
Choose an option: 4
Account: Alice, Balance: $100
Choose an option: 5
```

Save the program as `simple_bank.py` and attach it to the Blackboard lab assignment.

---

### **3. Multiplication Table Generator**

Write a program that generates a multiplication table for a given range of numbers. The user specifies the starting and ending numbers, and the program displays the table in a formatted grid.

**Example Input:**
```
Start: 1
End: 5
```

**Example Output:**
```
    1   2   3   4   5
1   1   2   3   4   5
2   2   4   6   8  10
3   3   6   9  12  15
4   4   8  12  16  20
5   5  10  15  20  25
```

Save the program as `mult_table.py` and attach it to the Blackboard lab assignment.

---

### **4. Simple Class: Library Book Tracker**

Write a class `Book` that keeps track of books in a library. Each `Book` should have attributes for the title, author, and whether the book is checked out. Your program should:
1. Allow users to add new books.
2. Allow users to check out or return books.
3. Display all available books.

**Example Interaction:**
```
1. Add Book
2. Check Out Book
3. Return Book
4. View All Books
5. Exit
Choose an option: 1
Enter title: Python Basics
Enter author: John Doe
Choose an option: 4
Available Books:
- Python Basics by John Doe
Choose an option: 2
Enter title to check out: Python Basics
Choose an option: 4
No books available.
Choose an option: 5
```

Save the program as `book_track.py` and attach it to the Blackboard lab assignment.

---


