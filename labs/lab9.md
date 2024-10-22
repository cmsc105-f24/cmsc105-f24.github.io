---
layout: default
permalink: lab/9
---

# Lab 9: More Lists

__Points Possible:__ 100

__Due:__ Thursday, October 31st

In this lab, we will write programs using Python _lists_.

Submission:
1.	Submit a Python file for each of the programs.

### Pair programming

Pair programming is a software development technique in which two programmers work together at one computer. One, the **driver**, writes code while the other, the **navigator**, reviews each line of code as it is typed in. **The two programmers switch roles frequently.**

* This is a **group assignment**, but you should each **turn in your code individually**. 
* Groups will be assigned at the beginning of lab.
* **Rules for groups work:**
    * Do not divide and conquer, i.e., do not assign each person an exercise to work on individually.
    * **Work together** on **each** exercise and share responsibilities, each person should have a chance to write code.

## Program 1: Concatenate Lists

Given two lists: `list1` and `list2`, write a program to concatenate the list elements index-wise (i.e. create a new list and print it). You may assume that both `list1` and `list2` are the same length.


Sample lists:
```python
list1 = ['W','ar','learn','pyt']
list2 = ['e','e','ing','hon']
```

Sample output:
```
['We', 'are', 'learning', 'python']
```

Save the program is `concatenate.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 20 points, result: 5 points)
**Total: 35 points**

# Program 2: Find Minimum

Write a function `findMin(list_of_numbers)` that takes as input argument a list `list_of_numbers` and returns the __index__ of the minimum value in the list.

Given:
```python
print(findMin([2,4,3,0,1]))
```

Sample output:
```
3                  
```

For above output, index of lowest element in the list i.e. 0 is lowest value with index 3.


Save the program is `min.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 20 points, result: 5 points)
**Total: 35 points**

## Program 3: Grades

Starter code found here:
[grades.py](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/grades.py)

Finish the Python program above that will analyze a list of student grades. The program will allow the user to input grades, and then it will perform various operations such as finding the highest and lowest grades, calculating the average, sorting the grades, and determining if a specific grade exists in the list. You must complete the `calculate_average(grades)`, `find_max(grades)`, and `find_max(grades)` functions. Complete the functions by adding your code where it says  `### YOUR CODE GOES HERE: ###`. After you complete the functions, test the code.

Sample run:
```
How many grades do you want to input? 5
Enter grade 1: 88
Enter grade 2: 92
Enter grade 3: 75
Enter grade 4: 85
Enter grade 5: 90

Menu:
1. Display all grades
2. Find the highest grade
3. Find the lowest grade
4. Calculate the average grade
5. Sort the grades
6. Check if a grade exists
7. Remove a grade
8. Exit

Enter your choice: 1
Grades: [88, 92, 75, 85, 90]

Enter your choice: 2
Highest grade: 92

Enter your choice: 4
Average grade: 86.0
```

Save the program is `grades.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 15 points, result: 5 points)
**Total: 30 points**



