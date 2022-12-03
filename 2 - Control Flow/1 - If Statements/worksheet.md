# Instructions

Copy and paste the following blocks of code **SEPARATELY** into your own `.py` file. 

Read the instructions for each question carefully before you begin typing your code.

Write your code into the place with the comment `# YOUR CODE HERE!!!`. Ignore everything else. 

If you programmed it correctly, you should see a **"YOU PASSED!"** message appear in your terminal. 

# Question 1
```python

'''
You will be given any number between 0 and 100.

Your job is to create a program that will take this number and assign it a letter grade.

Use the following rubric to assign grades:

Anything greater than or equal to 90 is an A

Anything between 89 and 80 (inclusive) is a B

Anything between 79 and 71 (inclusive) is a C

Anything that is exactly 70 is a D

Anything less than or equal to 60 (inclusive) is F

For example, if the number_grade given to the code is 72, then the "letter_grade" 
variable should be changed to "C"
'''
def Grade_Assignment(number_grade: int) -> str:
    letter_grade = ""
    # YOUR CODE HERE!!!

    return letter_grade



########################################################################
################ Ignore everything past this comment!!! ################
########################################################################

q_and_a = {
    90: "A",
    89: "B",
    80: "B",
    79: "C",
    71: "C",
    70: "D",
    60: "F",
    100: "A",
    23: "F",
    77: "C",
    54: "F",
}

i = 0
passed = 0
for number, expected in q_and_a.items():
    i += 1
    result = Grade_Assignment(number)

    if result == "":
        print("You've returned an empty string. Remember to reassign the 'letter_grade' variable with '=' ")

    elif result != expected:
        print("Number grade: " + q_and_a.keys()[i])
        print("Expected Grade: " + expected)
        print("Grade given by code: " + result)
        print("TEST CASE " + str(i) + "FAILED! \n")
    
    elif result == expected:
        passed += 1
        print("TEST CASE " + str(i) + " PASSED!! \n")

if passed == len(q_and_a):
    print("YOU PASSED!. Nice job!")
else:
    print("Failed one or more test cases. Adjust code and try again.")
```

# Question 2
```python

'''
You will be given two strings.

Write code that will be able to decide if the two strings are of equal length or not

For example, the strings "car" and "bed" are of equal length. Therefore, the program 
should return True.

The strings "name" and "business" are not the same length, so the program should return
False.
'''
def equal_string_length(string_one: str, string_two: str) -> bool:
    equivalency = True
    # YOUR CODE HERE!!!

    return equivalency



########################################################################
################ Ignore everything past this comment!!! ################
########################################################################

q_and_a = {
    ('', ''): True,
    ('car', 'bed'): True,
    ('asdfasdfasdfasdfasdfad', 'asdfasdfasdfasdfasdfada'): False,
    ('-1093824-0912834-0198324-0175019827341', '-1093824-0912834-0198324-0175019827341'): True,
    ('bus driver', 'bus rider'): False,
    (';lkajd;lkfjal;kdfjlakjd;lfkajklsdfj;lakjdsf;klajdfkldaj;dlfja;lkdfja;lkdjf;lakdjsf;lakdjf;laksdjf;lakjdf;lakdjf;lakdjf;alskdjf;alkdsfj;alkdjf;lkadsjfkaj;dslfkja',';lkajd;lkfjal;kdfjlakjd;lfkajklsdfj;lakjdsf;klajdfkldaj;dlfja;lkdfja;lkdjf;lakdjsf;lakdjf;laksdjf;lakjdf;lakdjf;lakdjf;alskdjf;alkdsfj;alkdjf;lkadsjfkaj;dslfkjaasdfasdf'): False,
    ('foo', 'bar'): True,
    ('Lost Ark', 'Kra tsoL'): True,
    ('', 'a'): False,
}

i = 0
passed = 0
for strings, expected in q_and_a.items():
    i += 1
    result = equal_string_length(strings[0], strings[1])

    if result != expected:
        if result is False:
            print("Got False. Expected True \n")
        else:
            print("Got True. Expected False \n")

    elif result == expected:
        passed += 1
        print("TEST CASE " + str(i) + " PASSED!! \n")

if passed == len(q_and_a):
    print("YOU PASSED! Nice job!")
else:
    print("Failed one or more test cases. Adjust code and try again.")
```

# Question 3
```python

'''
You will be given a random number (could be either positive or negative).

Create a program that can determine if the number is a divisible by 5 or 7.

If a number is divisible by 5, return the string 'Divisible by 5'

If a number is divisible by 7, return the string 'Divisible by 7'

If a number is divisible by both 5 and 7, return the string 'Divisible by 5 and 7'

If a number is not divisible by either 5 or 7, then return the string 'Void Number'


HINT: Use the modulo symbol '%' to get remainders after division. For example, 6 % 2 == 0. 3 % 2 == 1
'''
def divisibility(number: int) -> str:
    answer = ''
    # YOUR CODE HERE!!!

    return answer



########################################################################
################ Ignore everything past this comment!!! ################
########################################################################

q_and_a = {
    35: "Divisible by 5 and 7",
    25: "Divisible by 5",
    49: "Divisible by 7",
    3: "Void Number",
    105: "Divisible by 5 and 7",
    45: "Divisible by 5",
    140: "Divisible by 5 and 7",
    6: "Void Number",
    14: "Divisible by 7",
    60: "Divisible by 5",
    105: "Divisible by 5 and 7",
    9: "Void Number",
    25: "Divisible by 5",
    140: "Divisible by 5 and 7",
    700: "Divisible by 5 and 7",
}

i = 0
passed = 0
for number, expected in q_and_a.items():
    i += 1
    result = divisibility(number)

    if result != expected:
        print("Number given: " + str(number))
        print("Expected: " + expected)
        print("Code result: " + result)
        print()
    elif result == expected:
        passed += 1
        print("TEST CASE " + str(i) + " PASSED!! \n")

if passed == len(q_and_a):
    print("YOU PASSED! Nice job!")
else:
    print("Failed one or more test cases. Adjust code and try again.")
```
