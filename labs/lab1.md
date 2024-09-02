---
layout: default
permalink: lab/1
---

# Lab 1: Math expressions and input/output 

__Points Possible:__ 100

__Due:__ Thursday, September 5th 

In this lab, we will practice several Python statements from the __IDLE__ (Integrated Development and Learning Environment). Then we will write a program that will input data do a small calculation and then output (print) the result.  

* Read through this document carefully, and practice running Python expressions using IDLE. 
* Run the commands and check their outputs. 
* Please copy and paste the IDLE output into a file called `lab1.txt` and attach it to the lab 1 assignment on Blackboard. (75 Points)
* We will also write and execute a Python program. 
* The program file `circle.py` is required for submission on Blackboard as well. (25 points)


## Objectives

The purpose of this assignment is to give an experience with:
* Using the IDLE command prompt and writing a program.
* Converting mathematical expressions into Python expressions.
* Doing input and output at the command line.
* Using strings.

## Part 1: The Python Prompt

In this lab, I have you type expressions into Python. First, you must start IDLE. When I show you an expression that starts with a prompt like this:
```python
>>> 4
```
Then, that means you should type the expression into the Python Shell window in IDLE.
For example, this expression:
```python
>>> 1 + 5
```
means that you should type the part that follows the prompt, meaning the expression `1 + 5`, into Python IDLE prompt, but not the `>>>` part.


### float and int

As we discussed in the lecture yesterday, there are three main data types that we will be using: `int`, `float`, `string`. There is a built-in function called `type` in Python that will tell you which of the two types of number you're looking at. Give it a try:
```python
>>> type(5)
```

<class 'int'>
<br />That means that the number `5` is treated as an `int`.


```python
>>> type(2.5)
```

<class 'float'>

That means that the number `2.5` is treated as an `float`.

<br />
You can convert easily between the numeric types:

```python
>>> float(2)
```
2.0

```python
>>> int(2.5)
```
2

```python
>>> int('100')
```
100

```python
>>> float('100')
```
100.0

But this doesn't work:
```python
>>> int('200.5')
```

Traceback (most recent call last):
File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '200.5'

<br />

It's ok to convert a string that looks like an `int` into an `int`, but it won't convert a string that looks like a `float` into an `int`.


### The input function

The `input` function in Python is a convenient way to let the user enter information that your program can use. 

```python
>>> input()
Hello
```
'Hello'


* What happened there was that I entered the `input()` statement, which is a function call, and then Python stopped and waited for me to enter a line. 
* I typed Hello and then hit `Enter`.
* It showed me what the result of that was: the string 'Hello'.

Notice that the string was shown with quotation marks around it. That's because Python showed me that string as the result of evaluating an expression, not as the output from a `print` statement.

It's more useful to use an assignment statement to save the result of the `input()` function call so that you can use it later.

```python
>>> x = input()
Hello
```

That statement stores the result of the `input()` function call into a variable called `x`. 

```python
>>> x
```
'Hello'

```python
>>> x = input()
100
```

```python
>>> x
```
'100'

<br />

It displays all the input values with quotation marks, meaning it displays them as a string.
This is where we use `eval` function that converts the key strokes entered by a user into a value.

You can also supply a string as an argument to the `input` function and it will display the string as a prompt to the user:
```python
>>> x = input('Please enter a number: ')
Please enter a number: 100
>>> x + 1
```
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
TypeError: Can't convert 'int' object to str implicitly

<br />

It's important to see error messages like this so that you can start to learn what they mean.
Here it's trying to convert an `int` (integer) into a `str` (string). Python does not let you do math using a string and a number, even if the string looks like a number.

Try this,

```python
>>> x = eval(input('Please enter a number: '))
Please enter a number: 100
>>> x + 1
```

Do you observe any error now? That’s how `eval` works! 


### Converting input to a float

You can call the `float` function directly on the result of the `input` function:

```python
>>> x = float(input('Please enter a number: '))
123.5
```

Be mindful of the parentheses: They must match up.

Now have a look at what's in the variable `x`:

```python
>>> x
```
123.5

```python
>>> type(x)
```
<class 'float'>


You can call the `float` function on the variable after the `input` function:

```python
>>> x = input('Please enter a number: ')
123.5
>>> x = float(x) + 1
```

Here, we are using the variable `x` twice, the original value of `x` entered by the user will be updated when converting to `float(x)`.

```python
>>> x
```
124.5

```python
>>> type(x)
```
<class 'float'>

You can also use another variable `y` so that the original value of `x` does not change. For example,

```python
>>> x = input('Please enter a number: ')
123.5
>>> y = float(x) + 1
```

Now try this,
```python
>>> x
```
'123.5'

```python
>>> y
```
124.5


## Part 2: Program Assignment


### Sample Code (for reference, please do NOT include this in your submission):

The code below calculates the sum of two numbers. It reads (takes as input) two numbers and displays the sum.

```python
''' 
Author name: Dr. David Balash
This program calculates the sum of two numbers
'''

number1 = eval(input("Enter number 1"))  # Asks users to input number 1
number2 = eval(input("Enter number 2"))  # Asks users to input number 2

# Calculate the sum of the two numbers
add_result = number1 + number2

# Print the results
print("Sum of two numbers is", add_result)

```

Notes:
* It starts with a multi-line comment block where you describe your program. 
* You can use `#` sign for this or `'''` three single quotes for multi-line comments.
* The program then reads input with the Python `input` function.
* The input entered will be in `string` format.
* The Python `eval` function will convert it into a value.



The basic structure of any program will have the following components:
* Comments
* Input
* Computation (addition in example above)
* Output

You can choose any meaningful names for the variables (except any keywords/reserved words in Python like `if`, `break`, `for`). For example, in this program, `number1`, `number2`, `add_result` are variables that store values.

You can read/practice more based on Lecture 2 slides.


### Write a program

Write a program that takes as input the radius of a circle and computes the circumference of the circle using the formula:

$$
circumference = 2 \pi r
$$

* Where $\pi$ is 3.14159


Please display the circumference using a `print` statement.

Save the program is `circle.py` and attach it to the Blackboard lab assignment. 


#### Grading Rubric for the program:

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

**TOTAL	25 points**




---