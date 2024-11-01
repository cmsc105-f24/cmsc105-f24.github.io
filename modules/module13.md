---
layout: default
permalink: module/13
---

# Module 13: Tuples, Sets, and Dictionaries

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 13 assignment.

**Note:** Create a text file called `module13.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Understand how a tuples, sets, and dictionaries are different from lists
* Explore the syntax around using tuples, sets, dictionaries in programs
* Use tuples, sets, and dictionaries in programs to solve problems


## Tuples

Suppose we want to write a function that computes both the square and cube of a number:

* One option is to write two separate functions
    ```python
    def square(x):
        return x * x

    def cube(x):
        return x * x * x

    x = 5
    print(x, square(x), cube(x))
    ```
* We can alternatively write one function that computes and returns two things:
    ```python
    def do_both(x):
        square = x*x
        cube = square*x 
        return (square, cube)

    x = 5
    (y, z) = do_both(x)
    print(x, y, z)
    ```
  
* Notice that the return statement returns a pair of values: 
    ```python
    return (square, cube)
    ```
  
* And that the pair is enclosed in parentheses.
* And notice that, since two values are being returned, we need a pair to capture the return values:
    ```python
    (y, z) = do_both(x)
    ``` 

* We can go beyond a pair to any number of such "_grouped_" variables:
    ```python
    def do_more(x):
        square = x*x
        cube = square*x 
        fourth = cube*x
        fifth = fourth*x
        return (square, cube, fourth, fifth)

    x = 5
    (a, b, c, d) = do_more(x)
    print(x, a, b, c, d)
    ```

* Such a grouping of variables is called a __tuple__.
 
Tuples are similar to lists in many ways, but different in one crucial aspect:

* First, let's examine how to write the same `do_both()` function above but using lists:
    ```python
    def do_both_list(x):
        square = x*x
        cube = square*x 
        return [square, cube]

    x = 5
    [y, z] = do_both_list(x)
    print(x, y, z)
    ```


* This works just fine.

* Another way in which a tuple is like a list is in using square-brackets and position indices to access individual elements, as in:
    ```python
    # List version:
    L = do_both_list(x)
    print(L[0], L[1])      # L[0] has the square, L[1] has the cube

    # Tuple version:
    t = do_both(x)
    print(t[0], t[1])      # t[0] has the square, t[1] has the cube
    ```

* However, here's the difference:
    ```python
    # List version:
    L = do_both_list(x)
    L[0] = 0              # This is allowed

    # Tuple version:
    t = do_both(x)
    t[0] = 0              # This is NOT allowed
    ```

Thus, you can replace a list element but you cannot replace a tuple element.

* This is in fact a bit subtle, as this example shows:
    ```python
    x = 3
    y = 4
    t = (x, y)   # The tuple's value is now fixed.
    print(t)     # (3, 4)
    x = 2
    print(t)     # (3, 4)
    ```  

Once the tuple is instantiated (that's the technical term for "made") then the tuple's value cannot be changed.

* You can of course assign a different tuple value to a tuple variable as in:
    ```python
    t = (1, 2)
    print(t)
    t = (3, 4)
    print(t)
    ```

Here, we're simply replacing one fixed-value tuple with another.

* Tuples are therefore said to be an immutable type (along with strings).
* Why use tuples at all? It's to allow programmers to signal clearly that their tuples shouldn't be changed.
* This turns out to be convenient for mathematical tuples (like points on a graph), which are similar.
 
Groups of tuples can be combined into lists and other data structures.

* It's very useful in working with points (the mathematical point you draw with coordinates) and other mathematical structures that need more than one number to describe.

* For example, here's a program that, given a list of points, finds the leftmost point (the one with the least `x` value).
    ```python
    def leftmost(L):
        leftmost_guess = L[0]
        for q in L:
            if q[0] < leftmost_guess[0]:
                leftmost_guess = q
        return leftmost_guess

    list_of_points = [(3,4), (1,2), (3,2), (4,3), (5,6)]
    (x,y) = leftmost(list_of_points)
    print('leftmost:', (x,y) )
    # leftmost: (1, 2)
    ```

---
**Exercise 1:** Type up the above in `my_tuple_example.py`. Then trace through the iteration in your `module13.txt`.
 
--- 

**Exercise 2:** Consider the following:

```python
import math

def distance(p, q):
    return math.sqrt( (p[0]-q[0])**2 + (p[1]-q[1])**2 )

def find_closest_point(p, L):
    # Write your code here to find the closest point in L to p
    # and to return both the point and the distance to it from p.

list_of_points = [(3,4), (1,2), (3,2), (4,3), (5,6)]
query_point = (5,4)
(c, d) = find_closest_point(query_point, list_of_points)
print('closest:',c,' at distance', d)
# Should print: 
# closest: (4, 3)  at distance 1.4142135623730951
```

In `my_tuple_example2.py`, fill in the missing code to find the closest point in a list of points to a given query point. Return both the closest point and the distance to the query point as a tuple.

---

## Sets

The general mathematical term __set__ means a "collection of like things but without duplicates".


Python has special syntax and operations to support this mathematical notion:

* Here are two sets being defined:
    ```python
    A = {2, 4, 5, 6, 8}       # Curly brackets
    B = {'hello', 'hi', 'hey', 'howdy'}
    ```  

The first set contains five numbers, whereas the second contains four strings.
 
Consider this variation

```python
A = {2, 4, 5, 6, 8}
B = {'hello', 'hi', 'hey', 'howdy'}

C = {8, 5, 4, 6, 2, 4, 5, 5}
print(C)

if A == C:
    print('they are equal')
else:
    print('they are not equal')
```
    
Given what we've said about sets, what will be printed?

--- 
**Exercise 3:** Type up the above in `my_set_example.py` to find out.

---


Note:

* Even though a set may not have duplicates, we are actually allowed to try to create duplicates:
    ```python
    C = {8, 5, 4, 6, 2, 4, 5, 5}
    ```
  
* Python simply **removes** the duplicates.

* Python also organizes sets so that sets can be compared for equality: 

* Thus, printing the set
    ```python
    C = {8, 5, 4, 6, 2, 4, 5, 5}
    ```  
* actually results in
    ```
    {2, 4, 5, 6, 8}
    ```  
 
What can we do with sets?

* The most common operation is to see whether some value is in some set we've defined using the keyword in:
    ```python
    def check_vowel(x):
        vowels = {'a','e','i','o','u'}
        if x in vowels:
            print(x, 'is a vowel')
        else:
            print(x, 'is not a vowel')

    check_vowel('a')
    check_vowel('b')
    ```

* Other, more mathematical operations, feature different ways of combining sets. For example:
    ```python
    A = {2, 4, 5, 6, 8}
    B = {1, 3, 5, 6}

    D = A | B    # union
    print(D)
    ```


Here, D contains every element across both sets.

* Other such operators include:
    * intersection (elements that are in both sets)
    * difference (elements in one set that are not in the other)


## Dictionaries

Consider this problem:

* We have a data file that looks like this:

Download the file here: [fruits.txt](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/fruits.txt)

**fruits.txt**
```
apple
banana
apple
pear
banana
banana
apple
kiwi
orange
orange
orange
kiwi
orange
```
  
This might represent, for example, a record of sales at a fruit stand.

* We'd like to count how many of each fruit.
* One way would be to define a counter for each kind:
    ```python
    num_apples = 0
    num_bananas = 0
    num_pears = 0
    num_kiwis = 0
    num_oranges = 0
    with open('fruits.txt','r') as data_file:
        line = data_file.readline()
        while line != '':
            fruit = line.strip()
            if fruit == 'apple':
                num_apples += 1
            elif fruit == 'banana':
                num_bananas += 1
            elif fruit == 'pear':
                num_pears += 1
            elif fruit == 'kiwi':
                num_kiwis += 1
            elif fruit == 'orange':
                num_oranges += 1
            else:
                print('unknown fruit:', fruit)
            line = data_file.readline()

    print('# apples:', num_apples)
    print('# bananas:', num_bananas)
    print('# pears:', num_pears)
    print('# kiwi:', num_kiwis)
    print('# oranges:', num_oranges)
    ```  
 
--
**Exercise 4:** Type up the above in `my_fruits.py` and use the data file `fruits.txt` to confirm. Next, in `my_fruits2.py`, change the program to accommodate the additional fruits in `fruits2.txt`.

Download the file here: [fruits2.txt](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/fruits2.txt)

**fruits2.txt**
```
apple
banana
apple
pear
banana
banana
apple
kiwi
orange
plum
orange
orange
kiwi
plum
orange
peach
```
-- 

Aside from being tedious, this approach has other issues:

* One would like to be able to write a general program that does not need to know which fruits are in a file.
* What if there were a thousand different kinds of items (not fruits, say, but department-store items)?
* A single mistake in a variable can cause the counts to be wrong.
 
Fortunately, the use of dictionaries will make it easy:

```python
# Make an empty dictionary
counters = dict()

with open('fruits.txt','r') as data_file:
    line = data_file.readline()
    while line != '':
        fruit = line.strip()
        if fruit in counters.keys():
            # If we've seen the fruit before, increment.
            counters[fruit] += 1
        else:
            # If this is the first time, set the counter to 1
            counters[fruit] = 1
        line = data_file.readline()

print(counters)
```    
 
**Exercise 5:** Type up the above in `my_fruits3.py` and first apply it to `fruits.txt` and then to `fruits2.txt`. (Submit your program with the latter file as the input file.) In your `module13.txt`, describe what you had to change in the code to make it work for the second file.
 

Now let's explain:

* A __dictionary__ is a technical term that is only somewhat related to an actual English dictionary.
* Think of an English dictionary as something where you look up a word and receive its meaning.
* They operations here are look up and receive an associated value (the word's meaning, in this case).
* In Python, a dictionary is a structure that lets you associate one kind of data with another.
* The technical equivalent of a word is called a key and the equivalent of the meaning is called the value.
* So, a dictionary is a collection of key-value pairs.

* Here's an example:
    ```python
    d = {'apple': 3, 'banana': 3, 'pear': 1, 'kiwi': 2, 'orange': 4}
    ```

* In this case, we're associating
    * The value `3` with the key `'apple'`
    * The value `3` with the key `'banana'`
    * The value `1` with the key `'pear`'
    * The value `2` with the key `'kiwi'`
    * The value `4` with the key `'orange'`

* Conveniently, Python allows array indexing using the key:
    ```python
    d = {'apple': 3, 'banana': 3, 'pear': 1, 'kiwi': 2, 'orange': 4}

    print(d['apple'])  # Prints 3

    d['banana'] = 0    
    # Which changes the value associated with 'banana' to 3
    ``` 

* The above is an example of a dictionary that's already built (after we've processed the data).

* To process data on-the-fly, we need an additional operation that an English dictionary does not really have: we need to be able to add something that's not already there.

* To add a new key, we simply use it as an index:
    ```python
    d = {'apple': 3, 'banana': 3, 'pear': 1, 'kiwi': 2, 'orange': 4}

    d['plum'] = 0
    ```  
 
With this understanding we can now revisit the code in the fruit example:

* We've seen how to read a file line-by-line before
    ```python
    with open('fruits.txt','r') as data_file:
        line = data_file.readline()
        while line != '':
            fruit = line.strip()    # Remove whitespace on either side

            # This is where we'd do something with the data

            line = data_file.readline()    # Get the next line
    ```

* The rest is merely the dictionary part:
    ```python
    with open('fruits.txt','r') as data_file:
        line = data_file.readline()
        while line != '':
            fruit = line.strip()    # Remove whitespace on either side

            if fruit in counters.keys():
                # If we've seen the fruit before, increment.
                counters[fruit] += 1
            else:
                # If this is the first time, set the counter to 1
                counters[fruit] = 1

            line = data_file.readline()    # Get the next line
    ```