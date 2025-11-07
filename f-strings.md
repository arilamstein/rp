# An Introduction to f-strings

## Review: Strings, Variables and Printing

Earlier you learned how to create strings, store them in variables, and print them. As a reminder, here's a short program that stores "Hello world." in a variable, and then prints it to the console:


```python
greeting = "Hello world."
print(greeting)
```

    Hello world.

In the program above, `greeting` is *static*. That is, the value inside of it never changes. However, in programming it is common to create strings that contain variables inside them. For example, below is a program that greets a user by name:

```python
name = "Bob"
greeting = "Hello " + name + "."
print(greeting)
```

    Hello Bob.


While this works, the code to create `greeting` is a bit hard to read. We need to put a `+` before and after `name`, and this makes it hard to visualize what the final string will look like. f-strings offer a cleaner way to include variables inside strings.

# f-strings

To create an f-string, just put the letter `f` in front of the quote that starts the string:


```python
f"Hello world."
```




    'Hello world.'

This behaves just like a regular string. The differences only occur when you add variables and evaluated expressions to the string.

## Variable Substitution

Instead of using `+`, f-strings let you embed a variable directly in a string. To do this, put the variable inside curly braces `{}` in the string. Here's our example from above, but using f-strings:


```python
name = "Bob"
greeting = f"Hello {name}."
print(greeting)
```

    Hello Bob.


Here the assignment of `greeting` is easier to read, because it's defined all at once. And the curly braces make it easy to see when a variable is being used. 

## Evaluated Expressions

While the main use of f-strings is to embed variables in strings, you can also use them to embed evaluated expressions. For example, here's a program that calculates the result of 2+2 inside an f-string:


```python
f"2 + 2 = {2+2}"
```




    '2 + 2 = 4'



Python evaluates the expression inside the braces and inserts the result into the string. 

## Unlimited Substitutions

A single f-string can contain an unlimited number of variables and evaluated expressions. For example, here's our addition example from above, but using variables for each number:


```python
x = 2
y = 2
print(f"{x} + {y} = {x + y}")
```

    2 + 2 = 4

This f-string includes two variables (`x` and `y`) and an expression (`x + y`). Python evaluates each part inside the braces and inserts the results into the string, producing the output `2 + 2 = 4`.

# Exercise

Now it's your turn to practice using f-strings to combine variables and expressions. Below is a program that contains a user's name and age. Create a single f-string that:
  * Greets the user by name
  * Tells them their current age
  * Tells them what their age will be next year
  
```python
name = "Jane"
age = 25

# output = f"..."
# print(output)
```
