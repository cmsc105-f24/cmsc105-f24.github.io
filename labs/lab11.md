---
layout: default
permalink: lab/11
---

# Lab 11: File I/O

__Points Possible:__ 100

__Due:__ Thursday, November 14th

In this lab, we will write programs using Python file input and output commands.

Use the [File I/O guide](/guides/file) for assistance. 

Submission:
1.	Submit a Python file for each of the programs.


## Program 1: Word Counter

Write a program `word_counter.py` that reads from a text file, counts the number of words in the file, and outputs the count to the console.  

- Save the file called [sample.txt](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/sample.txt)
- Your program should read the contents of `sample.txt` and count the words.
- For simplicity, you can define a word as any sequence of characters separated by whitespace.

**Sample Output:**
```
Word count: 45
```

Save the program as `word_counter.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**  
(Headers and comments: 5 points, file reading: 5 points, word count calculation: 10 points, output: 5 points)  
**Total: 25 points**  


## Program 2: Uppercase Writer

Write a program `uppercase_writer.py` that reads from one file, converts its content to uppercase, and writes the uppercase text to a new file.  

- Create a file named `textfile.txt` with sample lowercase text.
- Read the contents of `textfile.txt` and write the uppercase version of the content to a new file named `uppercase_output.txt`.
- After running the program, `uppercase_output.txt` should contain the uppercase text from `textfile.txt`.

**Sample Input (textfile.txt):**  
```
hello world  
this is a test file  
```

**Sample Output (uppercase_output.txt):**  
```
HELLO WORLD  
THIS IS A TEST FILE  
```

Save the program as `uppercase_writer.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**  
(Headers and comments: 5 points, file reading: 5 points, text transformation: 10 points, file writing: 5 points)  
**Total: 25 points**  


## Program 3: Grade Average Calculator

Write a program `grade_calculator.py` that reads a list of grades from a file, calculates the average grade, and appends the average to the end of the file.  

- Create a file called `grades.txt` with a list of integer grades, one per line.
- Read all the grades, compute the average, and append the average grade to the end of the file in the format:  
  ```
  Average: [calculated_average]
  ```
  
**Sample Input (grades.txt):**  
```
85  
90  
78  
92  
88  
```

**Sample Output (grades.txt after running the program):**  
```
85  
90  
78  
92  
88  
Average: 86.6
```

Save the program as `grade_calculator.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**  
(Headers and comments: 5 points, file reading: 5 points, average calculation: 10 points, file writing/appending: 5 points)  
**Total: 25 points**  


## Program 4: Student Grades Report

Write a program `student_grades_report.py` that reads student grades from a file, processes each student’s grades, and writes a report with the highest, lowest, and average grades for each student to a new file.

- Create a file `student_grades.txt` with each line containing a student’s name followed by a list of grades, separated by commas, e.g.:  
  ```
  Alice,88,90,79  
  Bob,72,85,91  
  Charlie,100,95,100  
  ```
- Read each line from `student_grades.txt`, calculate the highest, lowest, and average grade for each student, and write these results to a new file `grades_report.txt` in the following format:  
  ```
  Alice - Highest: 90, Lowest: 79, Average: 85.67  
  Bob - Highest: 91, Lowest: 72, Average: 82.67  
  Charlie - Highest: 100, Lowest: 95, Average: 98.33  
  ```

Save the program as `student_grades_report.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**  
(Headers and comments: 5 points, file reading: 5 points, data processing: 15 points, file writing: 5 points)  
**Total: 25 points** 


