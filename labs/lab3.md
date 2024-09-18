---
layout: default
permalink: lab/3
---

# Lab 3: Math and Strings in Python

__Points Possible:__ 100

__Due:__ Thursday, September 19th 

In this lab, we will practice the concepts learned in week three. We will use math module functions, string functions, and Python programming to solve the problems.

Submission:
1.	Submit a Python file for each of the four programs.

### Pair programming

Pair programming is a software development technique in which two programmers work together at one computer. One, the **driver**, writes code while the other, the **navigator**, reviews each line of code as it is typed in. **The two programmers switch roles frequently.**

* This is a **group assignment**, but you should each **turn in your code individually**. 
* Groups will be assigned at the beginning of lab.
* **Rules for groups work:**
    * Do not divide and conquer, i.e., do not assign each person an exercise to work on individually.
    * **Work together** on **each** exercise and share responsibilities, each person should have a chance to write code.


## Program 1: Math and Strings


Write a program that prints the results of the following:

1.	$sin(2 \pi)$				(you can use `math.pi`)
2.	$log(16)$				(use natural log)
3.	`round(-12.5)`
4.	
   ```python
   string_val="Introduction to Computing."
   string_val[:-1]
   ```
5.	
   ```python
   string_val="Introduction to Computing."
   string_val[2:]
   ```

Save the program is `math_and_strings.py` and attach it to the Blackboard lab assignment. 


## Program 2: Compute Interest

Write a program that reads the values of total amount and interest rate. Then prints the value of the interest amount. Please display the result up to 2 decimal places.

Use the formula:

$$
interestAmount = totalAmount * interestRate
$$

Save the program is `interest.py` and attach it to the Blackboard lab assignment. 

## Program 3: Math Library

Using math library functions, write a program that reads the value of 2 numbers `a`, `b` and solve the following equations:

$$
\sqrt{(a^2 + b^2)}
$$

$$
a^b + \log a
$$

Please display the results up to 2 decimal places. Please use `math.log` function for natural log.

Save the program is `library.py` and attach it to the Blackboard lab assignment. 


## Program 4: Grade Count

Suppose the text below indicates the grades of students and the text is stored in a variable, compute the total count of students who got "Grade-A", "Grade-B" and "Grade-C" and display the counts. **Hint:** You can use the `count` function.

string_val = "User1:Grade-A, User2:Grade-B, User3:Grade-C, User4:Grade-A, User5:Grade-B, User6: Grade-A, User7: Grade-C, User8: Grade-B, User9:Grade-A, User10: Grade-A, User11: Grade-C, User12: Grade-A, User13: Grade-B, User14: Grade-C, User15: Grade-A"

Save the program is `grades.py` and attach it to the Blackboard lab assignment. 


* Starter code here [grades.py](https://raw.githubusercontent.com/cmsc105-f24/cmsc105-f24.github.io/main/labs/grades.py)

## Grading Rubric for the programs:

<table>
    <tr>
        <td>Grading</td>
        <td>Points Possible</td>
    </tr>
    <tr>
        <td>Appropriate header and comments</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Input</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Computation</td>
        <td>10</td>
    </tr>
    <tr>
        <td>Print output</td>
        <td>5</td>
    </tr>
</table>



**TOTAL	25 points for each program**

---