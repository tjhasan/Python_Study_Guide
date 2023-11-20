# If Statements

There are 3 basic types of `if` statements: `if`, `elif`, `else`

The best way to understand the 3 is to put them into practice. Try and run the following code block:

```python
variable = 10

if variable == 10:
    print("Variable is equal to ten")
```

As you can see, the program will print out `Variable is equal to ten` because the *boolean expression* (the stuff written after and on the same line as `if`) is `True`. In this case, `variable` *is* equal to 10.

Let's see what happens if the boolean expression is false:

```python
variable = 9

if variable == 10:
    print("Variable is equal to ten")
```

You'll see that nothing prints out. This is because the boolean expression resulted in false.

But what if you want to do something if the first boolean expression is false? This is where the `else` comes into play:

```python
variable = 9

if variable == 10:
    print("Variable is equal to ten")
else:
    print("Variable is not ten")
```

If you run the above code block, you will see that the `else` condition is run and not the `if`. This is because, since the if boolean expression resulted in `False`, the program immediately jumps into the `else` statement.

That's all well and good, but what do we do in a situation where, if the first condition is `False`, we want to check the variable against other conditions before going to the `else` statement? That is where the `elif` statement comes in.

`elif` is shorthand for `else if`. You can have as many `elif` statements, after an associated `if` statement, as you want. It is used in the following scenarios:

```python
variable = 9

if variable == 10:
    print("Variable is equal to ten")
elif variable == 8:
    print("Variable is eight")
elif variable == 9:
    print("Variable is nine")
elif variable == 7:
    print("Variable is seven")
```

Running the above code block will print the 2nd `elif` statement. Notice that this code block does not contain an `else` statement, but we can add one if you want to. 

Keep in mind that an `if` and `elif` statements due **NOT** require to have an associated `else` statement. But **EVERY** `else` statement **MUST HAVE** an associated `if` or `elif` statement preceeding it.

## if VS elif

A common beginner question is in regards to using multiple `if` statements vs multiple `elif` statements. Specifically what the difference is and which is more appropriate to use. 

The difference between multiple `if` statements and multiple `elif` statements is that all subsequent `if` statements will be always be checked, whereas subsequent `elif` statements will be ignored once **exactly one** condition is true.

Take for example, the following 2 code blocks. We are trying to assign a letter grade given a number grade.

```python
number_grade = 96

if number_grade >= 90:
    print("Letter Grade: A")
if number_grade >= 80:
    print("Letter Grade: B")
if number_grade >= 70:
    print("Letter Grade: C")
if number_grade >= 60:
    print("Letter Grade: D")
else:
    print("Letter Grade: F")
```

```python
number_grade = 96

if number_grade >= 90:
    print("Letter Grade: A")
elif number_grade >= 80:
    print("Letter Grade: B")
elif number_grade >= 70:
    print("Letter Grade: C")
elif number_grade >= 60:
    print("Letter Grade: D")
else:
    print("Letter Grade: F")
```

Try running both blocks of code and see what the output looks like!

The first block of code will output:

```bash
Letter Grade: A
Letter Grade: B
Letter Grade: C
Letter Grade: D
```

The second block of code will output:
```bash
Letter Grade: A
```

The reason why they are different is because in the first code block, even after the first `if` statement is deemed `True`, every other `if` statement still has to be checked.

In the second code block, the subsequent `elif` and `else` statements are ignored as soon as a single boolean expression is deemed `True`.

Please note that this does not mean the `elif` method is better than the `if` method. Sometimes, it might be necessary to run multiple `if` statements on a single variable. It all just depends on the context of the problem you are trying to solve.

## Comparison Operators

The following symbols can be used to compare different variables to create boolean expressions:

| Syntax      | Description |
| ----------- | ----------- |
| `==` | Equal to |
| `!=` | Text |
| `<` | Less than |
| `>` | Greater than |
| `>=` | Less than or equal to |
| `<=` | Greater than or equal to |

Examples:

```python
variable_one = 10
variable_two = 30

if variable_one == 10:
    print("variable_one is equal to 10")

if variable_two != 10:
    print("variable_two is not equal to 10")

if variable_one < variable_two:
    print("variable_one is less than variable two")

if variable_two > variable_one:
    print("variable_two is greater than variable one")

if variable_one >= 10:
    print("variable_one is greater than or equal to 10")

if variable_one <= 10:
    print("variable_one is less than or equal to 10")
```

The following keywords can be used to check multiple things at the same time:

| Syntax      | Description |
| ----------- | ----------- |
| `is` | See if the variable is of some type |
| `is not` | See if a variable is NOT of some type |
| `and` | Check two boolean expressions at once. They both must equal `True` |
| `or` | Check two boolean expressions at once. Either must be `True` |

Examples:

```python
variable_one = 10
variable_two = 30

if type(variable_one) is int:
    print("variable_one is an int")

if type("this is a string") is not int:
    print("This varialbe is not an int")

if variable_one == 10 and variable_two == 10:
    print("This will not print because both variables are not equal to 10")

if variable_one == 10 or variable_two == 10:
    print("One of these variables is equal to 10")

```