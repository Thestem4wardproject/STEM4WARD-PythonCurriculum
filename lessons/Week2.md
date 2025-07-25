# Week 2: Making Your Programs Interactive 💬

Last week you learned how to make Python print things. This week, we're going to make your programs way cooler by letting them talk back to you!

## Getting Input from Users

Remember how you could only make Python say the same thing every time? That's about to change. Meet the `input()` function - it lets your program ask questions and wait for answers.

Try this:

```python
input("What's your name? ")
```

Cool, right? But there's a problem - Python asks the question and then... forgets your answer. That's where variables come in!

## Variables: Python's Memory

Think of variables like labeled boxes where Python can store information. Once you put something in a variable, Python remembers it until you change it or your program ends.

Here's how to create a variable:

```python
name = input("What's your name? ")
print("Hello " + name + "!")
```

The `=` sign doesn't mean "equals" like in math. It means "store this value in this variable." So `name = input("What's your name? ")` means "ask for the user's name and store their answer in a box labeled 'name'."

**Try this:** Create a program that asks for your favorite color and then tells you something cool about that color.

## Different Types of Information

Python is pretty smart about different types of information. Let's learn about the three main types:

### Strings (Text)
Anything in quotes is a string - letters, numbers, symbols, whatever:
```python
favorite_food = "pizza"
funny_sound = "meow123!"
```

### Integers (Whole Numbers)
These are regular counting numbers:
```python
age = 13
dogs_in_neighborhood = 7
```

### Floats (Decimal Numbers)
Numbers with decimal points:
```python
height = 5.2
temperature = 98.6
```

## The input() Trick

Here's something important: `input()` ALWAYS gives you back a string, even if someone types a number.

Try this and see what happens:

```python
age = input("How old are you? ")
next_year = age + 1
print("Next year you'll be " + next_year)
```

Did you get an error? That's because Python can't add a string (like "13") to a number (like 1). They're different types!

## Converting Types

Don't worry - Python has tools to fix this. You can convert between types:

```python
age = input("How old are you? ")
age_number = int(age)  # Convert string to integer
next_year = age_number + 1
print("Next year you'll be " + str(next_year))  # Convert back to string for printing
```

Or you can do it all in one line:

```python
age = int(input("How old are you? "))
next_year = age + 1
print("Next year you'll be " + str(next_year))
```

**The conversion functions:**
- `int()` - converts to whole numbers
- `float()` - converts to decimal numbers  
- `str()` - converts to text

## Making Dynamic Messages

Now you can create programs that feel personal! Instead of printing the same thing every time, you can use variables to make custom messages:

```python
name = input("What's your name? ")
hobby = input("What's your favorite hobby? ")
print(name + " loves " + hobby + "!")
```

You can also use variables in math:

```python
favorite_number = int(input("What's your favorite number? "))
doubled = favorite_number * 2
print("Your number doubled is " + str(doubled))
```

## Practice Challenge: Personal Calculator

Create a program that:
1. Asks for your name
2. Asks for two numbers
3. Adds those numbers together
4. Tells you the result using your name

**Example run:**
```
What's your name? Sarah
Give me a number: 15
Give me another number: 7
Hey Sarah, 15 + 7 = 22!
```

**Bonus challenges:**
- Make it do subtraction, multiplication, or division too
- Ask for their age and tell them how old they'll be in 10 years
- Ask for the number of pets they have and tell them something fun about it

## Common Mistakes (Don't Worry, Everyone Makes These!)

**"I can't add my numbers!"**
- Remember: `input()` gives you strings, use `int()` to convert them

**"I get weird error messages"**
- Check if you're trying to add strings and numbers together
- Make sure you have quotes around text: `"hello"` not `hello`

**"My variable disappeared"** 
- Variables only exist inside your program - when it ends, they're gone
- Make sure you spelled the variable name exactly the same way

## Why Variables Are Awesome

Variables make your code:
- **Reusable:** You can use the same value multiple times
- **Readable:** `name` is clearer than `"Sarah"` scattered everywhere
- **Flexible:** Change one variable and it updates everywhere

## What's Coming Next Week?

Next week we'll learn about making decisions in your code - teaching Python to choose different paths based on what the user tells it. Get ready for `if` statements!

## Quick Reference

```python
# Getting input
name = input("Question here: ")

# Converting types
number = int(input("Enter a number: "))
decimal = float(input("Enter a decimal: "))
text = str(42)  # Turns number into text

# Using variables
print("Hello " + name)
result = number + 5
```
