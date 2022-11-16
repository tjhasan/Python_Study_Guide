# Python Study Guide

Use this repository as a guide as you learn Python.

This Study guide is broken up into different directories, which each directory being a seperate topic in Python.

Each directory will also have coding challenges related to the given topic which you can copy and paste to complete on your IDE. 


## Before You Begin

If you do not have Python or VS Code installed, follow the instructions shown in [this](https://code.visualstudio.com/docs/python/python-tutorial) website. You only need to follow the instructions **up to and including** “Configure and Run Debugger”. You can ignore everything else after that point. 

After you've got everything working feel free to start the subjects in this repo.

## Absolute Basics

### Variable Assigment

To create a variable, use the following syntax: `<var-name> = <value>`. This is knows as "assignment" and it holds for every single kind of variable in Python.

Variables can be assigned to other variables, and (most) can be adjusted after assignment, and can be reassigned with no issues.

```python
variable_one = 0

variable_two = variable_one

variable_one = variable_one + 1

variable_one += 1

variable_two = 9999
```

### Printing

To print a value to the screen, use the following syntax: `print(<value>)`. You can print hardcoded strings or a variable:

```python
print("Test print")

qwerty = "Example"

print(qwerty)

number_example = 9998899

print(number_example)
```

### Commenting

To create a comment in your code, simply type `# ` before your comment:

```python
# This is a comment
print("This statement is not affected by the comment")
```
Comments are ignored by the compiler and do not actually do anything in your code. They are exclusively used for documentation or personal notes.
