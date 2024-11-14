---
layout: default
permalink: module/14
---

# Module 14: Classes

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 14 assignment.

**Note:** Create a text file called `module14.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Understand how a class is created and used in Python
* Explore the syntax around using classes in programs
* Use classes in programs to solve problems

---

Example class:

```python
import math

class Circle:
    # Create a constructor method, __init__
    def __init__(self, radius):
        self.radius = radius
    
    # Define a get perimeter function
    def getPerimeter(self):
        return 2 * math.pi * self.radius
    
    def getArea(self):
        return math.pi * self.radius ** 2
    
# Create a new instance of the Circle class
my_circle = Circle(10)

# Call the p
print(f"Perimeter = {my_circle.getPerimeter()}")
print(f"Area = {my_circle.getArea()}")
```



**Exercise: 1** Create a class `Rectangle` that contains the following:
* Data field: `length_side`, `width_side`
* Method:
    * A constructor using the two sides.
    * Get and set methods for the two data fields.
    * `getArea()` method that returns the area of rectangle:

$$
area = length\_side * width\_side
$$

Write test code (outside the class) that reads user input for the length and width of rectangle and creates an object of class Rectangle. Print the area of rectangle using getArea method.

Draw a UML diagram that represents the `Rectangle` class. Take a picture of the diagram and upload it to Blackboard.

---


**Exercise 2:** Create a class `Enrollment` that contains the following:
* Data fields: `course_number`, `semester`, `total_capacity`, `total_enrolled`, `total_available`.
* Methods:
    * A constructor with the above data fields (__init__)
    * Get and set methods for the data fields.
    * `checkStatus` that prints the "Enrollment successful!" message if total_available is more than 0 and it prints "Waitlist" message otherwise.

Write some test code (outside the class) that reads the values (input statements) for `course_number`, semester (example, Fall/Spring), `total_capacity`, `total_enrolled`, `total_available`. It then creates an object of Enrollment class using these values. Call `checkStatus` message using this object to print the enrollment status.


Draw a UML diagram that represents the `Enrollment` class. Take a picture of the diagram and upload it to Blackboard.

---


**Exercise 3:** Create a class `SummerCamp` that contains the following:
* Private data fields: `date`, `activity`, `location`.
* Methods:
    * A constructor with the above data fields (__init__)
    * Get and set methods for the data fields.

Write some test code (outside of the class) that reads the value for `date`, `activity` (example: soccer, baseball etc.) and `location`. Create an object of `SummerCamp` using these values. Change the value of location (put any arbitrary value) by calling the `setLocation` method and print the updated details of Summer camp. 

__Hint:__ You can use get methods to print the details.

Draw a UML diagram that represents the `SummerCamp` class. Take a picture of the diagram and upload it to Blackboard.






