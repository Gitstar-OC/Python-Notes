# Complete Python Notes from Scratch!

## Overview

- ### [Quicknote](#quicknote-1)

- ### [Syntax and Code Blocks](#Syntax-and-Code-Blocks)

  - #### [Common Syntax Errors](#common-semantic-errors-1)

  - #### [Common Semantic Errors](#common-semantic-errors-1)

- ### [Print](#print-1)

- ### [Functions](#functions-in-python)
  
  - #### [type()](#type-1)

  - #### [str()](#str-1)

  - #### [sorted()](#sorted-1)

  - #### [max() and min()](#max-and-min-1)

  - #### [Some other built in functions](#this-is-a-link-for-all-built-in-functions-in-python)


## Quicknote

Python is a general-purpose programming language used for scripting, automation, and developing various applications. It's compatible with Windows, Linux, and macOS, and runs on servers, workstations, PCs, mobile devices, and IoT.

### Python is:

- General purpose and widely used for scripting.
- Compatible with various operating systems.
- Utilized in IT support, system administration, web development, machine learning, and more.
- Beginner-friendly with English-like syntax.

### Python is not:

- Platform or OS-specific.
- A client-side scripting language.
- Purely object-oriented.


## Syntax and Code Blocks

Correct syntax is crucial in code writing. Small typos can cause syntax errors and prevent code execution. Be mindful of syntax to avoid minor mistakes that could take hours to identify in long code.

### Common Syntax Errors

- Misspellings
- Incorrect indentations
- Missing or incorrect key characters:
  - Bracket types - ( curved ), [ square ], { curly }
  - Quote types - "straight-double" or 'straight-single', “curly-double” or ‘curly-single’
  - Block introduction characters, like colons - :
- Data type mismatches
- Misused or misplaced Python reserved words
- Wrong case (uppercase/lowercase) - Python is case-sensitive

If syntax is correct but the script behaves unexpectedly, it may be due to a semantic problem. Semantics are the meaning and logic of coded statements. Syntactically correct code can run successfully but not do what we want.

### Common Semantic Errors

- Functional code with unintentional output
- Poor logic structures in code design

When working with code blocks, be mindful of syntax and semantic errors, and the overall result of your code. Fixing an error doesn't guarantee the desired effect when the code runs. Always click Run to check your work after fixing an error.

## print() 

The print() function outputs a specified object to the screen. The print() function is one of the most commonly used functions in Python because it allows you to output any detail from your code.

To use the print() function, you pass the object you want to print as an argument to the function. The print() function takes in any number of arguments, separated by a comma, and prints all of them.

```python
month = "September"
print("Investigate failed login attempts during", month, "if more than", 100)
```










## Functions in Python

Functions in Python are reusable blocks of code that perform a specific task. They help organize code, promote reusability, and improve readability.

### Defining Functions:

Functions in Python are defined using the `def` keyword followed by the function name and parentheses containing any parameters. The function body is indented beneath the function definition.

Example:

```python
def greet(name):
    print("Hello, " + name + "!")

greet(Raj)
```

The above code will output `Hello Raj!` 


## type()

The type() function returns the data type of its argument. The type() function helps you keep track of the data types of variables to avoid errors throughout your code. 

To use it, you pass the object as an argument, and it returns its data type. It only accepts one argument. For example, you could specify type("security") or type(7).

Passing one function into another
When working with functions, you often need to pass them through print() if you want to output the data type to the screen. This is the case when using a function like type(). Consider the following code:

```python 
print(type("This is a string"))
print(type(8))
print(type(7.233))
```

The above code will print `<class 'str'>` for first one, `<class 'int'>` for second, and `<class 'float'>` for the last one.


## str()
The str() function can be used to convert any data type to a string. The str()function takes a single argument, which is the value that you want to convert to a string. The str() function will then return a string representation of the value.

In this example, the str() function will convert the number 12 to a string. This will run the code and print the string representation of the number.

```python
number = 12
string_representation = str(number)
print(string_representation)
```

same can be done and you can use `float` and `int` to change some numeral strings into integers or floats which means decimals


## sorted() 

The sorted() function sorts the components of a list. The sorted() function also works on any iterable, like a string, and returns the sorted elements in a list. By default, it sorts them in ascending order. When given an iterable that contains numbers, it sorts them from smallest to largest; this includes iterables that contain numeric data as well as iterables that contain string data beginning with numbers. An iterable that contains strings that begin with alphabetic characters will be sorted alphabetically.

The sorted() function takes an iterable, like a list or a string, as an input. So, for example, you can use the following code to sort the list of login sessions from shortest to longest:

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(sorted(time_list))
```

This will print list in sorted order which is `[2, 12, 14, 19, 22, 32, 57]`

The sorted() function does not change the iterable that it sorts. The following code illustrates this:

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(sorted(time_list))
print(time_list)
``` 

This will output `[2, 12, 14, 19, 22, 32, 57]` for first and `
[12, 2, 32, 19, 57, 22, 14]` for second print statement. 

The first print() function displays the sorted list. However, the second print() function, which does not include the sorted() function, displays the list as assigned to time_list in the first line of code.

One more important detail about the sorted() function is that it cannot take lists or strings that have elements of more than one data type. For example, you can’t use the list [1, 2, "hello"].


## max() and min()
The max() function returns the largest numeric input passed into it. The min() function returns the smallest numeric input passed into it.

The max() and min() functions accept arguments of either multiple numeric values or of an iterable like a list, and they return the largest or smallest value respectively.

For example, you could use these functions to identify the longest or shortest session that a user logged in for. If a specific user logged in seven times during a week, and you stored their access times in minutes in a list, you can use the max() and min() functions to find and print their longest and shortest sessions:

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(min(time_list))
print(max(time_list))
```

This will print `2` as minimum from list and `57` as maximum from list. 

- ## [This is a link for all built in functions in python](https://docs.python.org/3/library/functions.html)