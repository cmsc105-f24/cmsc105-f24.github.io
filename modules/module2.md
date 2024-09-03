---
layout: default
permalink: module/2
---

# Module 2: A few more getting-started examples

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 2 assignment.

**Note:** Create a text file called `module2.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Learn what a comment is, and how to write them
* Write programs with multiple prints
* Escape sequences
* Identify new syntactic elements
* Understand case-sensitivity
* Find and fix errors
 
## Comments

A comment is like a note-to-self that you include directly in a program as a way to explain something to yourself for later, or to someone else who reads your program.

```python
# This is a comment
    # This is one too, but not recommended 

print("Something")      # And so is this
```

Let's explain:
- A comment begins with a # and ends at the end of the line.
- Anything written as a comment is not treated by your computer as a "command" or as programming intent.
- Thus, as far as programming goes, the above program is as good as:
    ```python
    print("Something")
    ```

---
**Exercise 1:**  Write up the above in a file called `my_comments.py`. Fix the second comment to start at the beginning of the line, and add an entirely new comment line of your own. Attach this file to the Blackboard module 2 assignment (and do this for every exercise in the future that involves a program). 

---


Sometimes one needs a comment to spill over multiple lines, as in

```python
# I wrote this program at midnight
20 seconds before the deadline
print("Something") 
``` 
    
Notice the missing `#` in the second line of the comment.
 
--- 
**Exercise 2:** Write up the above in a file called `comment_error.py`. What is the error displayed when you try to run the program? Write the error in your `module2.txt` file.

---

## Whitespace 

Consider the following program:

```python
print   (  "Hello World!"     ) 
```    

Notice the spaces inserted in various places.
 
--- 
**Exercise 3:** Write up the above in `whitespace_example.py`. Does the program run? Write your answer in `module2.txt` file. Remember: if it's not clear where to write your answer, write it in your module text file (for this module that's `module2.txt`).

---


Consider this variation

```python
  print("Hello World!") 
```

(Two spaces before print).
 
--- 
**Exercise 4:** Write up the above in `whitespace_example2.py`. What is the error produced? Write your answer in `module2.txt`.

---

Finally, look at:

```python
print("Hello     World!") 
```

(Extra spaces between Hello and World.)
 
--- 
**Exercise 5:** Write up the above in `whitespace_example3.py`. What is printed out? Write your answer in `module2.txt`.

--- 

Let's point out a few things:
- Some kinds of whitespace, even if ill-advised, is permitted.
- When starting a line of code, proper indentation is expected, which is why we got an error when we indented the line starting with print.
- The extra spaces between Hello and World are perfectly acceptable if the goal is to print them. Printing accepts whatever spaces you want printed.


## Strings
 
A string in Python is a sequence of letters, digits, or symbols (like $ or *) surrounded by either
- A pair of double quotes, as in: "Hello World!"
- A pair of single quotes as in: 'Hello World!'

Note:
- Whichever quote you use to start a string must be used to end the string.
- The ending quote must be on the same line as the starting quote.
- There are special techniques to handle long strings that need to spill over multiple lines (which we'll see below).
- This raises some questions:
    - Is it possible to print a single line but with multiple print statements?
    - How does one print a quote?

First, note that we can use single or double quotes for different strings in the same program:
```python
print('Hello')
print("World!") 
```    
--- 
**Exercise 6:** Confirm that Hello and World! get printed on two lines by writing the above in `my_string_example.py`.

---
 

A print statement prints the string within parenthesis and then goes to the next line of output, which is why we see World! on the next line.
 

To keep printing on the same line:

```python
print("Hello", end=' ')
print("World!")
```

 
--- 
**Exercise 7:** Confirm by writing the above in `my_string_example2.py`.

--- 

We'll now go the other way and have a single string itself contain a directive to spill over to the next line.

```python
print('Hello\nWorld!') 
```    

Notice the backslash \ followed by n inside the string: 'Hello\nWorld!'
 

--- 
**Exercise 8** Write up the above `my_string_example3.py`. What is the output? Write your answer in `module2.txt`.

---

Strings can embed special so-called escape sequences that begin with backslash.

This will give us one way to print a quote:

```python
print('My friend\'s friend\'s dog\'s friend')
```
    
Another way is to use one set of quotes to delimit the string that are different from the ones used within:

```python
print('My friend\'s friend\'s dog\'s friend')
print("bit my friend's dog's ankle")
print('who yelped "owww"')
```

How does one print a backslash itself? By using a double backslash:

```python
print("The backslash character, \\, is less intimidating now")
```    
 
--- 
**Exercise 9:** Write a program called `practice_escaping.py` that prints out

```text
  "    "   \\\
  "    "    \    
  """"""    \    
  "    "    \    
  "    "   \\\  
```  

---

Another use of backslash: to make long strings
- Sometimes we need to type in a really long string.
- The following does NOT work:

```python
print("An Ogden Nash poem:")
print("The camel has a single hump; 
The dromedary, two; 
Or else the other way around. 
I’m never sure. Are you?")
```
    
 
**Exercise 10:** Write a program called `my_string_example4.py` with the above program and run it. What is the error you observe? Write your answer in `module2.txt`.

--- 

To spread a single string over multiple lines, one uses a triple quote as in:

```python
print("An Ogden Nash poem:")
print('''The camel has a single hump; 
The dromedary, two; 
Or else the other way around. 
I’m never sure. Are you?''')
```    
 
**Exercise 11:** Write a program called `my_string_example5.py` with a 5-line limerick.

---
 

Empty strings:

- It is possible to not have anything in a string, as in:
    ```python
    print('')
    ```
- Notice: there are no letters, digits or anything between the two single quotes above.
- Such a string is called an empty string.
- Odd as it may seem, empty strings are useful (we'll see later) when you want to add strings to make a longer string.


## Case sensitivity
 
What if we had used uppercase P instead of lowercase p in print?

```python
Print('Hello World!')
```    
 
**Exercise 12:** Write up the above program in `case_error.py` and run it. What is the error you get? Write your answer in `module1.txt`.

---

What if we changed the case inside a string?

```python
print('helLo WoRLd!')
```  
 
**Exercise 13:** Write up the above program in `my_string_example6.py` and run it to see if it works.

---

Python is case sensitive but strings are like data inside programs, which means they can be whatever we like.
- The two strings 'Hello World!' and 'helLo WoRLd!' are fine as two different strings, if that's we want.
- However, Python has only one print and so it won't recognize Print (with capital P).


