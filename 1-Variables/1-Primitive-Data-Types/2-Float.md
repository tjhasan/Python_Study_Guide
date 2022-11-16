# Floats

Referred to as `floating point numbers` in practice. Literally a positive or negative **decimal** number.

## Creating Floats

```python
first_number = 99999.0
second_number = 123.456
third_number = 0.0
```

## Using Floatss

Floats can be added and subtracted from each other using basic math symbols:

```python
first_number = 10.5
second_number = 3.8

result_one = first_number + second_number
result_two = first_number - second_number
result_three = first_number * second_number
result_four = first_number / second_number
result_five = first_number // second_number

print(result_one) # -> 14.3
print(result_two) # -> 6.7
print(result_three) # -> 39.9
print(result_four) # -> 2.763157894736842
print(result_five) # -> 2.0
```

Notice that using `/` and `//` give different results. This is because sometimes you may want the resulting decimal and sometimes you may want to ignore them. This is just a choice you can make while coding depending on your situation. 

You can do multiple math operations at once and use parentheses to enforce order of operations:

```python
first_number = 10.5
second_number = 3.8

result_one = first_number + second_number * 3 * 4
result_two = (first_number + second_number) * (3 * 4)

print(result_one) # -> 56.099999999999994
print(result_two) # -> 171.60000000000002
```

## Converting Float -> Integer

The relationship between floats and integers can be annoying if you don't understand how to handle both at once.

If you do math on **two floating point numbers**, the result will be a floating point number, even if the result has nothing after the decimal.

```python
first_number = 10.0
second_number = 2.0

result_one = first_number + second_number 

print(result_one) # -> 12.0
```

If you do math on **One floating point number and one int**, the result will be a floating point number. This is the one that usually causes trouble for people starting out. 

```python
first_number = 10.0
second_number = 2

result_one = first_number + second_number 

print(result_one) # -> 12.0
```

If you ever do math that would result in a float, but you *need* it to be an integer, you can use integer casting like so:

```python
first_number = 10.0
second_number = 2

result_one = int(first_number + second_number)

print(result_one) # -> 12
```

The opposite can also be done, but it's very rarely used.

```python
first_number = 10
second_number = 2

result_one = float(first_number + second_number)

print(result_one) # -> 12.0
```