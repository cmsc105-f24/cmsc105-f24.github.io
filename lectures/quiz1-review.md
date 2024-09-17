---
layout: default
permalink: /lecture/q1
---

# Quiz 1 review 

## Background 
The quiz will be based on the topics covered in weeks 1 through 3. There are 3 sections — short answer questions, tracing, and a programming problem. Students are allowed to use the Thonny IDE for __Section III only__. Please see the grading rubric for the programming problem. Scratch paper and a simple calculator are allowed.


## Section I (20 points)
		
**1** Show the output of the following:
```python
import math
print(math.floor(9.6))
```

**2** Show the output of the following:
```python
print(abs(-14.2))
```

**3** Show the output of the following:
```python
print(round(5.78437234, 2))
```

**4** Show the output of the following:
```python
import math
print(math.pow(4, 2))
```

**5** Show the output of the following:
```python
import math
print(math.sqrt(36))
```

**6** What will be the output of the following:
```python
string_val = "Python Programming"
result = string_val.find('m')
print(result)
```

**7** What will be the output of the following:
```python
string_val = "Python Programming"
result = string_val.lower()
print(result)
```

**8** What will be the output of the following:
```python
string_val = "Python Programming"
result = string_val * 3
print(result)
```

**9** What will be the output of the following:
```python
string_val = "Python Programming"
result = string_val[3:8]
print(result)
```

**10** What will be the output of the following:
```python
string_val = "Python Programming"
result = string_val[:-4]
print(result)
```



## Section II (30 points)

Trace the execution of the following program by filling in a tracing table. You can draw the tracing table on a piece of paper and include an image file (`tracing.png`) on Blackboard. 

You may use the following guide for reference: 
* [Tracing Worksheet](/guides/tracing)

**Note:**  Assume that the user enters `20` for the height.
```python
import math

# Constants
g = 9.81  # Acceleration due to gravity (m/s^2)

# Read the height from which the object is dropped from the user
height = float(input("Enter the height dropped (in meters): "))

# Calculate the time it takes to hit the ground using the formula t = sqrt(2h/g)
time_to_hit_ground = math.sqrt(2 * height / g)

# Print the time to hit the ground
print("Time to hit the ground is", round(time_to_hit_ground), "seconds.")


```


## Section III (50 points)


Programming question:
* You can use the Thonny Python IDE for writing the program.
* You can draw the flowchart on a piece of paper and include an image file (`flowchart.png`) on Blackboard.

You may use the following guide for reference: 
* [Flowchart Guide](/guides/flowchart)


<br />

Create a program that reads in the $radius$ and $length$ of a cylinder and computes the $area$ and $volume$ using the following formulas:

$$
area = radius * radius * \pi
$$

$$
volume = area * length
$$

* Where $\pi$ is 3.14159

Please print the $area$ and $volume$ values. 

* First, draw a flowchart of the program.

* Next, write the code for the program. Save the program as `cylinder.py` and attach it to Blackboard.

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
