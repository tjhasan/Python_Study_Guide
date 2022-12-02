# Strings

Literally a word or phrase.

## Creating Strings

```python
first_string = "Test"
second_string = 'ing'
```
Note that using `''` or `""` doesn't make a difference.

## Using Strings

Strings can be concatenated to each other using the `+` symbol:

```python
first_string = "Test"
second_string = 'ing'

result_one = first_string + second_string
result_two = first_string + "ing with hardcoded string"

print(result_one) # -> Testing
print(result_two) # -> Testing with hardcoded string
```

Strings can also contain numbers, so long as they are enclosed using `""`

```python
foo = "123"
```

If a string has **only** a number, then you can cast that string into an integer or float.

```python
foo = "123"
bar = "123.456"

int_variable = int(foo)
float_variable = float(bar)

print(int_variable) # -> 123
print(float_variable) # -> 123.456
```

Strings are very closely tied with `Lists`. You will see why once you get to the `Lists` section of this lesson.
