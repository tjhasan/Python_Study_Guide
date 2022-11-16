# Booleans

Called `bools` in practice. Literally a `True` or `False` value, or an expression which can be True or False.

## Creating Bools

```python
first_bool = True
second_bool = False

print(first_bool) # -> True
print(second_bool) # -> False
```

## Using Bools

Bools are usually not hardcoded like you see above. Instead, bools are used via "boolean expressions". There are math expressions which can either be true or false. 

For example:

```python
number1 = 10
number2 = 5

print(number1 > number2) # -> True
print(number1 < number2) # -> False
print(number1 == number2) # -> False
```
Notice that to compare two things for equality, you use `==`. This is because `=` is used for assignments.

```python
string1 = "Test"
string2 = "test"

print(string1 == string2) # -> False
print(string1 != string2) # -> True
```
Notice that strings are **case-sensitive**. However this can be subverted which we will see in a later section.

```python
number1 = 1
float1 = 1.0

print(number1 > float1) # -> False
print(number1 < float1) # -> False
print(number1 == float1) # -> True
```
Notice that although they are different types (floats vs ints), they are still considered equal.

It's hard to talk about bools without also talking about conditional statements. However, that is a whole topic on its own so for now just keep this in mind and move on.