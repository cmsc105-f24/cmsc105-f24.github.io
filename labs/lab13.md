---
layout: default  
permalink: lab/13  
---

# Lab 13: Fun with Matplotlib  

__Points Possible:__ 100  

__Due:__ Thursday, December 5th  

In this lab, you will use Matplotlib to create visualizations using real-world data. Each program will involve reading data from a file and creating a corresponding plot.

**Submission:**  
Submit a Python file for each of the programs, along with any output images saved during execution.

---

## Program 1: Temperature Trends  

**Points Possible: 25**  

**Tasks:**  
1. Read the data from the file and create a **line plot** of the average temperature against the year.  
2. Add appropriate labels for the x-axis, y-axis, and title.  

**Starter Code for `temperature.py`**  
```python
import matplotlib.pyplot as plt

# Read data from the file
with open("temperature_data.txt", "r") as file:
    years = []
    temperatures = []
    for line in file:
        year, temp = line.strip().split(",")
        years.append(int(year))
        temperatures.append(float(temp))

# Create the line chart

```

**`temperature_data.txt`**
```
1880,14.0
1900,13.8
1950,14.3
2000,14.9
2020,15.3
```

---

Save the program as `temperature.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**  
(Comments: 5 points, read from file: 15 points, plot data: 5 points) 
**Total: 25 points**  


## Program 2: Olympic Medals  

**Points Possible: 50**  

**Tasks:**  
1. Read the data from the file and create a **bar chart** showing the number of gold medals for each country.  
2. Customize the chart by:
   - Adding labels and a title.
   - Using different colors for the bars.  

**Starter Code for `medals.py`**  
```python
import matplotlib.pyplot as plt

# Read data from the file


# Create the bar chart

```

**`olympic_medals.txt`**  
```
USA,39
China,38
Japan,27
Great Britain,22
ROC,20
```
Save the program as `medals.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**  
(Comments: 5 points, read from file: 25 points, plot data: 20 points) 
**Total: 50 points**  

---

## Program 3: Shooting Stars  

**Points Possible: 25**  

**Task:**  
1. Read the data from the file and create a **scatter plot** showing brightness against distance.  
2. Customize the plot by:
   - Adding labels and a title.
   - Using a different color or size for each point based on brightness.  

**Starter Code for `star.py`**  
```python
import matplotlib.pyplot as plt

# Read data from the file


# Create the scatter plot
plt.scatter(distances, brightness, c=brightness)
plt.xlabel("Distance from Earth (light-years)")
plt.ylabel("Brightness (magnitude)")
plt.title("Star Brightness vs. Distance")
plt.colorbar(label="Brightness Scale")
plt.show()
```

**`star_data.txt`**  
```
4.2,100
3.8,200
4.0,300
3.5,400
3.9,500
```  

Save the program as `star.py` and attach it to the Blackboard lab assignment.

**Grading Rubric for the program:**  
(Comments: 5 points, read from file: 15 points, plot data: 5 points) 
**Total: 25 points**  

---
