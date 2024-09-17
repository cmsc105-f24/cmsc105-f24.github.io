---
layout: default
permalink: module/7
---

# Module 7: Build Automation with Make

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 7 assignment.

**Note:** Create a text file called `module7.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Evaluate Boolean (pronounced: BOO-lee-unn) expressions.
* Construct Boolean expressions from English descriptions.
* Mentally execute (trace) code with conditionals: that is: if, if-else, and if-multi-else statements.
* Write and debug code with conditionals.
* Identify new syntactic elements related to the above.


## A simple example

Consider this program:

```python
x = 5
y = 4

if x > y:
    print('Hey, x is bigger')

print("OK, we're done")
```    
 
--- 
**Exercise: 1** In `my_ifexample.py`, type up the above and examine the output. Then, just below the `print` with `'Hey'` (_and indented 4 spaces_) add another `print` to print anything. Then, change the value of `y` to `6` and report the output in `module7.txt`. Submit the program with these modifications.

---

Let's explain:

* First, observe:

  ```python
  x = 5
  y = 4

  # The reserved word "if"
  # The "x > y" is called the condition
  if x > y:
      # The body of the if statement is indented
      print('Hey, x is bigger') 

  # The rest of the program's code 
  # follows with previous indent level
  print("OK, we're done")
  ```

* Now, at the moment the if-statement executes, the condition is evaluated:

  ```python
  x = 5
  y = 4

  # x has 5, y has 4. Thus at the moment, x > y
  # so the condition evaluates to True
  if x > y:
      # Because the condition evaluates to True, 
      # the code in the body-of-the-if executes
      print('Hey, x is bigger') 

  # After the if-body executes,
  # execution continues here
  print("OK, we're done")
  ```

If the condition is `True` then the code that's indented below the if-statement executes.

* Consider what happens when `y` is `6`:

  ```python
  x = 5
  y = 6

  # x has 5, y has 6. Thus at the moment, x > y is False
  if x > y:
      # Because the condition evaluates to False, 
      # execution skips past the if-body
      print('Hey, x is bigger') 

  # Since the condition evaluates as False,
  # execution goes here
  print("OK, we're done")
  ```

--- 
**Exercise: 2** Consider this program:

```python
s = 7

s = s + 9

if s < 15:
    print('Less than 15')

print('Done')

```

Try to mentally execute (trace its execution in your mind) and predict the output before typing it up in `my_ifexample2.py` to confirm.

---

## if-else

Think of else as if's occasional partner.

Consider this example:

```python
x = 5
y = 4

if x > y:
    print('Hey, x is bigger')
else:
    print('Who said x is bigger?')
    print('In fact, y is bigger')

print("OK, we're done")
```    
 

--- 
**Exercise 3:** Type up the above in `my_ifexample3.py` and examine the output. Then, change the value of `y` to `6`. What is the output? Change `y` to `5`. What is the output? Report these in your `module7.txt` file.
 
--- 

Let's point out:

* When `x` is indeed larger than `y`, the code in the if-body executes:

  ```python
  x = 5
  y = 4

  # x has 5, y has 4. Thus at the 
  # moment, x > y is True
  if x > y:
      # Because the condition evaluates to True,
      # execution enters the if-body
      print('Hey, x is bigger')
  else:
      print('Who said x is bigger?')
      print('In fact, y is bigger')

  # After the if-body code completes,
  # execution skips past the else-body
  print("OK, we're done")
  ``` 

* When the if-condition evaluates to False:

  ```python
  x = 5
  y = 6

  # x has 5, y has 6. Thus at the 
  # moment, x > y is False
  if x > y:
      print('Hey, x is bigger')
  else:
      # Because the condition evaluates to False,
      # execution enters the else-body
      print('Who said x is bigger?')
      print('In fact, y is bigger')

  # After the else-body code completes,
  # execution continues here
  print("OK, we're done")
  ``` 

* What happens when `x` is `5` **and** `y` is `5`?

  ```python
  x = 5
  y = 5

  # x has 5, y has 5. 
  # 5 is NOT greater than 5, so x > y is False
  if x > y:
      print('Hey, x is bigger')
  else:
      # Because the condition evaluates to False,
      # execution enters the else-body
      print('Who said x is bigger?')
      print('In fact, y is bigger')

  # After the else-body code completes,
  # execution continues here
  print("OK, we're done")
  ``` 

 ## if-elif-else

Consider this variation:

```python
x = 5
y = 5

if x > y:
    print('Hey, x is bigger')
elif y > x:
    print('Who said x is bigger?')
    print('In fact, y is bigger')
else:
    print('Actually, they are equal')

print("OK, we're done")

```   
 
--- 
**Exercise 4:** Type up the above in `my_ifexample4.py` and examine the output. Then, try `y = 6` and `y = 4`. Report results in your `module7.txt`.
 
--- 

Let's explain:

* First, consider the case `x = 5`, `y = 5`:

  ```python
  x = 5
  y = 5

  # x has 5, y has 5. 
  # 5 is NOT greater than 5, so x > y is False
  if x > y:
      print('Hey, x is bigger')   
  elif y > x: # In this case y > x is False
      print('Who said x is bigger?')
      print('In fact, y is bigger')
  else: 
      # So the execution continues to the else clause
      print('Actually, they are equal')

  print("OK, we're done")

  ``` 

  * Now consider `x = 5`, `y = 4`:

  ```python
  x = 5
  y = 4

  # x has 5, y has 4, so x > y is True 
  if x > y:
      print('Hey, x is bigger') 
      # After the if block of code executes, 
      # execution skips past the else block  
  elif y > x: 
      print('Who said x is bigger?')
      print('In fact, y is bigger')
  else: 
      print('Actually, they are equal')

  # After the if block, execution continues here
  print("OK, we're done")

  ```   

* Next `x = 5`, `y = 6`:

  ```python
  x = 5
  y = 6

  # x > y is False so execution tries the next condition
  # which is the elif part 
  if x > y:
      print('Hey, x is bigger')  
  elif y > x: 
      # In this case y > x is True,  
      # so the code in the elif block will execute
      print('Who said x is bigger?')
      print('In fact, y is bigger')
  else: 
      print('Actually, they are equal')

  # After the elif block, execution continues here
  print("OK, we're done")

  ``` 

One can have as many elif sections as one would like, for example:

```python
x = 3

if x == 1:
    print('one')
elif x == 2:
    print('two')
elif x == 3:
    print('three')
elif x == 4:
    print('four')
else:
    print('big')
```
    
Think of the whole thing as a giant if-statement:

```python
x = 3

# This if statement has an if, three elif's, and one else
# Execution of the if begins with the if condition.
if x == 1:
    print('one')
elif x == 2:
    print('two')
elif x == 3:
    print('three')
elif x == 4:
    print('four')
else:
    print('big')


# After navigating a path through the various parts of the giant
# if-statement, execution continues here    
```


In the above case, when `x` is `3`, the execution path through the giant if-statement is:

```python
x = 3

if x == 1:
    print('one')
elif x == 2:
    print('two')
elif x == 3: # This second elif succeeds
    print('three')
elif x == 4:
    print('four')
else:
    print('big')


# After the 2nd elif block, execution continues after the else    
```

--- 
**Exercise 5:** Type up the above in `my_ifexample5.py`. Then, try each of `x = 1`, `x = 2`, `x = 4`, `x = 5`. Explain the execution pathways (similar to the examples above) for each case in your `module7.txt`.
 
---


Consider this program:

```python
x = 5
y = 4
z = 3

if x > y:
    print('Hey, x is bigger')

if x > z:
    print('x is bigger than z')
    print('So, x must be the largest')
```

--- 
**Exercise 6:** Type up the above in `my_ifexample6.py`. Try `y = 6`. Explain why it does not work. Then try to alter the program without changing the print-statements so that it works in all cases for possible values of `x`, `y`, and `z`. That is, whichever of the above print-statements gets printed correctly reflects the values of `x`, `y` and `z`.

---


## Nested conditionals

Consider this program:

```python
a = 3
b = 4
c = 5

if a < b:
    if a < c:
        print('a is the smallest')
    else:
        print('a is not the smallest')

print('Done')

```
   
This is an example of a nested conditional (nested if):
* First, examine the indented structure:
  ```python
  a = 3
  b = 4
  c = 5

  # The condition used by the outer if statement
  if a < b:
      # The block of code that executes 
      # when outer if evaluates to True
      if a < c:
          print('a is the smallest')
      else:
          print('a is not the smallest')

  print('Done')

  ```

* The flow of execution:  
  ```python
  a = 3
  b = 4
  c = 5

  # When the outer condition is evaluated,
  # it evaluates to True
  if a < b:
      # Then the inner condition is evaluated
      # (it evaluates to True)
      if a < c:
          print('a is the smallest')
      else:
          print('a is not the smallest')

  # After the inner if block,
  # execution continues here 
  print('Done')

  ```


Consider this variation:

```python
a = 3
b = 4
c = 5

if a < b:
    if a < c:
        print('a is the smallest')
    else:
        print('a is not the smallest')
    print('We know a is less than b')
else:
    print('We know a is not less than b')

print('Done')
```


--- 
**Exercise 7:** Type up the above in `my_nestedif.py`. Trace the flow of execution for the following three cases: (1) when `a = 3`, `b = 4`, `c = 5`; (2) when `a = 3`, `b = 4`, `c = 2`; (3) when `a = 6`, `b = 4`, `c = 5`.

---
 

**Exercise 8:** In `my_smallest_of_three.py`, modify the above program so that it prints out, appropriately, one of "a is the smallest", "b is the smallest" or "c is the smallest", depending on the actual values of a, b, and c. Try different values of these variables to make sure your program is working correctly.

---


**Note:**

* A numeric variable can be: strictly less, less than or equal to, strictly greater, greater than or equal to, or equal to another variable.
* Accordingly, the different types of less/greater comparisons are:
  ```python
  a < b      # Strictly less than, as when a = 3, b = 4
  a <= b     # Could be less (a = 3, b = 5), could be equal (a = 3, b = 3) 
  a > b      # Strictly greater (a = 3, b = 2)
  a >= b     # Could be greater (a = 3, b = 1), could be equal (a = 2, b = 2)
  ```


## Combining conditions

Consider this program:

```python
x = 5
y = 5
z = 5

if x == y and y == z:
    print('All three are equal')

```

**Note:**
* The first thing to point out is the `==` operator:
  * Because we've been using the equals operator for assigning values to variables, we need something else to test for equality.
  * The equality operator in Python is `==` as in:
    ```python
    if x == y and y == z:
    ```  
  * Alas, the problems with limited keyboard symbols!

* **Important:** the difference between `=` and `==` is very important to remember. It's easy to make a mistake one forgets.

* The if-statement combines two conditions:
  ```python
  if x == y and y == z:
  ```
  
* The combining occurs with the Boolean operator and:
  ```python
  if x == y and y == z:
  ```

* We can clarify the parts and combination thereof using parens:
  ```python
  if (x == y) and (y == z):
  ```

* The two parts are often called clauses:
  * First clause (x == y):
    ```python
    if (x == y) and (y == z):
    ```  
  * Second clause (y == z):
    ```python
    if (x == y) and (y == z):
    ```  
  * You could have many more clauses.

* The `and` operator works like this:
  ```python
  # BOTH need to be True for the if-block to execute
  if (x == y) and (y == z):
  ```

* Boolean is pronounced "BOO lee unn".
* A Boolean operator takes expressions and computes to either `True` or `False`.
 
Let's go back to finding the smallest of three numbers using conditionals:

```python
a = 3
b = 4
c = 5

# Fill in code here ... 
``` 

---
**Exercise 9:** In `my_smallest_of_three2.py`, fill in code to identify which of the three variables has the smallest value, depending on the actual values of `a`, `b`, and `c`. Use if-statements with multiple clauses. Try different values of these variables to make sure your program is working correctly.

---


As the counterpart to the and operator, there is the `or` operator:

```python
a = -2.718

if (a <= 0) or (a >= 1):
    print('a is not between 0 and 1')

```
 
---  
**Exercise 10:** Type up the above in my_boolean2.py. Then try `a = 0.5`.
 
--- 

**Note:**

* We have shown how to write "less than or equal to" using `<=`.
* So, now we can add "equals" and "not equals" to the numeric comparisons:
  ```python
  a < b      # Strictly less than, like a = 3 < b = 4
  a <= b     # Could be less, could be equal (a = 3, b = 3)
  a > b      # Strictly greater (a = 3, b = 2)
  a >= b     # Could be greater, could be equal 
  a == b     # Exactly equal
  a != b     # Not equal
  ```

* For the `or` operator to evaluate to `True`, any one or both of the two expressions needs to be `True`.

* Consider:
  ```python
  a = 3
  b = 4
  if (a < 10) or (b < 10):
      print('One or both of them is less than 10')
  ```
  
  * In this case both will evaluate to `True`, and so the `print` statement executes.
  * Suppose we made `a = 3`, `b = 11`, the `print` statement will execute.
  * Suppose we change `a = 11`, `b = 3`, the `print` statement will execute.
  * But if `a = 11`, `b = 12`, the `or` fails (both clauses are `False`), and the `print` won't execute.
* Incidentally, let's replace or with and in the above case, and see what we get:
  ```python
  a = 3
  b = 4
  if (a < 10) and (b < 10):
      print('Both of them are less than 10')
  ```
  
In this case, both sub-conditions are satisfied, and so the whole if-condition is satisfied, which means the print will execute.

* But if we had
  ```python
  a = 3
  b = 4
  if (a < 10) and (b > 10):
      print('Both of them are less than 10')
  ```
  
In this case, the second comparison fails, and the `print` won't occur.

* Whereas if we had `or`:
  ```python
  a = 3
  b = 4
  if (a < 10) or (b > 10):
      print('One or both of them is less than 10')
  ```

* Here, it's enough that `a` is less than `3`, and so the `print` executes even though "b greater than 10" fails.
 
Next, let's look at the NOT operator (written with `!`):

```python
x = 5
y = 6
z = 7

if (x != y) and (x != z):
    print('x is different from y and from z')
```

Here, read `!=` as "not equals".
 
--- 
`Exercise 11:` Type up the above in `my_boolean3.py`, then change `z` to be `6` (same as `y`). What do you observe?
 
--- 


One can combine any number of and's, for example:

x = 5
y = 6
z = 7

if (x != y) and (x != z) and (y != z):
    print('x, y, z are all different')
  
 
The difference between != and not:

We should read != as "not equals" just as we read == as "equals".
There is another operator called not, which applies to Boolean expressions, as we'll see next.
 
The not operator

One can apply the not operator to groups of clauses using additional parens:
x = 8

if not ( (x == 5) or (x == 6) ):
    print('x is neither 5 nor 6')
  
Here, not is asking that whatever it applies to be false.
Thus, consider the expression
if not ( (x == 5) or (x == 6) ):
  
In this case, x is 8. So, neither of (x == 5) nor (x == 6) is true.
Thus, the whole expression ( (x == 5) or (x ==6) ) is false.
Which means not ( (x == 5) or (x ==6) ) evaluates to true.
Therefore, the print executes.
 
1.15 Exercise: Suppose integer variables a,b,c,d,e have values a=1, b=1, c=3, d=4, e=5. Consider the following three expressions:

	( (a <= b) and (c+d > e) and (d > 1) )

        ( (a > c) or ( (c+1 < e) and (c-b > a) ) )

        not ( (b == d-c) and (a > b) or (c < d) )
  
Try to evaluate each expression by hand. Then, in my_boolean4.py, write up each of these in an if-statement to see if the result matches with your hand-evaluation.
 
1.16 Exercise: In my_boolean5.py, write a program that begins with

a = -3
b = -4
  
and uses conditionals to print out the absolute difference between the two numbers. In the above case, the difference is 1. In the case of a=3, b=4, the difference is also 1. When a=-3, b=4, the difference is 7.
 