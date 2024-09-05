---
layout: default
permalink: module/4
---

# Module 4: Program Tracing

* First read this page then start coding the module.
* Post your Python files to Blackboard under the Module 4 assignment.
* This is a **group assignment**, but you should each **turn in your code individually**. 
* Groups can be of size 2 or 3.  No groups should be larger than 3 students.
* **Rules for groups work:**
    * Do not divide and conquer, i.e., do not assign each person an exercise to work on individually.
    * **Work together** on **each** exercise and share responsibilities, each person should have a chance to draw flowcharts, build tracing tables, and write code.


## Exercise 1: Physics: acceleration 

Average acceleration is defined as the change of velocity divided by the time taken to make the change, as shown in the following formula:		

$$
acceleration = (v1  – v0) / t
$$

Design a program that prompts the user to enter the starting velocity `v0` in meters/second, the ending velocity `v1` in meters/second, and the time span `t` in seconds, and displays the average acceleration.

Here is a sample run:
```
Enter v0: 5.5
Enter v1: 50.9
Enter t: 4.5
The average acceleration is 10.0889
```

1. __First__ design the program by drawing a __flowchart__. 
2. __Next__, write the program __code__.
3. __Finally__, trace this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value (using values in the sample run). 

* Use the following guides as references:
    * [Flowchart Guide](../guides/flowchart)
    * [Tracing Guide](../guides/tracing)

**Note:** Take a picture of the flowchart and attach it to Blackboard as `flowchart1.png`.  Write the code in a file called `acceleration.py` and turn in this file.  Take a picture of the tracing table that you created attach it to Blackboard as `tracing1.png`. 


## Exercise 2: Energy needed to heat water

Design a program that calculates the energy needed to heat water from an initial temperature to a final temperature. Your program should prompt the user to enter the amount of water in kilograms and the initial and final temperatures of the water. 

* The formula to compute the energy is

$$
Q = M * (finalTemperature – initialTemperature) * 4184
$$

* where `M` is the weight of water in kilograms, final and initial temperatures are in degrees Celsius, and energy `Q` is measured in joules. 


Here is a sample run:
```
Enter the amount of water in kilograms: 55.5
Enter the initial temperature: 3.5
Enter the final temperature: 10.5
The energy needed is 1625484.0 joules
```

1. __First__ design the program by drawing a __flowchart__. 
2. __Next__, write the program __code__.
3. __Finally__, trace this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value (using values in the sample run). 

* Use the following guides as references:
    * [Flowchart Guide](../guides/flowchart)
    * [Tracing Guide](../guides/tracing)

**Note:** Take a picture of the flowchart and attach it to Blackboard as `flowchart2.png`.  Write the code in a file called `energy.py` and turn in this file.  Take a picture of the tracing table that you created attach it to Blackboard as `tracing2.png`. 


## Exercise 3: Convert pounds into kilograms

Design a program that converts pounds into kilograms. The program prompts the user to enter a value in pounds, converts it to kilograms, and displays the result. One pound is 0.454 kilograms. Also, trace this program and show the values that will be stored in memory and the output value (using values in sample run).

Here is a sample run:
```
Enter a value in pounds: 55.5
55.5 pounds is 25.197 kilograms
```

1. __First__ design the program by drawing a __flowchart__. 
2. __Next__, write the program __code__.
3. __Finally__, trace this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value (using values in the sample run). 

* Use the following guides as references:
    * [Flowchart Guide](../guides/flowchart)
    * [Tracing Guide](../guides/tracing)

**Note:** Take a picture of the flowchart and attach it to Blackboard as `flowchart3.png`.  Write the code in a file called `conversion.py` and turn in this file.  Take a picture of the tracing table that you created attach it to Blackboard as `tracing3.png`.


## Exercise 4: Financial application: calculate tips

Design a program that reads the subtotal and the gratuity rate and computes the gratuity and total. For example, if the user enters 10 for the subtotal and 15% for the gratuity rate, the program displays 1.5 as gratuity (subtotal * gratuity rate) and 11.5 as total (gratuity + subtotal).

Here is a sample run:
```
Enter the subtotal and a gratuity rate: 15.69, 15		
The gratuity is 2.35 and the total is 18.04
```

Hint:
* Note: There is 1 input statement that asks for both `subtotal` and `gratuity` values, i.e. using comma separated values, you can enter 2 values. Don't forget to separate the values entered by a comma (see sample run above). This is an example of simultaneous assignment (refer Lecture 2 slides)
    ```python
    subtotal, gratuity_rate = eval(input("Enter the subtotal and a gratuity rate: "))  
    ```
* If the gratuity value is stored in a variable named `gratuity` and total value is stored in a variable named `total`. Print statement can be printed as:
    ```python
    print("The gratuity is", gratuity," and the total is", total)
    ```
* To round the results you can use the Python `round` function. The `round` function takes both the number you want to round and the number of decimal digits to round to.  For example, if you want to round to two decimals you can use, `gratuity = round(gratuity, 2)`.

1. __First__ design the program by drawing a __flowchart__. 
2. __Next__, write the program __code__.
3. __Finally__, trace this program by drawing and filling out a __tracing table__ that shows the values that will be stored in memory and the output value (using values in the sample run). 

* Use the following guides as references:
    * [Flowchart Guide](../guides/flowchart)
    * [Tracing Guide](../guides/tracing)

**Note:** Take a picture of the flowchart and attach it to Blackboard as `flowchart4.png`.  Write the code in a file called `tips.py` and turn in this file.  Take a picture of the tracing table that you created attach it to Blackboard as `tracing4.png`.

---
