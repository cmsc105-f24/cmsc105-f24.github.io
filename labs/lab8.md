---
layout: default
permalink: lab/8
---

# Lab 8: Lists

__Points Possible:__ 100

__Due:__ Thursday, October 24th

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

## Program 1: Color counter

Write a function called `countColor` that takes as input a string of colors separated by spaces called `colorString` and a second input called `colorToCount`. The function should count `colorToCount` in the string of colors. Please test this function by reading input values from the user (input statement).

Please use __lists__ to solve this problem.

Sample run:
```
Enter colors: Red Blue Red Green Yellow
Enter color to count: Red
Red appears 2 times
```

Hint:
* You will need to use the `string.split()` function to convert a string to a list. The split function will split at each instance of a space character.  
* Example:

```python
colorString = "Red Yellow Orange Green Blue"
print(colorString)
colorList = colorString.split()
print(colorList)
```

Save the program is `colors.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 20 points, result: 5 points)
**Total: 35 points**

# Program 2: Find Names

Write a function `findName` that takes as input a string of names separated by spaces and a second input argument called `nameToFind`. The function should return the first position of `nameToFind` in the string of names and return -1 if `nameToFind` doesn’t exist in the string of names. Please test this function by reading input values from the user (input statement).

Please solve this using __lists__.
Hint: The `list.index(x)` function can be used in finding the `nameToFind` in a list of names.

Sample run:
```
Enter names: Della Shweta Bob Steve Shweta
Enter a name to find: Shweta
Shweta exists at the position number 2
```

Save the program is `names.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 20 points, result: 5 points)
**Total: 35 points**

## Program 3: Scores

Write a program that reads an unspecified number of scores and determines how many scores are above or equal to the average and how many scores are below the average. 

Sample run:
```
Enter scores: 90 80 85 65 55
The average score is 75.0
3 scores are above and equal to the average
2 scores are below the average
```

Save the program is `scores.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 15 points, result: 5 points)
**Total: 30 points**



