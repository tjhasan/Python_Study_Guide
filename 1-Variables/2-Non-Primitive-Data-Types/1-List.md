# Lists

Lists are a data structure that hold one or more primitive and / or Non-primitive data types. 

The things inside a list are referred to as `items` and each element can be accessed via an integer called the `index`.

List index's start from `0` and go up to the number of items in the list `-1`. This is often referred as `n - 1` where `n` is the number of items in the list.

## Creating Lists

```python
first_list = []
second_list = [1,2,3,4]
third_list = [[1,2,3], "Test", 1234.456, [1,[2,[3,4], 5], 6], 7]
```

Notice that the items in a list can be literally any combination of any data types.

## Adding & Accessing Items in a List

You don't have to populate a list with items immediately. You can add to lists using the `.append()` method.

```python
first_list = []

first_list.append("first")
first_list.append("second")
first_list.append("third")
first_list.append("fourth")

print(first_list) # -> ['first', 'second', 'third', 'fourth']
```

The items in a list can be accessed using its index. 

```python
first_list = ['first', 'second', 'third', 'fourth']

print(first_list[0]) # -> 'first'
print(first_list[1]) # -> 'second'
print(first_list[2]) # -> 'third'
print(first_list[3]) # -> 'fourth'
```

Notice that the first index is 0, and the last index is 1 less than the total number of items in the list.

You can get the total length of the list using the `len()` method.

```python
first_list = ['first', 'second', 'third', 'fourth']

print(len(first_list)) # -> 4

print(first_list[len(first_list)]) # -> IndexError: List index out of range

print(first_list[len(first_list) - 1]) # -> fourth
```

Notice how *not* doing `-1` results in an `IndexError`. This is because the length of the list is 4, but the last index is 3. 

## Changing List Items:

The items within a list can be changed by simply assigning the given index with a new value.

```python
first_list = ['first', 'second', 'third', 'fourth']

print(first_list[2]) # -> third

first_list[2] = "Replacement!!"

print(first_list[2]) # -> Replacement
```

## Practical Use of a List

Lists are usually used alongside `for each` or `while` loops, which is out of the scope of this section.