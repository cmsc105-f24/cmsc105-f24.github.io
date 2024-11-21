---
layout: default
permalink: lab/12
---

# Lab 12: Classes

__Points Possible:__ 100

__Due:__ Thursday, November 21st

In this lab, we will write programs using Python classes.

Submission:
1.	Submit a Python file for each of the programs.


## Program 1: Triangle

Design a class named `Triangle`. The `Triangle` class contains:	
- Three float data fields named `side1`, `side2` and `side3` to denote the three sides of the triangle.
- A constructor that creates a triangle with the specified `side1`, `side2` and `side3` with __default values 1.0__.
- A method named `getArea()` that returns the area of the triangle.
- A method named `getPerimeter()` that returns the perimeter of the triangle.

Write test code that prompts the user to enter three sides of a triangle. The program should create a triangle object with these sides and display the triangle’s area and perimeter.

Formula:

$$
s = (side1 + side2 + side3) / 2
$$

$$
area=\sqrt{s(s-side1)(s-side2)(s-side3)}
$$


Save the program as `triangle.py` and attach it to the Blackboard lab assignment.

Draw a UML diagram for the Triangle class and attach it to the Blackboard lab assignment. You can take a picture of the diagram, or use an online tool.

**Grading Rubric for the program:**  
(Comments: 5 points, class and methods: 30 points, UML: 5 points, test program: 5 points, UML: 5 points) 
**Total: 50 points**  


## Program 2: Practice

Create a class `Practice` that contains the following data fields:	
* `list1`
* `dict1`

Methods:
*	`__init__` that will initialize `list1` and `dict1`.
* `getList` that will return `list1`
* `setList` that will set `list1`
* `getDict` that will return the `dict1`
* `setDict` that will set the `dict1`
*	`findMinList` that returns the minimum values in `list1`.
*	`findMaxList` that returns the maximum values in `list1`.
*	`findSumDict` that returns the sum of values in `dict1`.

Write a test code that creates an instance of the `Practice` class and pass values for list and dictionary (you can use any arbitrary values). Print the minimum and maximum values in the list by calling the methods. Also, print the sum of values in dictionary by calling the `findSumDict` method.

Save the program as `Practice.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**  
(Comments: 5 points, class and functions: 40 points, test program: 5 points) 
**Total: 50 points**  


