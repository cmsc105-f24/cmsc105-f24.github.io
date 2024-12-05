---
layout: default
permalink: quiz/4
---

# Quiz 4

__Points Possible:__ 100

__Date:__ Thursday, December 5th 


## Background 
This quiz is based on the topics covered in weeks 11 through 14. There are 2 programming problems. You are allowed to use the Thonny IDE. Please see the grading rubric for each programming problem. Scratch paper and a simple calculator are allowed. You may also use the guides provided on the course web page: [https://cmsc105-f24.github.io/guides](https://cmsc105-f24.github.io/guides)

## Submission
* Submit a `quiz4.txt` file on Blackboard with your answers.
* Submit any Python code from the Thonny IDE on Blackboard.


## Program 1 (50 points)

You are tasked with creating a simple Python program to process a log file. The log file, named `server_logs.txt`, contains information about server requests in the following format:

**server_logs.txt**
```
2024-11-21 10:15:30 INFO User123 accessed /home
2024-11-21 10:20:45 ERROR User456 failed to access /dashboard
2024-11-21 10:25:50 WARNING User789 exceeded rate limit
2024-11-21 10:30:15 INFO User123 logged out
```

Each line contains a timestamp, a log level (`INFO`, `ERROR`, `WARNING`), a user identifier (e.g., User123), and a message.

The `server_logs.txt` file can be downloaded using this link: [server_logs.txt](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/server_logs.txt)


**Remember** to save the file in the same folder as your program.


Write a program to:

* Read the contents of the `server_logs.txt` file.
* Count the total number of lines in the file.
* Count how many times each log level (`INFO`, `ERROR`, `WARNING`) appears.
* Extract and save all lines with the `ERROR` log level into a new file called `error_logs.txt`.
* Print the results to the console:
    * Total number of lines.
    * Counts for each log level (`INFO`, `ERROR`, `WARNING`).
    * Confirmation that the `error_logs.txt` file has been created.


If the file `server_logs.txt` contains the sample data above, your program should print the output to the screen:

**sample output:**
```
Total lines: 4
INFO: 2
ERROR: 1
WARNING: 1
The error logs have been saved to error_logs.txt.
```

The contents of `error_logs.txt` should be:

**error_logs.txt**
```
2024-11-21 10:20:45 ERROR User456 failed to access /dashboard
```


* Save your program as `log.py` and attach it to Blackboard.
* (Comments: 5 points, file input: 10 points, computation: 20 points, file output: 10 points, print output: 5 points)


## Problem 2 (50 points)

Create a `Course` class and contains the following private data fields: `netid`, `admission_date`, `major_field_study`, `course_name`, `score`, and the following methods:
* A constructor (`__init__`) with the arguments `course_name`, `score`, `netid`, `admission_date`, `major_field_study`. Please note that all the fields except the `score` field are strings. The `score` is of type `float`.
* Get and set methods for the score field only.
* `printDetails()` method that prints the `netid`, `admission_date`, `major_field_study`, `course_name` and `score`.
* `calculateGrade()` method that returns the following grade using the following criteria:
    * Grade = "A" if the score is between 90 to 100 (including both 90 and 100)
    * Grade = "B" if the score is between 80 to 89 (including both)
    * Grade = "C" if the score is between 70 to 79 (including both)
    * Grade = "D" if the score is between 60 to 69 (including both)
    * Otherwise, Grade = "F"

<br />

Draw the **UML diagram** for the `Course` class.

<br />

Write test code that prompts the instructor to enter the `netid`, `admission_date`, `major_field_study`, `course_name` and `score`. Initiate an object of `Course` class, print the details and also print the final grade.

<br />

Sample run:

```
Enter student's netid: dbalash
Enter student's admission_date: 07-28-2023
Enter student's major: Computer Science
Enter student's course name: Algorithms
Enter student's score: 94


Student Details:

netid: dbalash
Admission Data: 07-28-2023
Major Field of Study: Computer Science
Course Name: Algorithms
Score: 94

Final Grade: A
```

* Save your program as `course.py` and attach it to Blackboard.
* Take a picture of your UML diagram and attach it to Blackboard.
* (Comments: 5 points, class and methods: 20 points, test code: 10 points, UML: 15 points)


