---
layout: default
permalink: quiz/1
---

# Quiz 1

__Points Possible:__ 100

__Date:__ Thursday, September 19th 


## Background 
This quiz is based on the topics covered in weeks 1 through 3. There are 3 sections — short answer questions, tracing, and a programming problem. Students are allowed to use the Thonny IDE for __Section III only__. Please see the grading rubric for the programming problem. Scratch paper and a simple calculator are allowed.

## Submission
* Submit a `quiz1.txt` file on Blackboard with your answers.
* Submit any Python code from the Thonny IDE on Blackboard.


## Section I (20 points)

			
**1** Show the output of the following:
```python
import math
print(math.ceil(-9.6))
```

**2** Show the output of the following:
```python
print(abs(-7.2))
```

**3** Show the output of the following:
```python
print(round(5.7))
```

**4** Show the output of the following:
```python
import math
print(math.pow(2, 3))
```

**5** Show the output of the following:
```python
import math
print(math.sqrt(25))
```

**6** What will be the output of the following:
```python
string_val = "Python programming"
result = string_val.find('t')
print(result)
```

**7** What will be the output of the following:
```python
string_val = "Python programming"
result = string_val.upper()
print(result)
```

**8** What will be the output of the following:
```python
string_val = "Python programming"
result = string_val * 5
print(result)
```

**9** What will be the output of the following:
```python
string_val = "Python programming"
result = string_val[:-1]
print(result)
```

**10** What will be the output of the following:
```python
string_val = "Python programming"
result = string_val[1:3]
print(result)
```



## Section II (30 points)

Trace the execution of the following program by filling in a tracing table. You can draw the tracing table on a piece of paper and include an image file (`tracing.png`) on Blackboard. 

You may use the following guide for reference: 
* [Tracing Worksheet](/guides/tracing)

**Note:**  Assume that the user enters `3` for the _first_ number and `7` for the _second_ number.
```python
# Simple Calculator

# Get input from the user
num1 = eval(input("Enter the first number: "))
num2 = eval(input("Enter the second number: "))

# Perform arithmetic operations
sum = num1 + num2
diff = num1 - num2
product = num1 * num2

# Display the results
print("The sum is", sum)
print("The difference is", diff)
print("The product is", product)

```


## Section III (50 points)


Programming question:
* You can use the Thonny Python IDE for writing the program.
* You can draw the flowchart on a piece of paper and include an image file (`flowchart.png`) on Blackboard.

You may use the following guide for reference: 
* [Flowchart Guide](/guides/flowchart)


<br />

Create a program that takes as input three numbers: num1, num2, num3 and displays the average of the three numbers as an integer by rounding off the average. 

Sample run:

```
Enter number 1: 34
Enter number 2: 30
Enter number 3: 25
The average of 34, 30, and 25 is 30
```


* First, draw a flowchart of the program.

* Next, write the code for the program. Save the program as `average.py` and attach it to Blackboard.

### Grading Rubric for Section III:

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
        <td>10</td>
    </tr>
    <tr>
        <td>Flowchart</td>
        <td>15</td>
    </tr>
    <tr>
        <td>Computation</td>
        <td>10</td>
    </tr>
    <tr>
        <td>Print output</td>
        <td>10</td>
    </tr>
</table>



