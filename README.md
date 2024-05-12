# Complete Python Notes from Scratch!

> You can click on (&#x25B2;) this arrow to head back to the overview section, it is added at the end of each part. 

## Overview

- [Quicknote](#quicknote)
- [Syntax and Code Blocks](#syntax-and-code-blocks)
  - [Common Syntax Errors](#common-syntax-errors)
  - [Common Semantic Errors](#common-semantic-errors)
- [Python Syntax](#python-syntax)
- [Data Types](#data-types)
- [Print](#print)
- [Function](#functions-in-python)
  - [type()](#type)
  - [str()](#str)
  - [sorted()](#sorted)
  - [max() and min()](#max-and-min)
  - [Some other built in functions](#this-is-a-link-for-all-built-in-functions-in-python)
- [Return Statement](#return) 


[**_&#x25B2; Go to Overview_**](#overview)


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

[**_&#x25B2; Go to Overview_**](#overview)

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

[**_&#x25B2; Go to Overview_**](#overview)

## Python Syntax

Python is a flexible programming language used in various fields like software development, machine learning, and data analysis. It's highly popular among data professionals, so understanding its basic syntax and meaning is crucial for your career growth. This reading discusses Python's syntax and meaning, stressing the importance of practice and exposure to code. Syntax includes words representing objects and commands, while punctuation provides structure and context. The meaning conveyed by syntax, known as semantics, is best learned through hands-on experience. Additionally, following established guidelines ensures consistent style within the language.

- **_Variables:_** Represent data stored as strings, tuples, dictionaries, lists, and objects.

 > (note: future readings explain these categories you can see them now by clicking on them!)

- **_Keywords:_** Special words that are reserved for specific purposes and that can only be used for those purposes
for ex => `in, not, or, for, while, return`

- **_Operators:_** Symbols that perform operations on objects and values
for ex => `+, -, *, /, **, %, //, >, <, ==`


- **_Expressions:_** A combination of numbers, symbols, and variables to compute and return a result upon evaluation


- **_Functions:_**  A group of related statements to perform a task and return a value

```python
def to_celsius(x):
   '''Convert Fahrenheit to Celsius'''
   return (x-32) * 5/9

to_celsius(75)
```


- **_Conditional Statements:_** Sections of code that direct program execution based on specified conditions

```python
number = -4


if number > 0:
   print('Number is positive.')
elif number == 0:
   print('Number is zero.')
else:
   print('Number is negative.')
```

As you’ll surely discover, Python generates syntax errors for incorrectly used keywords and syntax.

Example:

```python
print(This will throw an error because I didn’t make it a string.)
```

- **_Naming Rules and Convections_**

When assigning names to objects, programmers adhere to a set of rules and conventions which help to standardize code and make it more accessible to everyone. Here are some naming rules and conventions that you should know:

- Names cannot contain spaces.

- Names may be a mixture of upper and lower case characters.

- Names can’t start with a number but may contain numbers after the first character.

- Variable names and function names should be written in snake_case, which means that all letters are lowercase and words are separated using an underscore.

- Descriptive names are better than cryptic abbreviations because they help other programmers (and you) read and interpret your code. For example, student_name is better than sn. It may feel excessive when you write it, but when you return to your code you’ll find it much easier to understand.

Tim Peters, a Python programmer, wrote this now-famous “poem” of guiding principles for coding in Python:

<details>- <summary> <b> <i>  The Zen of Python </i></b></summary>
  
_Beautiful is better than ugly._

_Explicit is better than implicit._

_Simple is better than complex._

_Complex is better than complicated._

_Flat is better than nested._

_Sparse is better than dense._

_Readability counts._

_Special cases aren't special enough to break the rules._

_Although practicality beats purity._

_Errors should never pass silently._

_Unless explicitly silenced._

_In the face of ambiguity, refuse the temptation to guess._

_There should be one—and preferably only one—obvious way to do it._

_Although that way may not be obvious at first unless you're Dutch._

_Now is better than never._

_Although never is often better than *right* now._

_If the implementation is hard to explain, it's a bad idea._

_If the implementation is easy to explain, it may be a good idea._

_Namespaces are one honking great idea -- let's do more of those!_
</details>

Finally, it’s helpful to bookmark the [PEP 8 Style Guide for Python](https://peps.python.org/pep-0008/)  so you can reference it as needed. This reading is limited in scope, and PEP 8 is a more exhaustive resource for style-related matters. PEP stands for Python Enhancement Proposals. These are a running catalog of ways to improve or standardize Python as a language. Because Python is open source, PEP offers a framework to guide developers and build consensus around ideas. It’s a useful and trusted resource.

[**_&#x25B2; Go to Overview_**](#overview)



## Data Types 

In Python, data types are used to represent different kinds of information. Understanding these types is fundamental for effective programming. Here are the common data types:

- **String:** Represents text enclosed in quotes.
- **Integer:** Represents whole numbers without a decimal part.
- **Float:** Represents real numbers with a decimal part.

**Mixing Data Types:** Python doesn't allow mixing different data types in calculations. Combining an integer and a string will result in an error.

**Using the Type Function:** The type() function is handy for determining the data type of a value.

**Error Messages:** Errors are common in programming and provide clues to help you fix mistakes. Carefully reading error messages helps in understanding the problem.

## print()

The print() function outputs a specified object to the screen. The print() function is one of the most commonly used functions in Python because it allows you to output any detail from your code.

To use the print() function, you pass the object you want to print as an argument to the function. The print() function takes in any number of arguments, separated by a comma, and prints all of them.

```python
month = "September"
print("Investigate failed login attempts during", month, "if more than", 100)
```
[**_&#x25B2; Go to Overview_**](#overview)

## Functions in Python

Functions in Python are reusable blocks of code that perform a specific task. They help organize code, promote reusability, and improve readability.

### Defining Functions:

Functions in Python are defined using the `def` keyword followed by the function name and parentheses containing any parameters. The function body is indented beneath the function definition.

Examples:

```python
def greet(name):
    print("Hello, " + name + "!")

greet(Raj)
```

```python
def area_triangle(base, height):
    return base*height/2
area_a = area_triangle(5,4)
area_b = area_triangle(7,3)
sum = area_a + area_b
print("The sum of both areas is: " + str(sum))
```
The above code will print out `The sum of both areas is: 20.5`

```python
def convert_seconds(seconds):
    hours = seconds // 3600
    minutes = (seconds - hours * 3600) // 60
    remaining_seconds = seconds - hours * 3600 - minutes * 60
    return hours, minutes, remaining_seconds
 
hours, minutes, seconds = convert_seconds(5000)
print(hours, minutes, seconds)
```
The above code will print `1 23 20`

The above code will output `Hello Raj!`

[**_&#x25B2; Go to Overview_**](#overview)

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

[**_&#x25B2; Go to Overview_**](#overview)

## str()
The str() function can be used to convert any data type to a string. The str()function takes a single argument, which is the value that you want to convert to a string. The str() function will then return a string representation of the value.

In this example, the str() function will convert the number 12 to a string. This will run the code and print the string representation of the number.

```python
number = 12
string_representation = str(number)
print(string_representation)
```

same can be done and you can use `float` and `int` to change some numeral strings into integers or floats which means decimals

[**_&#x25B2; Go to Overview_**](#overview)

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

[**_&#x25B2; Go to Overview_**](#overview)

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

[**_&#x25B2; Go to Overview_**](#overview)

- ## [This is a link for all built in functions in python](https://docs.python.org/3/library/functions.html)


## Return 
The `return` statement is used to return a value from a function, causing the function to stop executing and return the specified value to the caller. Here are some key points about the `return` statement:

- It can return any type of value, including integers, floats, strings, lists, and dictionaries.
- If a function lacks a `return` statement, it will return `None` by default.
- Multiple `return` statements can be used within a function to return different values at different points in the execution.
- It can control the flow of execution within a function, allowing for early exits based on certain conditions.

```python
def calculate_area(base, height):
  """
  This function calculates the area of a triangle.
  """
  area = (base * height) / 2
  return area

# Call the function and store the result in a variable
area = calculate_area(5, 10)

# Print the result
print(area)
```
This will output the area as `25`
