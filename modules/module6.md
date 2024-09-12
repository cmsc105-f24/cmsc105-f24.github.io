---
layout: default
permalink: module/6
---

# Module 6: Real Numbers

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 6 assignment.

**Note:** Create a text file called `module6.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Create variable declarations for variables.
* Assign values to variables by simple assignment, and print them out.
* Demonstrate ability to perform operations for a desired output.
* Evaluate expressions with variables in them.
* Convert English descriptions of operations into expressions.
* Mentally trace execution with expressions and calculations.



## What are real numbers?

Let's start with some math facts:

* Whole numbers like 3, 42 and 1024 are integers. (As an aside: integers include 0 and the negative ones like -2 or -219).
* The collection of all integers is infinite in size.
* But integers are limited because some operations on integers do not yield integers:
    * 30 ÷ 5 gives 6, which is an integer.
    * But 31 ÷ 5 is not an integer, yet it's a quantity.
* Real numbers include all the integers but also numbers like 3.141, and -615.2368.
* The collection of all real numbers is also infinite.
* The term real is just that: a term that's came about historically to describe all these numbers.
* You might wonder: is there any other kind of number?
* What does one do with real numbers?
    * The same operations: +, -, *, /
    * What's nice is that applying these to real numbers will always result in real number results.
* For example:
    ```python
    x = 3.14
    y = 2.718
    z = x + y
    print(z)

    w = z * (x + y) / (x - y)
    print(w)
    ```

--- 
**Exercise 1:** Type up the above in `my_real_example1.py`. What is the output?

---

**Note:**
* You might have seen 5.8580000000000005 as the value of z printed out.
* However, you might also have seen something slightly different because of the approximate nature of such calculations, a limitation of computer hardware.
* These tiny errors are tiny indeed, but vary slightly from one computer to another, generally occurring around the 16th decimal place: 0.00000000000000001
* Do we need to worry about this? Only if we are engaged in complex scientific calculations.
* Occasionally, however, it can matter. For example, if two people calculate mortgage interest (with real consequences) slightly differently, it could lead to a legal conflict.

Quick review of some relevant math:

* One kind of operation that's useful is power.
* We write $2^6$ to mean $2×2×2×2×2×2$ (six times)
* It's easy to see that you could make this work for real numbers that get multiplied: $2.56^6 = 2.56 × 2.56 × 2.56 × 2.56 × 2.56 × 2.56$
* But could you do $2^{6.4}$ ? Turns out, yes, you can do this even if it's not easy to see or intuit.
(We would expect $2^{6.4}$
 to be larger than $2^6$
 and smaller than $2^7$, which it is.)

* The next step then is to allow numbers like $2.56^{6.4}$
* In fact, you can take any real number as the mantissa (the $2.56$ in $2.56^{6.4}$) and any real number as the exponent (the $6.4$ in $2.56^{6.4}$).
* Let's put this in code and introduce a new operator to raise a number to a power, as in $2.56^{6.4}$).

    ```python
    x = 2 ** 6
    print(x)

    y = 2.56 ** 6.4
    print(y)
    ```

---
**Exercise 2:** Type up the above in `my_real_example2.py`. What is the output? Consider $2.56x = y$. Can you guess what approximate value of $x$ would make $y$ become $400$ ?  Play around with the number `6.4` in the program above and see if you can guess approximately what value would make `y` become `400`.

---


Let's explore further:

* The technical term for "what is x that would make $2.56x=400$ ?" is _logarithm_.
* We would say: $x=log_{2.56}(400)$
* Read this as: x is equal to log of $400$ to the base $2.56$.
* We can calculate this directly:
    ```python
    import math

    x = math.log(400, 2.56)
    print(x)
    ```

* Here we've introduced some new concepts:

```python
# To use math functions, we apply the import statement
# to access these functions.
import math

# To use a particular math function like logarithm, 
# use math with the period and the name of the function.
# (in this case: log)
x = math.log(400, 2.56)

print(x)
```


* Just like you can ask Python to calculate logarithms using `math.log`, you can do other kinds of "calculator" functions conveniently.
* Example: `math.sqrt` for square roots.
 
--- 
**Exercise 3:*** In `my_real_example3.py`, fill in code below to compute the square root of 2 and `print` the square root (and only the square root - just one number).

```python
import math

# Write a line of code here

print(x)
```

---


##  Going from reals to integers and strings

Consider this program:

```python
import math

x = 3.141
print('x=' + str(x))

i = math.floor(x)
j = math.ceil(x)
print('Rounding down x gives ' + str(i))
print('Rounding up x gives ' + str(j))
```

**Note:**
* The `floor` function identifies the integer part of a number like 3.141, in this case 3.
* `ceil` identifies the next higher integer, in this case 4.
* So, any number with digits after the decimal point like 3.141 lies between its _floor_ and _ceiling_.

---
**Exercise 4:** Type the above in `my_real_example4.py`. Then, add additional lines of code to print the floor and ceiling of 2.718 in the same way that the floor and ceiling of 3.141 were printed above.

---


Let's point out a few things:

```python
import math

x = 3.141
print('x=' + str(x))

# Notice the "math." part of the math.floor function.
# Notice there are no spaces between math. and the floor function.
i = math.floor(x)
j = math.ceil(x)

# The str function converts the number given to it into a string.
# In this case that string is used to concatenate into a larger
# string that gets printed.
print('Rounding down x gives ' + str(i))
print('Rounding up x gives ' + str(j))

```

Next, getting real numbers as input:

```python
import math

# input always results in a string
x_str = input('Enter a number: ')

# This is how we convert a string into a real number:
x = float(x_str)

# We use str to embed a number in a string:
print('The square of the number you entered is: ' + str(x*x))
```

**Note:**

* Recall: we use the `int()` function to convert a string representation of an integer into an actual integer ready for arithmetic, as in:
    ```python
    pounds_str = input('Desired flour in pounds: ')
    pounds = int(pounds_str)
    ounces = 16 * pounds
    print('Flour amount in ounces: ' + ounces)
    ```
  
* The equivalent for real numbers is `float()`:
    ```python
    x = float(x_str)
    ```
  
* Why is it called so?
    * Observe that we can write the number $234.56$ as $23.456×10^1$ or as $2.3456×10^2$ or as $0.23456×10^3$, or to exaggerate this idea: $0.000000000023456×10^13$
    * The decimal point can thus, be "floated" around by adjusting the exponent (like 13).
    * This is called _floating-point_ notation.

* So, what does it mean to have a string representation of a number versus the actual number?
    * First, consider this program:
        ```python    
        some_string = '3.141'
        x = float(some_string)
        # Now we can use x in arithmetic
        y = x / 2
        ```
  
* We cannot use `some_string` in arithmetic.
The following does NOT work:
    ```python
    x = '3.141'
    y = x / 2
    print(y)
    ```
  
--- 
**Exercise 5:** What is the error in the above program? Now change the second statement from `y = x / 2` to `y = x * 2`. What do you see? Write your code in `my_real_example5.py`. Submit the version with `y = x / 2` but describe both cases in your `module6.txt`.

--- 


The last exercise illustrates the strange way in which operators like + and * are repurposed for strings when used with strings:

* Consider this example:

    ```python
    s = 'Hello'
    t = ' World'
    u = s + t
    print(u)
    v = s * 3   # Makes 3 copies of s and concatenates them
    print(v)    # Prints HelloHelloHello
    ```  
 
--- 
***Exercise 6:** Type up the above in `my_string_example.py` and confirm.

---

