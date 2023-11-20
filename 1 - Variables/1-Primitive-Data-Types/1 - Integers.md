# Integers

Referred to as `int`s in practice. Literally a positive or negative **whole** number (no decimals).

## Creating Integers

```python
first_number = 99999
second_number = -9923
third_number = 0
```

## Using Integers

Integers can be added and subtracted from each other using basic math symbols:

```python
first_number = 10
second_number = 5

result_one = first_number + second_number
result_two = first_number - second_number
result_three = first_number * second_number
result_four = first_number / second_number
result_five = first_number // second_number

print(result_one) # -> 15
print(result_two) # -> 5
print(result_three) # -> 50
print(result_four) # -> 2.0
print(result_five) # -> 2
```

Notice that using `/` and `//` give different results. This is because sometimes you may want the resulting decimal and sometimes you may want to ignore them. This is just a choice you can make while coding depending on your situation. 

You can do multiple math operations at once and use parentheses to enforce order of operations:

```python
first_number = 10
second_number = 5

result_one = first_number + second_number * 3 * 4
result_two = (first_number + second_number) * (3 * 4)

print(result_one) # -> 70
print(result_two) # -> 180
```