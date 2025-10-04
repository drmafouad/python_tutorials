# Python Tutorial #1: Your First Python Program in 10 Minutes

## Start Your Programming Journey the Right Way

You've heard Python is the perfect language for beginners. You've seen job postings asking for Python skills. Maybe you want to automate boring tasks, analyze data, or build websites. But where do you actually start?

In this tutorial, you'll write your first Python program and understand exactly what's happening behind the scenes. No fluff, no overwhelming theory—just practical, hands-on learning.

**What you'll learn:**
- How to set up Python on your computer
- Writing and running your first program
- Understanding basic Python syntax
- Creating interactive programs with user input
- Debugging common beginner mistakes

**Time required:** 10 minutes  
**Prerequisites:** None—just curiosity and a computer

---

## Why Python?

Before we dive in, let's quickly understand why Python is dominating the programming world:

**Easy to read and write** - Python reads almost like English, making it perfect for beginners. Compare this Python code to other languages and you'll see the difference immediately.

**Versatile** - From web development to artificial intelligence, data science to automation, Python does it all.

**In-demand** - Python developers are among the highest paid, with average salaries exceeding $100,000 in many markets.

**Huge community** - Stuck on a problem? Thousands of developers are ready to help, and millions of tutorials exist online.

Now, let's write some code.

---

## Setting Up Python (5 Minutes)

### Step 1: Install Python

1. Visit [python.org/downloads](https://www.python.org/downloads)
2. Download Python 3.12 (or latest version)
3. Run the installer
4. **Important:** Check "Add Python to PATH" during installation

### Step 2: Verify Installation

Open your terminal (Command Prompt on Windows, Terminal on Mac/Linux) and type:

```bash
python --version
```

You should see something like:
```
Python 3.12.0
```

If you see this, congratulations! Python is ready to go.

**Troubleshooting:** If you get "command not found," try `python3 --version` instead. On some systems, Python 3 is called `python3`.

### Step 3: Choose Your Code Editor

For now, we'll use Python's built-in editor called IDLE (it came with your installation). Later, you can explore VS Code, PyCharm, or other professional editors.

**To open IDLE:**
- Windows: Search "IDLE" in Start menu
- Mac: Search "IDLE" in Spotlight
- Linux: Type `idle3` in terminal

---

## Your First Python Program: Hello, World!

Let's follow the time-honored tradition of programmers worldwide—writing a "Hello, World!" program.

### Open IDLE and Type This:

```python
print("Hello, World!")
```

Press **Enter**. You should see:

```
Hello, World!
```

**That's it!** You just wrote your first Python program. 

### What Just Happened?

Let's break down this single line:

- **`print()`** - A built-in Python function that displays text on screen
- **`"Hello, World!"`** - A string (text) enclosed in quotes
- When you press Enter, Python interprets your code and executes it immediately

**Try this:** Change "Hello, World!" to your name:

```python
print("Hello, Sarah!")
```

See how easy it is? You're already customizing Python code.

---

## Writing a Python Script File

So far, you've been typing directly into IDLE's interactive mode (called the Python shell). But real programs are saved as files you can run multiple times.

### Creating Your First Script

1. In IDLE, click **File → New File**
2. A new window opens—this is your script editor
3. Type the following code:

```python
# My first Python script
print("Welcome to Python programming!")
print("This is my first script.")
print("Python makes coding fun!")
```

4. Save the file: **File → Save As** → Name it `first_program.py`

### Running Your Script

Click **Run → Run Module** (or press F5).

You'll see:
```
Welcome to Python programming!
This is my first script.
Python makes coding fun!
```

**Notice the `#` symbol?** That's a comment. Python ignores everything after `#`, so you can write notes to yourself or other programmers.

### Why Use Script Files?

- **Reusable** - Run your program anytime without retyping
- **Shareable** - Send your `.py` file to others
- **Professional** - All real Python projects use script files
- **Complex** - Build programs with hundreds of lines

---

## Making It Interactive: Getting User Input

Static programs are boring. Let's make your program interactive by asking for user input.

### Example: Personalized Greeting

Create a new file and type:

```python
# Interactive greeting program
name = input("What is your name? ")
print("Hello, " + name + "!")
print("Welcome to the world of Python.")
```

**Run the program.** It will pause and wait for you to type your name. Type your name and press Enter.

**Output:**
```
What is your name? John
Hello, John!
Welcome to the world of Python.
```

### Understanding the Code

Let's examine each line:

**Line 2:** `name = input("What is your name? ")`
- **`input()`** - Function that waits for user to type something
- **`"What is your name? "`** - The prompt shown to the user
- **`name =`** - Stores whatever the user types in a variable called `name`

**Line 3:** `print("Hello, " + name + "!")`
- **`+`** - Combines (concatenates) strings together
- **`name`** - The variable containing what the user typed
- Result: "Hello, " + "John" + "!" = "Hello, John!"

**Variables are like boxes** that store information you want to use later. You can name them anything meaningful (age, email, favorite_color, etc.).

---

## Building Something Useful: A Simple Calculator

Let's create a program that actually does something useful—adding two numbers.

```python
# Simple addition calculator
print("=== Simple Calculator ===")

# Get first number
num1 = input("Enter first number: ")
# Get second number
num2 = input("Enter second number: ")

# Convert strings to integers and add them
result = int(num1) + int(num2)

# Display the result
print("The sum is:", result)
```

**Try running this program.**

**Example interaction:**
```
=== Simple Calculator ===
Enter first number: 15
Enter second number: 27
The sum is: 42
```

### New Concept: Data Types

Notice the `int()` function? Here's why it's needed:

- **`input()` always returns text (a string)**, even if you type numbers
- **You can't do math with text:** "15" + "27" = "1527" (string concatenation)
- **`int()` converts text to a number:** int("15") = 15 (the number)
- **Now math works:** 15 + 27 = 42

**Try removing `int()` and see what happens:**

```python
result = num1 + num2  # Without int()
```

You'll get "1527" instead of 42—because Python combined the strings instead of adding numbers!

---

## Common Beginner Mistakes (And How to Fix Them)

### Mistake 1: Forgetting Quotes Around Text

```python
# Wrong
print(Hello)  # Python looks for a variable named Hello

# Correct
print("Hello")  # Text must be in quotes
```

**Error you'll see:** `NameError: name 'Hello' is not defined`

### Mistake 2: Mismatched Quotes

```python
# Wrong
print("Hello World')  # Started with " but ended with '

# Correct
print("Hello World")  # Both quotes match
```

**Error you'll see:** `SyntaxError: unterminated string literal`

### Mistake 3: Forgetting Parentheses

```python
# Wrong
print "Hello"  # Missing parentheses (this worked in Python 2, not Python 3)

# Correct
print("Hello")  # Functions need parentheses
```

**Error you'll see:** `SyntaxError: Missing parentheses in call to 'print'`

### Mistake 4: Case Sensitivity

```python
name = "John"
print(Name)  # Wrong - capital N

print(name)  # Correct - lowercase n
```

Python is case-sensitive. `name` and `Name` are completely different variables.

---

## Practice Exercises

Now it's your turn! Try building these programs yourself:

### Exercise 1: Personal Introduction
Create a program that asks for:
- Your name
- Your age  
- Your favorite hobby

Then prints: "Hi [name]! You're [age] years old and you love [hobby]."

### Exercise 2: Temperature Greeter
Ask the user for the current temperature, then print:
- "It's hot outside!" if they enter a number over 80
- Just print the temperature back to them for now (we'll learn conditional logic in Tutorial #2)

### Exercise 3: Story Generator
Ask for three words: a noun, a verb, and an adjective.  
Create a silly sentence using those words.

**Example:** "The [adjective] [noun] [verb] over the moon!"

---

## What You've Learned

Let's recap what you accomplished in just 10 minutes:

✓ **Installed Python** on your computer  
✓ **Ran your first program** using `print()`  
✓ **Created script files** that can be saved and reused  
✓ **Made interactive programs** using `input()`  
✓ **Worked with variables** to store information  
✓ **Understood data types** and conversions with `int()`  
✓ **Debugged common mistakes** like syntax errors  

That's a solid foundation! You're no longer a complete beginner—you're a Python programmer who can write functional programs.

---

## Next Steps

In **Tutorial #2: Control Flow - Making Decisions in Python**, you'll learn:
- if/else statements to make your programs intelligent
- Comparison operators (>, <, ==)
- Building a number guessing game
- Creating a basic login system

### Before moving on, make sure you can:
1. Write and run a Python script file
2. Use `print()` and `input()` comfortably
3. Understand what variables are
4. Convert between strings and integers

If any of these feel unclear, that's okay! Re-read those sections and practice the exercises above.

---

## Additional Resources

**Official Python Documentation:** [docs.python.org](https://docs.python.org)  
**Practice Python Problems:** Try coding challenges on [HackerRank](https://www.hackerrank.com/domains/python) or [Codewars](https://www.codewars.com)  
**GitHub Repository:** [Link to your repo will go here]

---

## Join the Conversation

**What will you build with Python?** Drop a comment below and let me know what you're excited to learn. 

**Found this helpful?** Give it a clap (or 50!) and follow for Tutorial #2 coming [day of week].

**Questions or stuck on something?** Ask in the comments—I respond to everyone within 24 hours.

---

**Happy coding! 🐍**

*This is part of my Python Learning Series. [View all tutorials here](#)*

---

## Tags to Use
- Python
- Programming
- Learn Python
- Python Tutorial
- Python For Beginners
