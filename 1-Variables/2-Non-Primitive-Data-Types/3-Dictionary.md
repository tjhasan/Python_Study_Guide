# Dictionary

Dictionaries are a collection of key - value pairs. The keys are required to be unique, but the values can be anything. Additionally the keys can be any **Primitive** data type. 

## Creating A Dictionary

Create a dictionary using {} after the `=` and use the format `<key> : <value>,`

```python
first_dict = {
    'first_key' : 1000,
    'second_key' : "12341234",
    'third_key' : 1234.33431234,
    'fourth_key' : True,
    'fifth_key' : [1,2,3,4,5]
}
```

## Adding & Accessing Items in a Dictionary

Dictionaries can also be created empty, and the keys and values can be added later on using the following syntax:

```python
first_dict = {}

first_dict['Test'] = 100
first_dict['Test2'] = 200
first_dict['Test3'] = 300

print(first_dict) # -> {'Test': 100, 'Test2': 200, 'Test3': 300}
```
In order to add to a dictionary, you must provide a unique key. Otherwise the old value for that key will be replaced.

When adding to a dictionary, a value must be given or else you will receive an error.

```python
first_dict = {}

first_dict['Test'] = 100
first_dict['Test'] = 200
first_dict['Test3'] = 300

print(first_dict) # -> {'Test': 200, 'Test3': 300}

first_dict['Test4'] # -> KeyError

```

Notice how the `Test` Key's value is overwritten due to the second assignment.

Also Notice how trying to add a new, unqiue key to the dictionary without a value results in a KeyError.

## Practical Use of Dictionary

Dictionaries are used for mapping items which make sense to pair together. For example, a student's name and their information:

```python
# first_dict contains a Student and their corresponding: 
#       [overall grade, homeroom, studentID number, expulsion status]

first_dict = {
    "John Smith": ['A+', 'Room 123', 89213, True],
    "Tyler Perry": ['F', 'Room 443', 12332, False],
    "Ali Jones": ['B', 'Room 322', 78890, False]
}
```
In the above example, each students name correspondes to their personal information. Therefore, it makes sense to organize it all in a dictionary since the pairing comes out naturally.
```