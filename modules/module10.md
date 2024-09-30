---
layout: default
permalink: module/10
---

# Module 10: Functions: a first look

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 10 assignment.

**Note:** Create a text file called `module10.txt` where you will store you answers to exercise questions. The questions that are not related to changing code. You will submit this file on Blackboard along with your code. 

## Objectives

By the end of this module you will be able to:
* Demonstrate function calls.
* Use mental tracing to identify output without execution.
* Add numbered comments to show an execution trace.
* Identify and correct syntax errors related to the above objectives.


## An example with function calls


Consider the following program:

```python
# define a function we'll use later
def print_big_M():    
    print('*   *')
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *')

# define another one we'll use later
def print_big_O():    
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****')

# Print MOO using the above defined functions
print_big_M()
print_big_O()
print_big_O()
```

--- 
**Exercise 1:** Type up the above in `animal_sounds.py` and run it. 
 
--- 

Let's point out a few things:

```python
# The "def" keyword tells Python we are defining a function
# print_big_M is the name we have given to this function
# The parens () in this case don't have anything between them
# The line that defines a function must end with a colon
def print_big_M():
    # These 5 indented prints form the "body" of the function    
    print('*   *')
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *')

def print_big_O():    
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****')

# Here, we invoke (or call) the function print_big_M
print_big_M()

# The function print_big_O is invoked twice
print_big_O() 
print_big_O()
```

* Let's start by distinguishing between a function definition (which uses `def`. and merely tells Python what the function is about), and invocation (which asks Python to execute the function at that moment).
* A __function definition__ is a piece of code that begins with the word `def`.
    * A function definition is sometimes also called function declaration.
    * A function definition does not execute the code immediately.
    * Instead it's like saving in one place a bunch of instructions that can be invoked with just the name of the function.
    * This saves writing lots of code if a group of code can be given a name (in this case, a function name).

* A function definition has 5 elements:
    ```python
    # (1) The "def" word (not indented)
    # (2) A name like print_big_M
    # (3) Parentheses that may or may not enclose things
    # (4) A colon after the parentheses
    def print_big_M():
        # (5) A block of code that is indented    
        print('*   *')
        print('** **')
        print('* * *')
        print('*   *')
        print('*   *')
    ```

* A function with a given name is defined just once.
* A function invocation merely uses the name, along with parentheses:
    ```python
    print_big_M()
    ```
We'll later see examples where some things can go between the parens.

* While a particular function is defined once, it can be used any number of times:
    * In fact, that is the whole purpose of defining functions.
    * Each use of a function is a single line of code, which saves us the trouble of rewriting all the code that was inside the function for each time we need it.
* Function definitions also help isolate code so that one doesn't have to see or understand what's inside to use it.
* We've already used such a function before: the `print` function.
    * The `print` function is defined internal to Python.
    * We don't type its definition, nor do we see it.
    * We just use it as often as we like.

* **Important:** please pay careful attention to indentation
    * The line that begins with `def` should NOT be indented.
    * Other lines that belong to the function should be indented.
    * There are other forms of indentation that we'll point out as we proceed - they're all `important`.


---
**Exercise 2:** Write your own animal sound that uses one function at least thrice with an exclamation mark at the end, e.g. print the big version of BAAA!. Write your code in `my_pet_sound.py`. 
 
--- 


Next, let's see how functions "work" by making a small change to the program:

```python    	
def print_big_M():
    print('*   *')
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *')

def print_big_O():
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****')

print('Step 1')
print_big_M()
print('Step 8')
print_big_O()
print('Step x')
print_big_O()
print('Step y')
```    
 
---
**Exercise 3:** Type up the above in `animal_sounds2.py` and run it.
 
--- 

Let's explain using an analogy:


```python 
# The print_big_M room	
def print_big_M():
    # After getting into this room
    # this gets executed next
    print('*   *') 
    print('** **') # Then this
    print('* * *') # Then this
    print('*   *') # Then this
    print('*   *') # Then this
    # After this last line
    # we return to after the instruction
    # to come into this room

def print_big_O():
    # Notice the 4-space indentation (tab)
    # This tells us that this group of 5 indented 
    # prints are all inside the print_big_O() function
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****')

# This is the main lobby
# Execution starts here
print('Step 1')
# This says "go to the print_big_M room"
print_big_M()
# Execution reaches here after returning from the print_big_M room 
print('Step 8') 
print_big_O()
print('Step x')
print_big_O()
print('Step y')
```  

* We'll use the analogy of a house to describe a program and its parts (the functions).
* A program's execution starts at the very top.
* In the above case, there are a number of definitions:
    * Definitions are merely "processed" but not executed.
    * It's understood that the definitions may be invoked later.
    * In our house analogy, we walk past these "rooms" to the main lobby.
* The first real line of code is the `print('Step 1')` statement.
    * Think of this section of code as the "main lobby".
* After this, we see the line (also a command) `print_big_M()`
    * This is an instruction that causes the computer to "go to the `print_big_M()` room".
    * We then head to that room and start executing commands in there.
* Thus, the third command that gets executed is `print('* *')`
* We're still in the room with more commands to go, and the next one (4th so far) is `print('** **')`
* Continuing, we execute the last line in the room, which will make this the 7th one executed.
* After we leave the "room", and this is important, we continue execution after the invocation that brought us to the room.
 
--- 
**Exercise 4:** At which step (which step number) do we execute the last line in `print_big_O`? And then, at which step do we enter `print_big_O` the second time and print its first line? In `animal_sounds2.py` replace `x` and `y` with the correct step number. Don't forget: non-coding responses to exercises go into `module10.txt`.

---

## Calling functions from other functions

Consider this program:

```python    	
def print_big_M():
    print('*   *')
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *\n')

def print_big_O():
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****\n')

def print_two_big_Os():
    print_big_O()
    print_big_O()

print_big_M()
print_two_big_Os()
```

* Yes, we can write our functions that call our own functions.
* Incidentally, did you notice the escape sequences?
    * We improved the output.

--- 
**Exercise 5:** Use this idea to rewrite your own animal sound in a file called `my_pet_sound2.py`. That is, add an additional function to your earlier program `my_pet_sound.py` that is analogous to `print_two_big_Os()` above.

--- 

Once again, let's trace through some steps:

```python    	
def print_big_M():
    print('*   *')     # 2
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *\n')   # 6

def print_big_O():
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****\n')

def print_two_big_Os():
    print_big_O()      # 8
    print_big_O()      # ?

print_big_M()          # 1
print_two_big_Os()     # 7
```

--- 
**Exercise 6:** Look at the example above. What step number is represented by the question mark (?) next to the second `print_big_O()` inside the `print_two_big_Os()` function? What line in the program represents step 15? Write your answer in `module10.txt`. 

--- 


Mental execution:

* We will use the term mental execution for the above exercise of tracing through the execution without actually compiling and running the program.
* **Note:** Mental execution is extremely important in developing programming skill
    * Please be sure to practice this with every program you read or write.
* We can't emphasize this enough. Really.

* Remember:
    * Execution starts at the top of a program and goes downwards.
    * Function definitions are processed (understood) but not executed.
    * When a function are invoked, execution "goes" into the function to execute the code in there.

## More about functions
 
About function names:

* Consider the function name `print_big_M`.
* This is a name we chose.
* We could just as easily have called it `my_crazy_function`:

    ```python
    def my_crazy_function():
        print('*   *')
        print('** **')
        print('* * *')
        print('*   *')
        print('*   *\n')

    def print_big_O():
        print('*****')
        print('*   *')
        print('*   *')
        print('*   *')
        print('*****\n')

    def print_two_big_Os():
        print_big_O()
        print_big_O()

    # Use the different name:
    my_crazy_function()     
    print_two_big_Os()
    ``` 

* In other words, the compiler does not look into the _English meaning_ of function names.
* We choose function names to help us read programs.
 
Beware of name clashes:

* Consider the following program (that has a mistake):

    ```python
    def print_big_M():
        print('*   *')
        print('** **')
        print('* * *')
        print('*   *')
        print('*   *\n')

    def print_big_M():      # A mistake! We meant to have typed
        print('*****')      # print_big_O()
        print('*   *')
        print('*   *')
        print('*   *')
        print('*****\n')

    # What happens now?
    print_big_M()
    ```

* In this example, we have functions with different content but with the same name.
 
--- 
**Exercise 7:** Implement the above in `name_clash.py` and describe what happens in `module10.txt`

---

* What we see is that the second definition replaces the first.
* The program runs but this error is not identified as such by the language. Instead, we need to be careful not to unintentionally make such a mistake.
 
The order of function invocation matters. For example, consider:

```python
def print_big_M():
    print('*   *')
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *\n')

def print_big_O():
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****\n')

def print_two_big_Os():
    print_big_O()
    print_big_O()

# We've changed the order here:
print_two_big_Os()
print_big_M()
```

--- 
**Exercise 8:** Describe in your `module10.txt` how the output would be different, first without typing up the program, and then typing it up in `animal_sounds3.py`.
 
---


## And now for something strange

Consider the following program:

```python
def print_big_M():   
    print('*   *')
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *\n')

def print_big_O():   
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****\n')
    print_big_O()    # We're invoking the function from within

print_big_M()
print_big_O()
```
    
--- 
**Exercise 9:** Mentally execute the above program. That is, __without__ typing it up, try to follow how the program executes, step by step. Which statement gets executed in the 10-th step of execution? Do you notice anything unusual at step 13? As a result, what line is executed in step 15? Write your answer in your `module10.txt` file.
 
---

**Exercise 10:** Before doing this exercise, remember in Thonny you can click the "**STOP**" button to stop endlessly running programs. Now, type up and execute the above program in `my_strange_example.py`. What do you notice? (Or you might get an "recursion depth exceeded" error.)
 
---

The term _recursion_ is used when function calls itself:

* In the above example, it's an obvious error
    * Nothing useful is accomplished.

* Later, we'll learn to use recursion to solve problems.
* In fact, _recursion_ is one of the most powerful computational problem-solving paradigms.


## Functions with for-loops

Consider the following program:

```python
def print_big_M():  
    print('*   *')
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *\n')

def print_big_O():  
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****\n')

print_big_M()
print_big_O()  
print_big_O()  # 1st repetition
print_big_O()  # 2nd repetition
print_big_O()
print_big_O()
print_big_O()  # 5th repetition - 6 O's in all
``` 

What we would like is a way to organize repetition.

We will do this using one version (there are many) of the for-loop, one of the most important programming constructs:

```python
def print_big_M():  
    print('*   *')
    print('** **')
    print('* * *')
    print('*   *')
    print('*   *\n')

def print_big_O():  
    print('*****')
    print('*   *')
    print('*   *')
    print('*   *')
    print('*****\n')


print_big_M()
for i in range(6):
    print_big_O()
```    

--- 
**Exercise 11:** Type up the above in `animal_sounds_loop.py` and run it. 
 
---

**Exercise 12:** Using the example above as a point of reference, print out your own animal sound. Be sure to use a `for` loop to repeatedly print one letter in the sound. Write your code in `my_pet_sound_loop.py`.

---
 
