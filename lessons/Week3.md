# Week 3: Making Decisions and Building Functions 🎯

This week is where programming gets really exciting! You're going to teach your programs how to make decisions and create your own custom commands.

## Teaching Python to Make Decisions

Right now, your programs do the same thing every time. But what if you want Python to do different things based on what the user says? That's where `if` statements come in!

### Your First If Statement

```python
age = int(input("How old are you? "))

if age >= 13:
    print("You're a teenager!")
```

The `if` statement checks if something is true. If it is, Python runs the code underneath (notice how it's indented!). If not, Python skips it.

### Comparison Operators (How Python Compares Things)

Python uses special symbols to compare values:
- `==` means "exactly equal to" (not just one `=`!)
- `!=` means "not equal to"
- `>` means "greater than"
- `<` means "less than"
- `>=` means "greater than or equal to"
- `<=` means "less than or equal to"

**Try this:**
```python
favorite_number = int(input("What's your favorite number? "))

if favorite_number == 7:
    print("Seven is my favorite too!")
```

### Adding More Choices with elif and else

What if you want multiple options? Use `elif` (which means "else if") and `else`:

```python
weather = input("What's the weather like? ")

if weather == "sunny":
    print("Perfect day for the park!")
elif weather == "rainy":
    print("Good day to stay inside and code!")
else:
    print("Sounds like an interesting day!")
```

**The Rules:**
- You can have as many `elif` statements as you want
- `else` is optional and always comes last
- Python checks them in order and stops at the first true one

### Combining Conditions

You can check multiple things at once using `and` and `or`:

```python
age = int(input("How old are you? "))
grade = input("What grade are you in? ")

if age >= 13 and grade == "8th":
    print("You're probably in middle school!")

if age < 10 or age > 18:
    print("You're either really young or getting old!")
```

## Practice: Choose Your Own Adventure

Let's build a mini adventure game:

```python
print("You're walking through a forest and see two paths.")
choice = input("Do you go left or right? ")

if choice == "left":
    print("You find a friendly dragon who gives you gold!")
elif choice == "right":
    print("You discover a hidden cave full of crystals!")
else:
    print("You stand there confused and a squirrel laughs at you.")
```

**Your challenge:** Expand this story! Add more choices, more `if` statements, and make it longer.

## Functions: Creating Your Own Commands

You know how `print()` and `input()` are commands that do specific things? You can create your own commands called functions!

### Your First Function

```python
def say_hello():
    print("Hello there!")
    print("Welcome to my program!")

# To use your function, you "call" it:
say_hello()
```

The `def` keyword tells Python "I'm creating a new function." Everything indented underneath is part of that function.

### Functions with Parameters (Giving Functions Information)

Functions become way more useful when you can give them information:

```python
def greet_person(name):
    print("Hello " + name + "!")
    print("Hope you're having a great day!")

# Now you can use it with different names:
greet_person("Alex")
greet_person("Sam")
```

You can give functions multiple pieces of information:

```python
def introduce_person(name, age, hobby):
    print("This is " + name)
    print("They are " + str(age) + " years old")
    print("They love " + hobby)

introduce_person("Maya", 13, "skateboarding")
```

### Functions That Give Back Answers (Return Values)

Sometimes you want a function to calculate something and give you back the answer:

```python
def add_numbers(num1, num2):
    result = num1 + num2
    return result

# Now you can use the answer:
answer = add_numbers(5, 3)
print("The sum is " + str(answer))

# Or use it directly:
print("10 + 7 = " + str(add_numbers(10, 7)))
```

### Combining Functions and If Statements

Here's where it gets really cool - you can put if statements inside functions:

```python
def check_password(password):
    if password == "python123":
        return "Access granted!"
    else:
        return "Access denied!"

user_password = input("Enter password: ")
result = check_password(user_password)
print(result)
```

## Scope: Where Variables Live

Here's something important: variables inside functions stay inside functions (unless you return them):

```python
def my_function():
    secret = "This is hidden!"
    print(secret)

my_function()  # This works
print(secret)  # This will cause an error!
```

Think of functions like separate rooms - what happens in the function room stays in the function room.

## Practice Project: Personal Assistant

Create a program with these functions:

1. **A greeting function** that asks for the user's name and welcomes them
2. **A calculator function** that takes two numbers and an operation (+, -, *, /)
3. **A decision helper** that helps them choose what to do based on the weather

**Example structure:**
```python
def greet_user():
    name = input("What's your name? ")
    print("Hello " + name + "! I'm your personal assistant.")
    return name

def simple_calculator():
    # Your calculator code here
    pass

def weather_advisor():
    # Your weather advice code here
    pass

# Main program:
user_name = greet_user()
# Add calls to your other functions here
```

## Why Functions Are Amazing

Functions help you:
- **Avoid repetition:** Write code once, use it many times
- **Stay organized:** Break big problems into smaller pieces
- **Fix bugs easier:** If something's wrong, you know exactly where to look
- **Work with others:** Functions make it easy to share code

## Common Mistakes (And How to Fix Them)

**"My if statement never works!"**
- Remember: use `==` to compare, not `=`
- Check your spelling exactly: `"yes"` is different from `"Yes"`

**"My function doesn't do anything"**
- Make sure you're calling it: `my_function()` not just `my_function`
- Check your indentation - everything in the function should be indented

**"I get an error about variables"**
- Variables created inside functions can't be used outside them
- Use `return` to get values out of functions

## Next Week Preview

Next week we'll learn about loops - how to make Python do things over and over again without writing the same code 100 times. Get ready to build some seriously cool programs!

## Quick Reference

```python
# If statements
if condition:
    # do this
elif other_condition:
    # do this instead
else:
    # do this if nothing else was true

# Functions
def my_function(parameter):
    # do something
    return result

# Calling functions
answer = my_function("some value")
```
