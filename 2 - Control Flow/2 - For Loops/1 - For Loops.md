# For Loops

There are 2 types of `for` loops: `for` and `for each`. Both types of loops will execute a portion of code multiple times given some condition. 

For example, if you want to print “Hello” 10 times without `for` loops, you would do something like this:

```python
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
```

But if you use a `for` loop you can simply write this:
```python
for i in range(0, 10):
    print("Hello")
```

The basic syntax of a `for` loop is this: 
```python
for <variable> in <sequence>:
    <block of code>
```
The `<variable>` is a name that you can choose to refer to each element in the` <sequence>`. The `<sequence>` is a collection of values, such as a list, a range, or a string. The `<block of code>` is indented under the for loop and will be executed for each element in the sequence.

Let's break down our previous example using this syntax:
```python
for i in range(0, 10):
    print("Hello")
```

In this example, the `<variable>` is `i`. I chose `i` for no particular reason. You can literally name it anything, but ideally you want to choose a descriptive name. You'll see what I mean by that later.

The `<sequence>` is the expression `range(0, 10)`. Now you may be wondering what the `range` thing is. `range` is a special function that comes pre-installed with Python that creates a sequence of numbers given whatever numbers you input. In this case, I gave it 0 and 10, and it creates the sequence `(0, 1 ,2, 3, 4, 5, 6, 7, 8, 9).` Now you might be wondering why `10` isn't there despite me specifying it. I will explain that a bit later.

The `<block of code>` is what will be run during each the for loop for each element in the sequence. So in this example, it will print `"Hello"` 10 times to the terminal.

Putting it all together, when you see a `for` loop, think of reading it like this: `"For every number between [0, 10), print the word 'Hello'"`

Feel free to try making your own for loop and see how it all works!

## Off By 1

Take a look at the following for loop:
```python
for i in range(0, 10):
    print("i")
```

Now, if you actually run the code above, you'll notice that it only prints the numbers 0 -> 9 **NOT** 10. This is because, for the `range` function, the first number is *inclusive* (included in the sequence) while the second number is *exclusive* (**not** included in the sequence). So if you want to print all numbers from 0 -> 11, you need to change the 10 to an 11:

```python
for i in range(0, 11):
    print("i")
```
Now it will print the numbers 0 -> 10. Now if, you want to print only the numbers 1 -> 10 you would change the 0 to a 1: 

```python
for i in range(1, 11):
    print("i")
```

This inclusive / exclusive nature is known as the `off by 1` error because new programmers ALWAYS assume inclusivity. 

The next question you might have is why this is the way it is. The reason is because of how data is stored in the non-primitive variables we learned in Section 1. For example: 

```python
example = ["foo","bar", "foobar"]
```
This list has `3` elements and it is of length 3. However, the **index** of these elements start from 0 and end at 2. So if you wanted to use a for loop to print every element in this loop you would write the following:

```python
example = ["foo","bar", "foobar"]

for i in range(0, 2)
    print(example[i])
```
This will keep the variable `i` inlined with the element's index's.

## For Each Loops

The for loops above, using the `range` function, can be considered "normal" loops. They are similar to what you might see in Java under the following syntax:

```java
for (int i = 0; i > 10, i++)
{
    System.out.prinln(i);
}
```

However, there is "another type" of for loop that Python uses that makes it even easier to print items out. This type is known as a `for each` loop. (I put "another type" in quotes for a reason that I will get to later).

Think of for each loops like this: "For each element in `<sequence>`, do `<code block>`"
For example:

```python
planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]

for planet in planets:
    print(planet)
```
The above would read like this: "For each planet in planets, print out the planet."

This type of for loop can be really useful for math problems too. Take for instance the following:

```python
numbers = [10, 234, 66, 4, 23, 5, 66, 0]

for number in numbers:
    new_number = number // 2
    print(new_number)
```
The above would read like this: "For each number in numbers, divide that number by 2 and print it to the terminal."

Now, the reason why earlier I said that this is "another type" of for loop is because, in reality, it's not another type. The syntax might be different, but under the hood their both the same! Let's take another look at our first example:

```python
for i in range(0, 10):
    print("Hello")
```
Remeber what I said about the `range` function? I said that it creates a sequence of numbers given whatever numbers you input. Well, under the hood, the `range` function creates a sequence that looks like this: `(0, 1 ,2, 3, 4, 5, 6, 7, 8, 9)`. So if we break it down, our example above is *actually* doing the following:

```python
manual_range = (0, 1 ,2, 3, 4, 5, 6, 7, 8, 9)
for i in manual_range:
    print("Hello")
```
Look familiar? Hopefully this gives you a deeper understanding of for loops.

## For VS For Each

After reading all that you, you might be wondering what the point of the `range` function even is if you're able to traverse a list of items using much simpler syntax. Well, it's all about options and use cases. Take for instance this example:

```python
numbers = [10, 234, 66, 4, 23, 5, 66, 0]

for number in numbers:
    new_number = number // 2
    print(new_number)
```

What if, instead of just printing the number, we wanted to replace the number in the list? Long story short we wouldn't be able to do it in a `for each` loop (not without some more complex syntax anyway).

So the solution would be to use the `range` function:

```python
numbers = [10, 234, 66, 4, 23, 5, 66, 0]

for index in range(0, len(numbers)):
    number = numbers[index]
    new_number = number // 2
    numbers[index] = new_number
```
As you can see here, we use the `range` function, set to 0 (the first index) to the length of the `numbers` list (exclusive. i.e our range will go up to but not past the last index) to get each index of the list.

Then we use the index to get the number at that index, apply math to it, then save it back to the list at the same position as the current number. 

So when to use a normal for loop and when to use a for each loop is entirely up to the problem you are trying to solve.

## Nested For loops

For loops can also be "nested" What that means is that basically for loops can exist inside another for loop. Try running the following code and see what happens:

```python
for i in range(1, 11):
    for j in range(1, 11):
        print(i * j)
    print()
```

Now, nested for loops are somewhat of an advanced topic so don't be too concerned with understanding them just yet. But just keep in mind that they can be done.