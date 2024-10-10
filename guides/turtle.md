---
layout: default
permalink: /guides/turtle
title: Turtle Commands Guide
---

# Turtle Commands Guide

This guide provides an overview of the most common turtle graphics commands in Python, with simple examples for each.

### Getting Started

Before you can use turtle commands, you need to import the turtle module and create a turtle object.

```python
import turtle

# Create a turtle object
my_turtle = turtle.Turtle()
```

To keep the window open after the turtle finishes drawing, use:

```python
turtle.exitonclick()
```

## Movement Commands

### `forward(distance)`

Moves the turtle forward by the specified distance (in pixels).

```python
my_turtle.forward(100)  # Moves forward by 100 units
```

### `backward(distance)`

Moves the turtle backward by the specified distance.

```python
my_turtle.backward(50)  # Moves backward by 50 units
```

### `left(angle)`

Turns the turtle counterclockwise by the specified angle (in degrees).

```python
my_turtle.left(90)  # Turns left by 90 degrees
```

### `right(angle)`

Turns the turtle clockwise by the specified angle.

```python
my_turtle.right(45)  # Turns right by 45 degrees
```

### `goto(x, y)`

Moves the turtle to the specified `(x, y)` coordinates.

```python
my_turtle.goto(100, 200)  # Moves to coordinates (100, 200)
```

### `setheading(angle)`

Sets the turtle's heading (direction) to the specified angle (0 is east, 90 is north, etc.).

```python
my_turtle.setheading(180)  # Sets heading to 180 degrees (west)
```

### `circle(radius, extent=None, steps=None)`

Draws a circle with the specified radius. Optional arguments `extent` (portion of the circle) and `steps` (number of sides in the polygon) can be used to modify the circle.

```python
my_turtle.circle(50)  # Draws a full circle with radius 50
my_turtle.circle(50, 180)  # Draws a half circle with radius 50
```

## Pen Control Commands

### `penup()`

Lifts the pen, so moving the turtle will not draw anything.

```python
my_turtle.penup()  # Lifts the pen
```

### `pendown()`

Lowers the pen to start drawing again after it was lifted.

```python
my_turtle.pendown()  # Puts the pen down to resume drawing
```

### `pensize(width)`

Sets the width of the turtle's pen.

```python
my_turtle.pensize(5)  # Sets pen width to 5 pixels
```

### `pencolor(color)`

Sets the pen color. You can use color names (e.g., `'red'`, `'blue'`) or RGB values.

```python
my_turtle.pencolor('blue')  # Sets pen color to blue
my_turtle.pencolor(0.5, 0.2, 0.7)  # Sets pen color using RGB values
```

### `fillcolor(color)`

Sets the fill color used for shapes.

```python
my_turtle.fillcolor('yellow')  # Sets fill color to yellow
```

### `begin_fill()`

Marks the start of a shape to be filled.

```python
my_turtle.begin_fill()  # Begin filling a shape
```

### `end_fill()`

Fills the shape that was marked with `begin_fill()`.

```python
my_turtle.end_fill()  # Fill the shape
```

## Turtle State Commands

### `speed(speed)`

Sets the turtle’s speed. Values range from 1 (slowest) to 10 (fastest), or 0 for an instantaneous drawing.

```python
my_turtle.speed(5)  # Sets speed to 5
my_turtle.speed(0)  # Maximum speed (instant drawing)
```

### `shape(shape)`

Changes the turtle’s shape. Available shapes include `'arrow'`, `'turtle'`, `'circle'`, `'square'`, `'triangle'`, and `'classic'`.

```python
my_turtle.shape('turtle')  # Sets shape to turtle
```

### `stamp()`

Leaves an impression of the turtle’s shape at the current location.

```python
my_turtle.stamp()  # Leaves a stamp of the turtle's current position
```

### `clear()`

Clears all drawings but does not reset the turtle’s position or heading.

```python
my_turtle.clear()  # Clears the drawing
```

### `reset()`

Clears all drawings and resets the turtle to the starting position and heading.

```python
my_turtle.reset()  # Clears the drawing and resets turtle position
```

### `hideturtle()`

Hides the turtle's icon (it can still draw, but the turtle shape is invisible).

```python
my_turtle.hideturtle()  # Hides the turtle icon
```

### `showturtle()`

Shows the turtle's icon if it was hidden.

```python
my_turtle.showturtle()  # Shows the turtle icon again
```

## Utility Commands

### `home()`

Moves the turtle back to the origin `(0, 0)` and resets the heading to the default (facing east).

```python
my_turtle.home()  # Moves back to (0, 0) and resets heading
```

### `write(text, move=False, align='left', font=('Arial', 8, 'normal'))`

Writes text at the turtle's position. Optional arguments allow you to specify if the turtle should move after writing, the alignment, and the font.

```python
my_turtle.write("Hello, Turtle!", align="center", font=("Arial", 16, "bold"))
```

## Ending Commands

### `exitonclick()`

Keeps the turtle graphics window open until it is clicked. This is essential to prevent the window from closing immediately after the program finishes.

```python
turtle.exitonclick()  # Closes the window when clicked
```

---

## Full Example

Here is a complete example that demonstrates multiple commands from this guide:

```python
import turtle

# Create a turtle object
my_turtle = turtle.Turtle()

# Set pen size and color
my_turtle.pensize(3)
my_turtle.pencolor('blue')

# Draw a square
for _ in range(4):
    my_turtle.forward(100)
    my_turtle.right(90)

# Move to a new location without drawing
my_turtle.penup()
my_turtle.goto(-150, 100)
my_turtle.pendown()

# Draw a filled circle
my_turtle.fillcolor('yellow')
my_turtle.begin_fill()
my_turtle.circle(50)
my_turtle.end_fill()

# Write text
my_turtle.penup()
my_turtle.goto(0, -50)
my_turtle.pendown()
my_turtle.write("Turtle Graphics!", align="center", font=("Arial", 24, "bold"))

# Exit on click
turtle.exitonclick()
```

--- 

