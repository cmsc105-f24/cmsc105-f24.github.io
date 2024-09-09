---
layout: default
permalink: module/5
---

# Module 5: Strings and Characters

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 5 assignment.

**Note:** Create a text file called `module5.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Write simple code that works with strings and characters (letters, digits, symbols like $)
* Identify some syntax errors related to characters and strings.

## Strings

About strings:

* We have already seen examples of strings, as in:
```python
print('Hello')
```
* Here, whatever is in between the quotes is treated _as one thing_: a sequence of letters, digits or symbols.
* Here are examples with digits, symbols and spaces:
```python
print('Hello there. I'm on my way to 123 Main Street')
print('#@%&! I'm late!')
```
* The entire sequence of letters, digits, punctuation etc from the `H` in `Hello` to the `t` in `Street` is one string.

 
Just like integer values can be placed in variables, we can do the same with strings:

* Example:
    ```python
    s = 'The quick brown fox jumps over the lazy dog'
    print(s)
    ```
* Here, the variable s has the string The quick brown fox jumps over the lazy dog

 
Consider this example:

```python
# Make a string and print it:
s = 'The quick brown fox jumps over the lazy dog'
print(s)

# Extract the length of the string and print that:
k = len(s)
print(k)
```

* Here, we are using a function called len to extract the length of a string.
* The function len is like print in one respect: there is something that goes in between the parentheses:

```python
# The string s goes into the function len.
# The resulting integer is placed in the variable k.
k = len(s)  

# The value in k, after the length has been computed
# is then printed
print(k)
```

* But it is different in another respect: something comes out of the function and gets placed into the variable k
We will later look further into how we can write our own functions that have this property of "making something and giving the result" to a variable.
 
**Exercise 1:** Type up the above in `my_string_example.py`. What is the printed length? Remember, answers to non-coding questions like this need to be in the appropriate module text file, in this case `module5.txt`.

---

## String Concatenation

Strings would be of limited use if there were no way of combining them, just as integers would be if there were no way of performing arithmetic.

The joining of two strings end to end is called _concatenation_.

Consider this program:
```python
x = 'The'
y = 'quick'
z = 'brown'

s = x + y + z
print(s)
```
    
 
**Exercise 2:** Type up the above in `my_string_example2.py`. What is the output?
 
---

About concatenation:

* The same + that we used for integer addition is what's used to concatenate strings.
* Thus _multiple-usage_ of symbols in a programming language is common: we'll see other examples of a single symbol or function serving multiple purposes.
    * How come Python doesn't get confused and think that `x`, `y`, `z` are integers wanting to be added?
    * Python is smart about context, and understands that when `+` is used with strings, the only reasonable thing to do is to concatenate. Likewise, with numbers, Python will add them.

* You may have noticed the words all strung together without a space. So let's add the spaces:

    ```python
    x = 'Sphinx'
    y = 'of'
    z = 'black'

    s = x + ' ' + y + ' ' + z + ' quartz, judge my vow'
    print(s)

    print(len(s))
    ```

    
* Notice how multiple strings, some from variables, and some just written into the statement, are concatenated:

    ```python
    # The string x concatenates with 
    # the next string (which has one space).
    # The resulting 'Sphinx' then concatenates 
    # with y and so on.

    s = x + ' ' + y + ' ' + z ' quartz, judge my vow'
    ```

**Exercise 3:** Type up the above in `my_string_example3.py`. What is the output? How many times did a concatenation occur?

--- 

We also introduced something new:
```python
print(len(s))
```
  
Here's how to read this line:
* First look at print and notice that there's something between the parentheses: `print(len(s))`
  
* Think to yourself: something is going to be given to `print` to get printed.
* Now look at what's going to `print`: `print(len(s))`
  
* Here we see that the length of the string s is being computed.
* What you should be thinking is:
    * The length will first get computed.
    * And then the result (36, in this case) will be sent to `print`.
    * `print` then prints it to the output, which is what we see.
* One way to think about this is to use a term, nesting, that we've seen before:
    * Here, the function invocation to `len` is nested in the function invocation to `print`
    * The innermost in this case executes first.

* In case you were wondering: yes, one can nest deeply with one function invocation inside another, inside another etc. But we won't need that anytime soon.
 
Often we want to concatenate strings with numbers, or other kinds of things:


For example: consider
```python
k = 26
s = str(k)
t = 'A pangram must have all ' + s + ' letters'
print(t)
```
    
* Here, the value in k is an integer.
* Prior to concatenation with a string, we first need to make a string out of the integer:

```python
s = str(k)
```
  
* We do this by sending the integer `k` to the `str` function, which builds a string version of the integer and gives that back.

* The string so computed is then placed into the variable `s` above.
* This string `s` gets concatenated with the other strings to produce the final result.
 
**Exercise 4:** Type up the above in `my_string_example4.py` to confirm.

--- 


 

Let's examine a small variation:

```python
k = 26
# You can also build a string in the print statement itself:
print('A pangram must have all ' + str(k) + ' letters')
```    
 
**Exercise 5:** Type up the above in `my_string_example5.py` to see the resulting output.

---

## Variable names
 
Most often, we've been using single letter variable names, for example:

```python
i = 7
j = 15 * i
print(j)

x = 'Hello' 
y = 'World'
z = x + ' ' + y
print(z)
```
    
Let's rewrite the above with more meaningful variable names:

```python
days_in_a_week = 7
days_in_a_semester = 15 * days_in_a_week
print(days_in_a_semester)

first_greeting_word = 'Hello' 
second_greeting_word= 'World'
full_greeting = first_greeting_word + ' ' + second_greeting_word
print(full_greeting)
```    

About variable names:

* First, let's review the very notion of a name in Python, along with other kinds of "words" that are allowed in Python programs.
* Reserved words or keywords:
    * Some words in the language belong formally to the language itself.
    * These are words like `for`, `in`, `def`, and others.
    * In fact, just to complete this, here's the full set of 33 reserved words:
        ```    
        and as assert break class continue def del elif else except False finally for from global if import in is lambda None nonlocal not or pass raise return True try while with yield
        ```

**Exercise 6:**  Let's see what can go wrong if we use one of the words "already taken". Consider this program:

```python
s = 'Hello'
len = 5       # This is a BAD idea
print(len)
```  

We really should not be using a variable called `len` since `len` is a predefined "already taken" name. What happens if you type and run this? Type your program in `my_variable_name.py`. 

Then, type this program in `my_variable_name2.py`:

```python
s = 'Hello'
len = 5       # This is a BAD idea
print(len)

t = 'Some looooooong sentence'
k = len(t)
print(k)
```  

What do you see? (Respond in your `module5.txt`.)

---


## When things go wrong
 
In each of the exercises below, try to identify the error before typing it up and confirming. Report the error in the `module.txt`. Then, fix the error in the code, using the specified program (`.py`) name.
 

**Exercise 7:**

```python
x = 'Hello'
y = 'World'
s = 'x' + ' ' + 'y'
```

This should print Hello World, with a space in between. Fix the error in `error1.py`.

---

**Exercise 8:**

```python
k = 8
s = 'There are ' + k + ' planets in our solar system'
print(s)
```  

Fix the error in `error2.py`.

--- 

**Exercise 9:**

```python
long_sentence = 'How' + ' ' + 'vexingly' + ' ' +
   'quick' + ' ' + 'daft' + ' ' + 'zebras' + ' ' + 'jump'
```

Fix the error in `error3.py`.
 
---

**Exercise 10:**

```python
x = input('Enter a number between 1 and 10')
y = 2 * x
print(y)
```
  
Fix the error in `error4.py`.

---