# Breaks and Continues

Now that we know how for loops work, let's talk about how we would go about ending a for loop prematurely. 

Let's take for instance the following problem statement: Given a list of numbers, print all numbers until you find a number that is equal to 175. Then, end the program. 

To solve this problem we would use a break statement:

```python
numbers = [3, 4, 66, 7234, 623452345, 7878, 456, 175, 1, 3, 5, 62346, 6, 234]

for number in numbers: 
    print(number)
    if i == 175:
        break
```
What the break statement does here is that it "breaks" out of the loop as soon as the if condition becomes true. 

Now let's take for instance a different problem statement: Given a list of numbers, print all numbers EXCEPT even numbers.

We would solve this using a `continue` statement:

```python
numbers = [3, 4, 66, 7234, 623452345, 7878, 456, 175, 1, 3, 5, 62346, 6, 234]

for number in numbers: 
    if number % 2 == 0:
        continue
    print(number)
```
What `continue` does is it forces the for loop to move onto it's next iteration without executing the rest of the code. So in this case, if the current number is evenly divisible by 2 (it's even), then nothing is printed and we move onto the next number in the list. If the number is NOT divisible by 2, then it prints the number as normal.

The `continue` and `break` tools are useful in many cases. Keep in mind though that there are always multiple ways to solve a problem. For example, in the last example we could have also written this with the exact same result:

```python
numbers = [3, 4, 66, 7234, 623452345, 7878, 456, 175, 1, 3, 5, 62346, 6, 234]

for number in numbers: 
    if number % 2 != 0:
        print(number)
```

It's all about how you approach a problem and knowing what tools you have to solve it!