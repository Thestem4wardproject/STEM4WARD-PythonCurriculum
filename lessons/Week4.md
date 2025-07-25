# Week 4: Drawing with Code and Loops 🐢🎨

Get ready for the coolest week yet! Today you're going to learn how to draw pictures using code. We'll use Python's turtle graphics - imagine a little turtle with a pen that follows your commands.

## Meet Your Turtle

The turtle module lets you control a virtual turtle that draws on the screen. It's like having a remote-controlled pen!

First, let's set up our turtle:

```python
import turtle

# Create a turtle and a screen
my_turtle = turtle.Turtle()
screen = turtle.Screen()

# Keep the window open
screen.exitonclick()
```

**In Replit:** The turtle graphics will show up in a separate window next to your code.

## Basic Turtle Commands

Your turtle knows these commands:

### Moving Around
```python
my_turtle.forward(100)    # Move forward 100 pixels
my_turtle.backward(50)    # Move backward 50 pixels
my_turtle.left(90)        # Turn left 90 degrees
my_turtle.right(45)       # Turn right 45 degrees
```

### Pen Control
```python
my_turtle.penup()         # Lift the pen (move without drawing)
my_turtle.pendown()       # Put the pen down (draw while moving)
my_turtle.pencolor("red") # Change pen color
```

**Try this:** Draw a simple line:
```python
import turtle

my_turtle = turtle.Turtle()
my_turtle.forward(100)
my_turtle.left(90)
my_turtle.forward(100)

turtle.done()
```

## Drawing Your First Shapes

Let's draw a square:

```python
import turtle

my_turtle = turtle.Turtle()

# Draw a square
my_turtle.forward(100)
my_turtle.left(90)
my_turtle.forward(100)
my_turtle.left(90)
my_turtle.forward(100)
my_turtle.left(90)
my_turtle.forward(100)
my_turtle.left(90)

turtle.done()
```

That works, but it's a lot of repeated code. There's got to be a better way...

## Introducing For Loops

A `for` loop lets you repeat code without writing it over and over:

```python
import turtle

my_turtle = turtle.Turtle()

# Draw a square using a loop
for i in range(4):
    my_turtle.forward(100)
    my_turtle.left(90)

turtle.done()
```

**How it works:**
- `range(4)` means "do this 4 times"
- Each time through the loop, the indented code runs
- `i` is a counter that goes 0, 1, 2, 3 (but we don't use it here)

**Try these shapes:**
```python
# Triangle (3 sides, turn 120 degrees each time)
for i in range(3):
    my_turtle.forward(100)
    my_turtle.left(120)

# Pentagon (5 sides, turn 72 degrees each time)
for i in range(5):
    my_turtle.forward(100)
    my_turtle.left(72)
```

**Pro tip:** For any shape with n sides, turn 360/n degrees each time!

## Making Shape Functions

Let's turn our shapes into reusable functions:

```python
import turtle

my_turtle = turtle.Turtle()

def draw_square(size):
    for i in range(4):
        my_turtle.forward(size)
        my_turtle.left(90)

def draw_triangle(size):
    for i in range(3):
        my_turtle.forward(size)
        my_turtle.left(120)

# Now you can draw multiple shapes easily!
draw_square(100)
my_turtle.penup()
my_turtle.forward(150)
my_turtle.pendown()
draw_triangle(80)

turtle.done()
```

## While Loops: Keep Going Until...

`for` loops run a specific number of times. `while` loops keep going until something changes:

```python
import turtle

my_turtle = turtle.Turtle()
my_turtle.speed(10)  # Make it faster

size = 5
while size < 100:
    my_turtle.forward(size)
    my_turtle.left(91)  # Slightly more than 90 for a spiral effect
    size = size + 2

turtle.done()
```

This creates a cool spiral because:
- We start with a small line (size = 5)
- Each time through the loop, we make the line a bit longer
- We keep going until the line would be 100 or bigger

## Cool Patterns with Loops

### Star Pattern
```python
import turtle

my_turtle = turtle.Turtle()
my_turtle.speed(10)
my_turtle.pencolor("gold")

for i in range(5):
    my_turtle.forward(100)
    my_turtle.right(144)  # The magic angle for a 5-pointed star!

turtle.done()
```

### Colorful Spiral
```python
import turtle

my_turtle = turtle.Turtle()
my_turtle.speed(10)
colors = ["red", "blue", "green", "purple", "orange"]

for i in range(100):
    my_turtle.pencolor(colors[i % 5])  # Cycle through colors
    my_turtle.forward(i * 2)
    my_turtle.left(91)

turtle.done()
```

### Flower Pattern
```python
import turtle

my_turtle = turtle.Turtle()
my_turtle.speed(10)

def draw_petal():
    for i in range(2):
        my_turtle.circle(50, 90)
        my_turtle.left(90)

# Draw 8 petals
for i in range(8):
    draw_petal()
    my_turtle.left(45)

turtle.done()
```

## Loop Control: Break and Continue

Sometimes you want to exit a loop early or skip parts:

### Break (Exit the Loop)
```python
import turtle

my_turtle = turtle.Turtle()

for i in range(1000):  # This could go forever...
    my_turtle.forward(10)
    my_turtle.left(10)
    if i > 100:  # But we'll stop after 100 steps
        break

turtle.done()
```

### Continue (Skip to Next Loop)
```python
import turtle

my_turtle = turtle.Turtle()

for i in range(10):
    if i == 5:  # Skip drawing when i equals 5
        continue
    my_turtle.forward(20)
    my_turtle.left(36)

turtle.done()
```

## Challenge Projects

### Project 1: House Drawing Function
Create a function that draws a house with:
- A square base
- A triangular roof
- A door and windows
- Use loops where possible!

### Project 2: Geometric Art
Create a program that:
- Draws multiple shapes in different colors
- Uses both for and while loops
- Creates an interesting pattern

### Project 3: Interactive Drawing
Create a program that:
- Asks the user what shape they want
- Asks for the size and color
- Uses if statements and functions to draw their choice

**Starter code:**
```python
import turtle

my_turtle = turtle.Turtle()

def draw_polygon(sides, size):
    angle = 360 / sides
    for i in range(sides):
        my_turtle.forward(size)
        my_turtle.left(angle)

# Get user input
shape = input("What shape? (triangle, square, pentagon): ")
size = int(input("What size? "))
color = input("What color? ")

my_turtle.pencolor(color)

if shape == "triangle":
    draw_polygon(3, size)
elif shape == "square":
    draw_polygon(4, size)
elif shape == "pentagon":
    draw_polygon(5, size)

turtle.done()
```

## Cool Turtle Tricks

### Speed Control
```python
my_turtle.speed(1)   # Slowest
my_turtle.speed(10)  # Fastest
my_turtle.speed(0)   # Instant (no animation)
```

### Filling Shapes
```python
my_turtle.fillcolor("lightblue")
my_turtle.begin_fill()
# Draw your shape here
my_turtle.end_fill()
```

### Moving Without Drawing
```python
my_turtle.penup()
my_turtle.goto(100, 100)  # Move to specific coordinates
my_turtle.pendown()
```

## Why Loops Are Game Changers

Loops let you:
- **Write less code:** 4 lines instead of 16 for a square
- **Create complex patterns:** Spirals, flowers, fractals
- **Handle repetitive tasks:** Drawing 100 shapes without going crazy
- **Make interactive programs:** Keep asking for input until they're done

## Common Mistakes (Don't Worry, We All Make These!)

**"My turtle draws weird shapes"**
- Check your angles - remember 360/sides for regular polygons
- Make sure you're turning the right direction (left vs right)

**"My loop never stops"**
- In while loops, make sure the condition eventually becomes false
- Check that you're updating your counter variable

**"I can't see my drawing"**
- Make sure you have `turtle.done()` or `screen.exitonclick()` at the end
- Try making your turtle faster with `my_turtle.speed(10)`

## Next Week Preview

Next week we'll learn about lists - a way to store multiple pieces of information together. Imagine having a list of colors, names, or high scores that your program can remember and work with!

## Quick Reference

```python
import turtle

# Setup
my_turtle = turtle.Turtle()

# Movement
my_turtle.forward(distance)
my_turtle.left(angle)
my_turtle.right(angle)

# Pen control
my_turtle.penup()
my_turtle.pendown()
my_turtle.pencolor("red")

# Loops
for i in range(n):
    # repeat n times

while condition:
    # keep going until condition is false

# End program
turtle.done()
```
