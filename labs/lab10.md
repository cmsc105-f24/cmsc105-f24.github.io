---
layout: default
permalink: lab/10
---

# Lab 10: Dictionaries

__Points Possible:__ 100

__Due:__ Thursday, November 7th

In this lab, we will write programs using Python _dictionaries_.

Submission:
1.	Submit a Python file for each of the programs.


## Program 1: Count Vowels

Write a function `countVowel(vowel_string)` that takes as input a string `vowel_string` and returns a dictionary with the vowel in `vowel_string` as key and corresponding count as value. The search should NOT be case-sensitive. Test your function by printing the dictionary returned from the function.

Sample run:
```
Enter a string of vowels: aeiouIUOaeio
{'a': 2, 'e': 2, 'i': 3, 'o': 3, 'u': 2}
```

Save the program is `countvowels.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 10 points, output: 5 points)
**Total: 25 points**


# Program 2: Unique Values

Given a dictionary of lists, write a program that extracts unique values in the
list and print a new list of unique values.

Given:

```
{'Student 1': [100, 98, 97, 96], 'Student 2': [88, 97, 75, 100], 'Student 3': [98,
97, 96, 77]}
```

Output: 

```
Unique items : [100, 98, 97, 96, 88, 75, 77]
```

__Hint:__  First, iterate over each key of the dictionary, next iterate over each element of the list associated with that key.

```python
for element in dict[key]:  # Here d[key] is a list.
```

Save the program is `uniqueValues.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 30 points, result: 5 points)
**Total: 45 points**


## Program 3: Min Max Mean

Write a program that takes as input a list of numbers and prints a dictionary
that contains key-value pairs for -- "Mean Value","Maximum Value" and
"Minimum Value".

Sample run:
```
lst=[10,12,32,4]
d={"Mean Value":14.5,"Maximum Value":32,"Minimum Value":4}
```

Save the program is `minMaxMean.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**
(Headers and comments: 5 points, input: 5 points, computation: 15 points, result: 5 points)
**Total: 30 points**
