# Tuples

Tuples are similar to lists, except the values within a Tuples cannot be adjusted after they are assigned.

## Creating Tuples

Tuples are created in a similar way as lists, except you replace `[]` with `()`.

```python
first_tuple = ('first', 'second', 'third', 'fourth')

print(first_tuple) # -> ('first', 'second', 'third', 'fourth')
```

You can also create a Tuple with only one item, but you need to add a trailing `,`. Otherwise it will not become a Tuple.

```python
first_tuple = ('first',)
not_a_tuple = ('first')

print(first_tuple) # -> ('first',)
print(not_a_tuple) # -> first
```

## Adding & Accessing Items in a Tuple

You can add to a tuple by simply using the `+` symbol with another tuple.

```python
first_tuple = ('first',)
second_tuple = ('second', 'third', 'fourth')
print(first_tuple) # -> ('first',)

first_tuple += second_tuple
print(first_tuple) # -> ('first', 'second', 'third', 'fourth')
```

You can access the items in a tuple in two ways. The first is simply via indexing, the same way as lists. The second is via 'unpacking'


First method: Indexing
```python
first_tuple = ('first', 'second', 'third', 'fourth')
print(first_tuple[0]) # -> first
print(first_tuple[3]) # -> fourth
```

Second method: Unpacking
```python
first_tuple = (10, -45, 'last item')

first_item, second_item, third_item = first_tuple

print(first_item) # -> 10
print(second_item) # -> -45
print(third_item) # -> last item
```

## Practical Use of Tuples

The main use of Tuples is as a method's return type. 

"What is a method" and "what is a return type" are both questions that are out of the scope of this section. 