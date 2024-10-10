---
layout: default
permalink: module/11
---

# Module 11: Introduction to Turtle Graphics

* First read this page and then start coding the module.
* Post your Python files to Blackboard under the Module 11 assignment.

## Objectives

By the end of this module, you will be able to:
* Use the Turtle graphics library in Python.
* Control turtle movements with basic commands.
* Create simple shapes and patterns using Turtle.
* Use loops to generate repeated patterns.
* Customize colors and pen properties in Turtle graphics.

## Getting Started with Turtle Graphics

### What is Turtle?

Turtle graphics provides a visual way to see what your code does by moving a turtle (cursor) around the screen.

### How to Use Turtle

Before we can use Turtle, make sure to import the library:

```python
import turtle
```

This library provides all the tools to control the turtle. When you run your program, a new window will appear where the turtle will draw shapes and patterns.

---

**Exercise 1:** Open your Python editor and create a new file called `turtle_intro.py`. Use the following code to get started:

```python
import turtle

# Create a turtle object
leonardo = turtle.Turtle()

# Set the shape of the turtle
leonardo.shape('turtle')

# Move the turtle forward by 100 units
leonardo.forward(100)
```

Run the program and observe the turtle moving across the screen!

---

## Turtle Movement Commands

You can move the turtle using several commands. Below are some basic turtle movement functions:

- `turtle.forward(distance)`: Moves the turtle forward by the given distance.
- `turtle.backward(distance)`: Moves the turtle backward by the given distance.
- `turtle.left(angle)`: Turns the turtle left by the specified angle (in degrees).
- `turtle.right(angle)`: Turns the turtle right by the specified angle.

### Example: Drawing a Square

Let’s use these commands to draw a square.

```python
import turtle

leonardo = turtle.Turtle()
leonardo.shape('turtle')

# Move the turtle in a square
for i in range(4):
    leonardo.forward(100)
    leonardo.right(90)
```

---

**Exercise 2:** In your `turtle_intro.py` file, add code to draw a square, as shown above. Experiment by changing the angles and distances to create new shapes.

---

## Customizing Your Turtle

You can customize your turtle’s appearance and how it draws on the screen.

### Changing the Pen Size and Color

You can change the thickness of the lines the turtle draws and its color:

- `turtle.pensize(size)`: Changes the width of the pen.
- `turtle.pencolor(color)`: Changes the color of the turtle’s pen. You can use common color names like `'red'`, `'blue'`, or `'green'`.

### Example: Drawing a Colored Triangle

```python
import turtle

leonardo = turtle.Turtle()
leonardo.shape('turtle')

# Set pen size and color
leonardo.pensize(5)
leonardo.pencolor('blue')

# Draw a triangle
for i in range(3):
    leonardo.forward(150)
    leonardo.left(120)
```

---

**Exercise 3:** Modify your `turtle_intro.py` file to draw a triangle with different pen sizes and colors. Experiment with drawing other polygons like pentagons or hexagons.

---

## Using Loops for Repeated Patterns

We can use loops to easily create complex patterns without repeating code. For example, let’s draw a flower by repeating a simple shape.

### Example: Drawing a Flower

```python
import turtle

leonardo = turtle.Turtle()
leonardo.shape('turtle')

# Draw a flower by repeating a petal shape
for i in range(36):
    leonardo.forward(100)
    leonardo.right(60)
    leonardo.forward(100)
    leonardo.right(120)
    leonardo.forward(100)
    leonardo.right(60)
    leonardo.forward(100)
    leonardo.right(10)
```

---

**Exercise 4:** Create a new file called `turtle_flower.py` and use the code above to draw a flower pattern. Experiment by changing the angles and the number of repetitions.

---

## Drawing Circles and Arcs

In addition to straight lines, the turtle can draw circles and arcs.

- `turtle.circle(radius)`: Draws a circle with the given radius.
- `turtle.circle(radius, angle)`: Draws an arc (a part of a circle) with the given radius and angle.

### Example: Drawing a Sun

```python
import turtle

leonardo = turtle.Turtle()
leonardo.shape('turtle')

# Draw a circle (the sun)
leonardo.pencolor('orange')
leonardo.circle(50)

# Draw sun rays
for i in range(12):
    leonardo.penup()      # Pick up the pen
    leonardo.goto(0, 50)  # Move to the center of the circle
    leonardo.pendown()    # Put down the pen
    leonardo.forward(100)
    leonardo.backward(100)
    leonardo.right(30)
```

---

**Exercise 5:** In a new file called `turtle_sun.py`, draw a sun with rays as shown above. Feel free to experiment with different colors, pen sizes, and patterns.

---

## Changing the Turtle’s Speed

If the turtle is moving too slowly, you can change its speed using the `turtle.speed()` function. The speed values range from 1 (slow) to 10 (fast), or you can use `0` for the fastest speed.

---

**Exercise 6:** Add `leonardo.speed(10)` to your `turtle_flower.py` file and see how fast your flower is drawn! What happens when you change the speed value?

---

## Adding Fill Colors

You can also fill shapes with colors using `turtle.begin_fill()` and `turtle.end_fill()`:

- `turtle.begin_fill()`: Starts filling the shape.
- `turtle.end_fill()`: Stops filling the shape.

### Example: Drawing a Filled Star

```python
import turtle

leonardo = turtle.Turtle()
leonardo.shape('turtle')

# Set fill color
leonardo.fillcolor('yellow')

# Begin filling the star
leonardo.begin_fill()

# Draw a star
for i in range(5):
    leonardo.forward(100)
    leonardo.right(144)

# End filling
leonardo.end_fill()
```

---

**Exercise 7:** In a new file called `turtle_star.py`, create a filled star like the example above. Experiment with other shapes and colors.

---

## Recap and Final Project

You now know how to:
- Move the turtle in different directions.
- Change the turtle’s pen size and color.
- Use loops to create repeated patterns.
- Draw circles, arcs, and other shapes.
- Fill shapes with color.

### Final Project: Design Your Own Pattern

Using everything you’ve learned in this module, create your own unique pattern in a new file called `turtle_project.py`. You can use loops, colors, shapes, and other turtle features. Be creative!

---

**Submission Instructions:**
- Submit the following files to Blackboard:
  - `turtle_intro.py`
  - `turtle_flower.py`
  - `turtle_sun.py`
  - `turtle_star.py`
  - `turtle_project.py`


---