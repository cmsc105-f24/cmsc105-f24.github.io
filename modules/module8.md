---
layout: default
permalink: module/8
---

# Module 8: Loops: the `for` loop

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 8 assignment.

**Note:** Create a text file called `module8.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Identify the new syntactic elements with the basic output-only `for` loop.
* Demonstrate ability to mentally trace execution of `for` loops.
* Produce desired output using `for` loop and `print`'s.
* Distinguish between count-up and count-down loops.
* Use some nested `for` loops with independent variables.
* Use some nested `for` loops with dependent conditions.
* Identify and correct syntax errors related to above objectives.
* Distinguish between syntax errors and debugging.

## An example

```python
for i in range(6):
    print(i)
```

--- 
**Exercise 1:** Type up the above in `my_forloop_example.py` and run it. You should observe this:

```
0
1
2
3
4
5
```

In the place in the code where you see the number `6`, replace 6 with `10` and then run the program. Next, try `2` instead of `6`. Finally, try `0` instead of `6`. What is the output in each case? Report in your module text file (`module8.txt`). Submit the program with `6`.

--- 

Let's now examine elements of the loop:

* There's the special word `for`:
    ```python
    for i in range(6):
        print(i)
    ```
* Then, there's the for-loop variable `i`:
    ```python
    # The loop variable i is defined here
    for i in range(6):
        print(i) # and also used here
    ```
* The special word `in`:
    ```python
    # Notice the in keyword between the i and range.
    for i in range(6):
        print(i) 
    ```
* The element that controls the spread of different values that variable `i` takes on at each iteration of the loop: `in`:
    ```python
    # The number 6 in the range 
    # implies the values 0, 1, 2, 3, 4, 5.
    for i in range(6):
        print(i) 
    ```
* Finally, the block of code (in this case, just one line) that's called the body of the loop:
    ```python
    for i in range(6):
        # The body of the for-loop
        print(i) 
    ```

Let's change the program slightly and then set about explaining how the loop works:

```python
for i in range(6):
    print(i)
    print('Hello')
```

--- 
**Exercise 2:** Type up the above in `my_forloop_example2.py` and run the program.

---

Observe that the body of this for-loop has two statements:

```python
for i in range(6):
    print(i)           # Body line 1
    print('Hello')     # Body line 2
```


Let's now use a slightly fictionalized way to explain the action of this loop:

* Think of the Python part of your computer (since your laptop does many things) as reading your program and then carrying out the instructions.
* When it encounters the for word, it says "Ah, here's a for-loop".
* Then it sees the variable `i` and says (to itself), "This is the variable whose value will change after each iteration".
* Then it sees the term `range(6)` and says "Oh, I will start at `0` and end just before `6`, which means it will be `0` in the first iteration, `1` in the second, `2` in the third, `3` in the fourth, `4` in the fifth, `5` in the last".
* Then, it starts executing the body of the loop for the first iteration:
    * For the first iteration, `i = 0`.
    * The entire body of the loop executes with `i` being replaced by `0`:
    ```python
    for i in range(6):
        print(i) # First iteration: i has the value 0
        print('Hello')     

    # During the first iteration: 
    # 0 is printed, followed by Hello
    ```

* For the second iteration, `i = 1`
    ```python
    for i in range(6):
        print(i) # First iteration: i has the value 1
        print('Hello')   

    # During the first iteration: 
    # 1 is printed, followed by Hello  
    ```

* Third iteration:
    ```python
    for i in range(6):
        print(i) # First iteration: i has the value 2
        print('Hello')   

    # During the first iteration: 
    # 2 is printed, followed by Hello  
    ```

* Fourth iteration:
    ```python
    for i in range(6):
        print(i) # First iteration: i has the value 3
        print('Hello')   

    # During the first iteration: 
    # 3 is printed, followed by Hello  
    ```

* Fifth iteration:
    ```python
    for i in range(6):
        print(i) # First iteration: i has the value 4
        print('Hello')   

    # During the first iteration: 
    # 4 is printed, followed by Hello  
    ```

* Sixth and final iteration:
    ```python
    for i in range(6):
        print(i) # First iteration: i has the value 5
        print('Hello')   

    # During the first iteration: 
    # 5 is printed, followed by Hello  
    ```

* Now the for-loop is done and the execution goes past the whole for-loop to whatever's there.
    * In this case, there's no other code and the program completes.


## Variations

To explore for-loops further, we'll look at some variations of the basic for-loop:

* First, we could have named our for-loop variable
    ```python
    for count in range(6):
        print(count)
    ```    
    **Note:** it's customary to use short variable names like `i` and `j`.

* To go through a loop five times, any range of numbers will do:
    ```python
    for i in range(10, 16):
        print(i)
    ```    
    **Note:** Here, the range feature has both a starting value (10) and just-after-ending value (16) specified.
    This will print the numbers 10 through 15.

* We don't have to increment the for-loop variable by 1.
    ```python
    for i in range(10, 16, 2):
        print(i)
    ```    

    * This prints the numbers 10, 12, 14.
    * The number 2 in range(10, 16, 2) specifies an increment amount.
    * Thus, we start with `i` taking the value 10 in the first iteration.
    * In the second iteration, `i` becomes 12 (because 10+2 = 12).
    * In the third iteration, `i` becomes 14 (incrementing 12 by 2).
    * If we were to increment 14 by 2 it becomes 16 which is past * the last value allowed.
    * **Important:** think of 16 as "the variable cannot have this value or anything past this value".
* We can decrement, as in:
    ```python
    for i in range(16, 10, -1):
        print(i)
    ```
    * This will print 16, 15, 14, 13, 12, 11.
    * We start with 16 (the first part of the range).
    * After each iteration we apply the increment/decrement amount.
    * In this case, applying -1 to 16 gives us 15, which gets printed.
    * Then, the third time through, `i` becomes 14. And so on.
    * In the last iteration, `i` becomes 11.
    * Finally, when `i` is decremented to 10, the loop is ended.
 
 ---
 **Exercise 3:** Type up the above four examples in `my_forloop_variation1.py`, `my_forloop_variation2.py`, `my_forloop_variation3.py`, and `my_forloop_variation4.py`. Run to confirm the output.

 ---
 

**Exercise 4:** In `count_odd_up.py`, write a loop to print the odd numbers from 1 to 25 (thus, skipping by 2, and including 1 and 25 in the output).

---

**Exercise 5:** In `count_even_down.py`, write a loop to print the even numbers from 24 down to 2 (inclusive of 24 and 2).

---

## Nested for-loops

We'll start by writing a program to print a little number triangle like this:

```
1
22
333
4444
```

Notice: there's repetition across a row of numbers: a potential use of for-loops!

We'll do this in stages, starting with this program:
```python
print(1)               # print 1 all by itself

for i in range(2):     # i will start at 0, go up to 1
    print(2, end='')
print()                # Print nothing but go to the next line.

for i in range(3):     # i ranges from 0 to 2
    print(3, end='')
print()

for i in range(4):     # i ranges from 0 to 3
    print(4, end='')
print()
```
    
Observe:

* We've used `end=''` (two single quotes in succession) to avoid printing each number on a single line.
* One could use two double quotes in succession as well.
* `print()` merely goes to the next line (Or, stated differently, ends the current line being printed.)
 
--- 
**Exercise 6:** Add a row for 5 (with five of them), writing your code in `my_forloop_print.py`

---
 

**Exercise 7:** Just for the heck of it, could one use a for-loop to achieve the printing of 1 all by itself? That is, answer the question in your `module8.txt`: can a for-loop be set up so that you go into it exactly once? Write your code in `my_forloop_print2.py`

---
 

Next, observe that the upper-limits of the for-loops are themselves _increasing_:

```python
print(1)               

for i in range(2):   # first loop has limit 2
    print(2, end='')
print()                

for i in range(3):   # second loop has limit 3
    print(3, end='')
print()

for i in range(4):   # third loop has limit 4
    print(4, end='')
print()
```

Also, observe that the very thing we're printing across a row is the loop limit itself:

```python
print(1)               

for i in range(2):   
    print(2, end='')   # print limit 2
print()                

for i in range(3):   
    print(3, end='')   # print limit 3
print()

for i in range(4):   
    print(4, end='')   # print limit 4
print()
```

Another way to say this:
1. **When the value is 2, print a row of two 2's**
2. **When the value is 3, print a row of three 3's**
3. **When the value is 4, print a row of four 4's**
  
Thus, we could try to do is:
```python
for j in range(2, 5):   # let j iterate from 2 to 4
    # print j occurrences of j using a loop
```  

But we already know how to print a row of `j`'s:
```python
for j in range(2, 5):   # let j iterate from 2 to 4
    # print a row of j's (j of them)
    for i in range (j):
        print(j, end='')
```

Let's put this together in a complete program:

```python
print(1)                   # print 1 all by itself

for j in range(2, 5):      # j iterates from 2 to 4
    for i in range(j):     # for each j, print j of them
        print(j, end='')
    print()    
```

---
**Exercise 8:** Change the program to print a fifth row with five 5's. Also adjust the for-loop so that the for-loop also takes care of printing the sole 1 that appears in the row of the sole 1's. That is, adjust the for-loop conditions so that you don't need the stand-alone `print(1)` to print 1. Write your code in `my_forloop_print3.py`

---

Let's review what we learned above:

* The _outer_ loop variable's value is used in the _inner_ loop:
    ```python
    print(1)                 

    # The outer loop variable j is used in 
    # setting the limit of the inner loop
    for j in range(2, 5):      
        for i in range(j):    
            print(j, end='')  # and in what gets printed
        print()    
    ```

* Consider a single iteration of the outer-loop (e.g., when `j` is `3`).  
    ```python
    print(1)                 

    for j in range(2, 5):    
        # Suppose j is 3 (2nd iteration of the outer loop)  
        for i in range(j):    # So this j now has value 3. Which means the inner loop runs 0 to 2.
            print(j, end='')  # j has value 3 at this moment. Which means j gets printed
        print()  # When the inner loop ends, this  goes to the next line  
    ```
    * For this value of `j`, the inner loop executes `j` times.
    * Thus, when `j` is `3`, the inner loop has 3 iterations.
* This is an example of a _nested for-loop_ in which the inner loop's execution _depends_ on the value of the outer-loop variable.
* Another way to say it: a _nested for-loop_ has one for-loop inside another.
* We will use _nesting_ in other contexts as well, when one structure is placed inside another.


## Tracing through a program in detail
 
We'll now look at an example of how to execute a program "by hand". That is, how to trace a program's execution by painstakingly following its execution step-by-step.

At first this will appear tedious, but it is critical to a firm understanding of how programs execute, and eventually to your own writing of programs.

We'll first do a longer, more narrative version here, and then show you how to submit a much shorter version for your exercises.

For our example, let's look at the program we last saw:
```python
print(1)                   

for j in range(2, 5):      
    for i in range(j):     
        print(j, end='')
    print()    
```

---
**Exercise 9:** Complete a [tracing table](../guides/tracing) of the program above and take a picture and save it as `traceforloop.png` and attach it to the Blackboard module 8 assignment.

---

**Exercise 10:** Write a program to print out consecutive integers in a diagonal, as in

```
  1
   2
    3
     4
      5
```
  
Use a nested for-loop as in earlier examples to print the requisite number of spaces before printing a digit. Write your code in `my_diagonal_print.py`

---
 
**Exercise 11:** Write a program to print out

```
I'm feeling cold: b rrrrrr rrrrr rrrr rrr rr r
```

Use a regular `print` to print everything up to the b. Then, use a __nested for-loop__ for the r's. Don't forget the __space__ between each grouping of r's. Write your code in `my_brr_print.py`

---

## When things go wrong
 
As code gets more complex, it gets easier to make mistakes, and harder to find them.

In each of the programs below, try to determine the error without compiling the program. Then, write up the program, compile and see what the compiler says. After that, fix the error.
 

---
**Exercise 12:**

```python
for i in range(0 6):
    print(i)
```

Write your corrected code in `my_loop_exercise1.py`.
 
---

**Exercise 13:**

```python
for i in range(0, 6)
    print(i)
```

Write your corrected code in `my_loop_exercise2.py`.
 

---

**Exercise 14:**

```python
for i in range(0, 6:
    print(i)
```

Write your corrected code in `my_loop_exercise3.py`.
 
---

**Exercise 15:**

```python
for i in range(0, 6):
print(i)
```

Write your corrected code in `my_loop_exercise4.py`.

---

**Exercise 16:**

```python
for in range(0, 6):
    print(i)
```

Write your corrected code in `my_loop_exercise5.py`.


---


**Exercise 17:**

```python
for i in range(0, 6):
    print i
```

Write your corrected code in `my_loop_exercise6.py`.
 
---

Let's point out the difference between a _syntax_ error and a _logical_ error:

* A _syntax_ error will not allow a program to run.
* This means you are using the language incorrectly.
* On the other hand, you could have a program that has no syntax errors (it runs) but it does not produce the desired output. This means there's a _logical_ error.
* The process of identifying and fixing logical errors is called _debugging_.
* A _bug_ is a logical error.
 
---
**Exercise 18:** The following code intends to print

```
55555
4444
333
22
1
```

```python  
for i in range(5, 0, 1):
    for j in range(1, i):
        print(i, end='')
    print()
```

But there are two bugs. First, try to find the problems solely by reading and mental execution. Then, type up the program in `my_loop_exercise7.py`. What does it print? Report what you see in `module8.txt`. Then __fix the program__ to get the desired output.

---