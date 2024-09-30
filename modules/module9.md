---
layout: default
permalink: module/9
---

# Module 9: Loops: the `while` loop

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 9 assignment.

**Note:** Create a text file called `module9.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Work through examples of indefinite loops.
* Write while-loop versions of for-loops.
* Work through examples of using the break statement.


## While loops: an example

The numbers 1, 4, 9, 16, 25, and so on are squares, with the next one being 36 (which is 62).

* Suppose we want to identify the largest square that's less than 1000.

* We'll first show how this can be solved with a new kind of loop: the `while` loop, and then try the same problem with a for-loop.

The program:

```python
k = 1
while k * k < 1000:
    k = k + 1

# Reduce by 1 because now k * k > 1000
k = k - 1

print('largest square < 1000:', k * k, '= square of', k)
```

--- 
**Exercise 1:** Type up the above in `my_while_example.py`.
 
--- 

How does a while-loop work?

* The essential idea is: a while-loop keeps iterating until its condition evaluates to `False`.
* Let's examine the structure:
    ```python
    # The initialization
    k = 1   

    # The condition
    while k * k < 1000:
        # The body of the loop
        k = k + 1

    # The code right after the loop
    k = k - 1
    ```

* In our example, the condition was:
    ```python
    while k * k < 1000:
    ```

Thus, as long as the value of `k` is such that `k * k` is less than `1000`, execution enters and stays inside the loop.

* Notice that `k` is incremented (or changed) inside the loop:
    ```python
    while k * k < 1000:
        k = k + 1
    ```  

* Thus, eventually `k` will get large enough so that `k * k` will be larger than `1000`.
* When `k` is `32`, in fact, 32 * 32 = 1024, which will cause the condition `k * k < 1000` to evaluate to `False`.
* At this moment, execution exits the loop to the whatever code follows:
    ```python
    k = 1   

    # When the condition evaluates to False,
    # execution skips past the (indented) body of the loop
    while k * k < 1000:    # When k is 32, k * k is 1024
        k = k + 1

    k = k - 1
    ```

Let's examine a simpler while-loop:

```python
k = 1
while k < 6:
    print(k)
    k = k + 1
```

---
**Exercise 2:** Trace this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value. Take a picture of the tracing table that you created attach it to Blackboard as `while2.png`._Then_ confirm by typing up the above in `my_while_example2.py`.
 
--- 

**Exercise 3:** Consider this variation:

```python
k = 7
while k < 6:
    print(k)
    k = k + 1
```  

Trace this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value. Take a picture of the tracing table that you created attach it to Blackboard as `while3.png`. _Then_ confirm by typing up the above in `my_while_example3.py`.
 
---

**Exercise4:** Consider this variation:

```python
k = 1
while k < 6:
    print(k)
```  

Trace the first 10 steps of this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value. Take a picture of the tracing table that you created attach it to Blackboard as `while4.png`. _Then_ confirm by typing up the above in `my_while_example4.py`. After a minute, you may need to terminate the execution of the program by hand (by clicking the "STOP" button).
 
---

Keep in mind:

* A while-loop typically must feature some kind of initialization before the loop as in:
    ```python
    k = 1    # Initialization
    while k < 6:
        print(k)
        k = k + 1
    ```

* The variable that's involved in the condition should be changed inside the loop so that the condition __eventually__ evaluates to `False`:
    ```python
    k = 1
    while k < 6:  # Eventually false
        print(k)
        k = k + 1 # Increments k
    ```
  
* Another important thing to remember: if you forget to change a variable like `k` inside the loop, the condition will never becomes `False`, which means the loop will iterate forever:
    ```python
    k = 1
    while k < 6:
        print(k)
        i = k + 1   # Error!
    ```  

* Here
    * The incremented value `k + 1` does not get stored in `k`.
    * Which means `k` never gets large enough.
    * Therefore `k < 6` will always be `True`.
    * Thus, we get an _infinite loop_ (that iterates forever).

* It's alright, but probably not useful, if the condition never evaluates to `True` even once:
    ```python
    k = 6
    while k < 6:
        print(k)
        k = k + 1
    ```  
* The code above still runs but the while-loop is not executed at all.

## While loops: an example with floating point variables
 
Consider this example:
```python
x = 0.5
s = 0
while s <= 2:
    s = s + x

print('s =', s)
```    

--- 
**Exercise 5:** Try to guess the output before confirming in `my_while_example5.py`.
 
---

**Note:**

* The value of `x` (which is `0.5`) keeps getting added to `s`, as long as `s` is less or equal to `2`.
* Thus, the last value of `s` to keep going in the loop is when `s = 2`.
* At this time, we stay for one more iteration, after which `s` becomes `2.5`.
 
Let's look at a more illustrative version now:

```python
x = 0.5
s = 0
k = 0
while s <= 2:
    s = s + x
    k = k + 1

print('s =', s, 'k =', k)
```

Here, we've added a _counter_ variable to track each loop iteration.
 
---
**Exercise 6:** Trace this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value. Take a picture of the tracing table that you created attach it to Blackboard as `while6.png`. Then confirm in `my_while_example6.py`.

--- 

So far it's been straightforward. Let's now solve a problem:

* Remember Zeno's paradox?
* To summarize one version, Zeno said (with a wry smile, probably):
    * To walk a mile, you'd have to first walk half the remaining distance (0.5 miles).
    * Then, to get to the rest, you'd have to walk at least half of the remaining (0.25).
    * Then, half of the remainder (0.125) 
    * ... and so on.
    * So, the total distance would be an infinite sum: 0.5 + 0.25 + 0.125 + ...
    * Which is infinite [he said]

* Let's count how many successive halvings add up to, say, 0.9.

* Here's the code:

```python
x = 1
s = 0
k = 0
while s < 0.9:
    x = x / 2   # Halve x each time
    s = s + x
    k = k +1

print(k)
```
  

* We accumulate the sum in `s`.
* Note that we start with `x = 1` because we perform the halving before adding to `s`.
* This means the first value added into `s` is `0.5` (as intended).
* Each such addition into `s` get counted in `k`.
 
--- 
**Exercise 7:** Trace this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value. Take a picture of the tracing table that you created attach it to Blackboard as `while7.png`. Then confirm in `my_while_example7.py`.

---       

A few comments that go beyond the scope of the course (just for curiosity):

* The infinite sum, in fact, adds up to 1.
* It took centuries for mathematics to develop to a point where one can prove that infinite sums are acceptable and can have finite results.
* However, a computer can only represent real numbers approximately, which means the sum is itself approximate.
* You can see this by changing the while-condition from
    ```python
    while s < 0.9:
    ```  
* to
    ```python
    while s < 1:
    ```  
* Theoretical math would say that the while-loop would execute forever, but because there limits to what's representable on a computer, the loop will indeed terminate.


## for vs. while
 
Let's contrast for-loops and while-loops by writing a for-loop as a while-loop, and vice-versa.

As an example, let's print the numbers `0` through `10`:

```python
# for-loop version
for k in range(11):
    print(k)

# while-loop version
k = 0
while k < 11:
    print(k)
    k = k + 1
```

 
**Note:**

* The for-loop is simpler to write.
* The while-loop must make explicit three things:
    * The initialization:
        ```python
        k = 0
        while k < 11:
            print(k)
            k = k + 1
        ```
    * The termination condition:
        ```python
        k = 0
        while k < 11:
            print(k)
            k = k + 1
        ```  
    * And the variable change (that will ultimately cause the condition to become `False`):
        ```python
        k = 0
        while k < 11:
            print(k)
            k = k + 1
        ```  
* All of this is hidden in the for-loop.
* Underneath the hood, it turns out, the for-loop also has these three elements.
* It's just that we don't have to write them, Python does so behind the scenes.
* When you write while-loops, ask yourself: "Do I have the three elements (initialization, condition, variable-change)?"
* A really common mistake: forgetting the change, as in:
    ```python
    k = 0
    while k < 11:
        print(k)
    ```  
* This loop runs __forever__!

--- 
**Exercise 8:** Consider this for-loop:

```python
for k in range(5, 20, 2):
    print(k)
```

In `my_for_while.py`, write the while-loop equivalent.
 
---

Next, let's go from `while` to `for`:

* Consider this while-loop that prints the letters in a string backwards:
    ```python
    s = "hello"
    k = len(s) - 1
    while k >= 0:
        print(s[k])
        k = k - 1
    ```
  
**Note:**
* The initialization starts `k` at the last index of the string:
    ```python
    k = len(s) - 1
    ```
    * The loop condition expects `k` to decrement until it hits `0`.
    * After this, `k` (when it's `-1`) will have gone past the left end of the string.
    * `k` decrements in the loop.
* The equivalent for-loop is efficient to write, but less pretty:
    ```python
    for k in range(len(s) - 1, -1, -1):
        print(s[k])
    ```

* Here:
    * The range begins with
        ```python
        for k in range(len(s) - 1, -1, -1):
        ```

    * Ends with 0, but has the index just past (-1) as the limit:
        ```python
        for k in range(len(s) - 1, -1, -1):
        ```  
        * And the increment is `-1` (which makes it a decrement).
* Later, when we learn more advanced ways of using slicing, we will be able to do the same thing with shorter code.
 
--- 
**Exercise 9:** Write and test both loops in `my_for_while2.py`.

---

## Using `break` in loops
 
Let's return to our first example of finding the last square that's less than 1000.

Recall what we wrote:

```python
k = 1
while k*k < 1000:
    k = k + 1

k = k - 1
print('largest square < 1000:', k*k, '= square of', k)
```  

* One can use a `break` statement as an alternative to writing the "loop exit" condition as the while condition.

* We'll first do this with a for-loop, and then see something unusual with the while-loop version.

* To simplify tracing, let's rephrase to "largest square less than 50".

* First, the for-loop version:

```python
for k in range(1, 50):
    # print('Before-if: k =', k)
    if k*k > 50:
        break
    # print('After-if: k =', k)

k = k - 1
print(k)
```
    
--- 
**Exercise 10:** Type up the above in `my_break.py`, removing the `#` to un-comment the two `print` statements, so that you can see exactly what happens when the if-condition triggers.
 
--- 

Let's point out:

* A break-statement is the reserved word `break` all by itself on a line, as seen above.
* When a `break` statement executes, Python looks for the loop that encloses the break and abruptly, right there and then, exits the loop.
* Break-statements are useful to check for conditions that should result in leaving the loop immediately.
* One could write code like this, but it would make no sense:
    ```python
    for k in range(10):
        print(k)
        break
    ```
* This would cause the first value (0) to print, and a break right out of the loop.
* As a mathematical aside, we know that we don't really need the for-loop range to be as high as `50`:
```python
for k in range(1, 50):
    if k * k > 50:
        break
```

* After all, as `k` gets close to `50`, there is no way `k * k` would be less than 50. However, we'll leave it as is, for the sake of simplicity.
* There are options in writing the loop. Consider this one:
    ```python
    for k in range(1, 50):
        if (k + 1) * (k + 1) > 50:
            print(k)
            break
    ```  
Is this more elegant, if a bit harder to understand at first?
 
--- 
**Exercise 11:** The type it up in `my_break2.py`, to confirm.

--- 

Next, let's look at a while-loop version of the original

* Here's the code:
    ```python
    k = 1
    while True:
        if k*k > 50:
            break
        k = k + 1

    k = k - 1
    print(k)
    ```

Observe:

```python
k = 1
# The condition is set to run forever,
# and instead rely on the if-condition 
# to break out
while True:
    if k*k > 50:
        # When the break executes,
        # we jump right out of the loop
        # to whatever code follows the loop
        break
    k = k + 1

# This code is after the loop
k = k - 1
print(k)
```

* Was it surprising that we deliberately set up a loop to appear to run forever?
* This is entirely do-able and often desirable, provided we are real careful to set up a condition inside the loop to break out eventually.
* We need to be sure we hit that condition eventually.
 
---
**Exercise 12:** In your `module9.txt`, describe what would go wrong if the statement `k = k + 1` was mistakenly typed in as `k = k - 1`.

---

## Loops within loops

Just as we've seen nested for-loops, so can we have nested while-loops or one kind inside another.

Consider this example:
```python
m = 10
while m <= 10000:
    for k in range(1, m):
        if (k + 1) * (k + 1) >= m:
            print('largest square <', m, ':', k * k)
            break
    m = m * 10
```    
 
---  
**Exercise 13:** Type the above in `my_nested_loop.py` and try to make sense of it.

--- 

Let's explain:

* First, notice that we have a for-loop inside a while-loop:
    ```python
    m = 10
    while m <= 10000:
        # Body of the outer loop (in this case, a while loop)
        for k in range(1, m):
            # Body of the inner loop (in this case, a for loop)
            if (k + 1) * (k + 1) >= m:
                print('largest square <', m, ':', k * k)
                break
        m = m * 10
    ``` 

* Let's start with understanding what happens in the outer loop:
    ```python
    # m starts as 10
    m = 10

    # As long as m is less than or equal to 10000,
    # we stay in the loop
    while m <= 10000:
        # Does the code in here change m?
        for k in range(1, m):
            # Body of the inner loop (in this case, a for loop)
            if (k + 1) * (k + 1) >= m:
                print('largest square <', m, ':', k * k)
                break
        # Notice how m changes by multiplication
        m = m * 10 
    ``` 

* Thus, `m` is first `10`, then `100`, then `1000`, then `10000`.

* Now let's see what happens within one iteration of the outer loop (for a particular value of `m`):
    ```python
    m = 10
    while m <= 10000:
        # In the first iteration of the outer loop m = 10
        # so the inner for-loop has k going from 1 to 9
        for k in range(1, m):
            # When we get a square that is larger then 
            # or equal to m, we print and break
            if (k + 1) * (k + 1) >= m:
                print('largest square <', m, ':', k * k)
                # The break here will break out of the for-loop
                break
        # We break out of the for-loop to here
        m = m * 10 
    ``` 

* **Important:** The `break` in the for-loop exits the for-loop (the enclosing loop), which means we'll still be inside the while-loop (where `m` changes).

---
**Exercise 14:** In `my_nested_loop2.py`, change the inner loop to a `while` loop so that we get the same output.

--- 

**Exercise 15:** In `my_nested_loop3.py`, change the code so that both the outer loop and inner loop are for-loops. One way to solve this problem: use a variable called `j` to range through the outer for-loop and then ensure that the inner loop executes only when `j` happens to equal `m`. (Aren't you glad we have while-loops?)

---