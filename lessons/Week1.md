# Week 1: Introduction to Python and Basic Syntax

## What is Python?

Python is a high-level programming language used to write instructions that a computer can understand. It is widely used because it is:

- Easy to read and write
- Beginner-friendly
- Used in many areas such as web development, automation, AI, and data science

In this course, we will use Python to learn how to think like a programmer and solve problems with code.

---

## Using Replit to Write Python

In this tutorial, we will use [Replit](https://replit.com), an online tool that lets you write and run Python code in your browser.

### How to Start a Python Repl

1. Go to [https://replit.com](https://replit.com)
2. Click on **+ Create Repl**
3. Select **Python**
4. Name your project (e.g., `week1-intro`)
5. Click **Create Repl**

You’re now ready to begin writing Python code.

---

## Printing Text with `print()`

To display something on the screen, we use the `print()` function.

```python
print("Hello, world!")
```

When you run this code, it will show:

Copy
Edit
Hello, world!
You can also print numbers or math expressions:

```
print(2 + 3)
print("Python version", 3.11)
```

Basic Math in Python
Python can be used as a calculator. Try the following expressions:


```
print(5 + 2)    # Addition
print(8 - 3)    # Subtraction
print(4 * 6)    # Multiplication
print(9 / 2)    # Division (with decimals)
print(9 // 2)   # Integer division (no decimals)
print(10 % 3)   # Modulo (remainder)
```

Writing Comments
Comments are notes you write in your code to explain what it does. Python ignores them when the code runs. Comments start with a # symbol.

```
# This is a comment
print("This will show up")
# print("This line will not run")
```
Use comments to explain what your code is doing.

Understanding Syntax
Syntax is the set of rules for how code must be written in Python.

Indentation
Python uses indentation (spaces or tabs at the beginning of lines) to group code blocks. For example:

```
if True:
    print("This line is indented correctly")
```
If you don’t indent properly, Python will give you an error.

Case Sensitivity
Python treats lowercase and uppercase letters as different. These two lines are not the same:

```
print("OK")   # This works
Print("OK")   # This gives an error
```

How Python Runs Code
Python reads your code from top to bottom, one line at a time.

Try:
```
print("Line 1")
print("Line 2")
print("Line 3")
```
Output:

scss
Copy
Edit
Line 1
Line 2
Line 3
This is called sequential execution.

Try It Yourself
In your own Replit project, try writing the following programs.

Print your name
python
Copy
Edit
print("My name is Alice")
Print a fun fact
python
Copy
Edit
print("I love cats and coding!")
Do some math
python
Copy
Edit
print("8 times 7 is", 8 * 7)
Create an error on purpose
python
Copy
Edit
Print("This will cause an error")
Challenges
Try solving these simple problems using what you’ve learned.

Challenge 1: Silly Joke
python
Copy
Edit
print("Why did the Python developer go broke?")
print("Because he used up all his cache!")
Challenge 2: Simple Calculator
python
Copy
Edit
print("2 + 2 =", 2 + 2)
print("9 // 4 =", 9 // 4)
print("10 % 4 =", 10 % 4)
Challenge 3: Use Comments
python
Copy
Edit
# This is a fun fact
print("Space is completely silent.")
Summary
This week you learned:

What Python is used for

How to use Replit to run Python code

How to use print() to show text and numbers

How to do basic math in Python

How to write comments

Why indentation and correct syntax matter
