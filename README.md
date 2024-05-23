# Complete Python Notes from Scratch
<!--
> You can click on (&#x25B2;) this arrow to head back to the overview section, it is added at the end of each part.
-->
## Overview

- [Quicknote](#quicknote)
- [Syntax and Code Blocks](#syntax-and-code-blocks)
  - [Common Syntax Errors](#common-syntax-errors)
  - [Common Semantic Errors](#common-semantic-errors)
- [Python Syntax](#python-syntax)
- [Data Types](#data-types)
  - [f-String](#f-string)
- [Data Structures](#data-structure)
- [Comments](#comment)
- [Print](#print)
- [Function](#functions-in-python)
  - [lower()](#lower)
  - [count()](#count)
  - [len()](#len)
  - [round()](#round)
  - [type()](#type)
  - [str()](#str)
  - [sorted()](#sorted)
  - [max() and min()](#max-and-min)
  - [Some other built in functions](#this-is-a-link-`for`-all-built-in-functions-in-python)
- [Writing good code](#writing-good-code)
- [Return Statement](#return)
- [Mathematical Operators](#mathematical-operators)
- [Random Module](#random-module)
- [Comparing Values](#comparing-values)
- [Comparison Operators with Equations](#comparison-operators-with-equations)
  - [Equality `==` and Not Equal To `!=` Operators](#part-1-equality--and-not-equal-to--operators)
  - [Greater Than `>` and Less Than `<` Operators](#part-2-greater-than--and-less-than--operators)
  - [Greater Than or Equal to `>=` and Less Than or Equal to `<=` Operators](#part-3-greater-than-or-equal-to--and-less-than-or-equal-to--operators)
- [Comparison Operators with Strings](#comparison-operator-with-strings)
  - [Equality `==` and Not Equal to `!=` Operators with Strings](#part-1-equality--and-not-equal-to--operators-with-strings)
  - [The Greater Than `>` and Less Than `<` Operators with Strings](#part-2-the-greater-than--and-less-than--operators)
  - [The Greater Than or Equal To `>=` and Less Than or Equal To `<=` Operators](#part-3-the-greater-than-or-equal-to--and-less-than-or-equal-to--operators)
- [Exponentiation](#exponentiation-in-python)
- [Logical Operators](#logical-operators)
  - [The `and` Logical Operator](#part-1-the-and-logical-operator)
  - [The `or` Logical Operator](#part-2-the-or-logical-operator)
  - [The `not` Logical Operator](#part-3-the-not-logical-operator)
- [Conditionals](#conditionals)
  - [If](#if)
  - [Else](#else)
  - [Elif](#elif)
- [Loops](#loops)
  - [For Loop](#for-loop)
  - [While Loop](#while-loop)
  - [Nested Loop](#nested-loop)

[**_&#x25B2; Go to Overview_**](#overview)

## Quicknote

Python is a general-purpose programming language used `for` scripting, automation, and developing various applications. It's compatible with Windows, Linux, and macOS, and runs on servers, workstations, PCs, mobile devices, and IoT.

### Python is

- General purpose and widely used `for` scripting.
- Compatible with various operating systems.
- Utilized in IT support, system administration, web development, machine learning, and more.
- Beginner-friendly with English-like syntax.

### Python is not

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

Python is a flexible programming language used in various fields like software development, machine learning, and data analysis. It's highly popular among data professionals, so understanding its basic syntax and meaning is crucial `for` your career growth. This reading discusses Python's syntax and meaning, stressing the importance of practice and exposure to code. Syntax includes words representing objects and commands, while punctuation provides structure and context. The meaning conveyed by syntax, known as semantics, is best learned through hands-on experience. Additionally, following established guidelines ensures consistent style within the language.

- **_Variables:_** Represent data stored as strings, tuples, dictionaries, lists, and objects.

 > (note: future readings explain these categories you can see them now by clicking on them!)

- **_Keywords:_** Special words that are reserved `for` specific purposes and that can only be used `for` those purposes
`for` ex => `in, not, or, `for`, while, return`

- **_Operators:_** Symbols that perform operations on objects and values
`for` ex => `+, -, *, /, **, %, //, >, <, ==`

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

As you’ll surely discover, Python generates syntax errors `for` incorrectly used keywords and syntax.

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

Tim Peters, a Python programmer, wrote this now-famous “poem” of guiding principles `for` coding in Python:

<details> <summary> The Zen of Python </summary>

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

_Although never is often better than _right_ now._

_If the implementation is hard to explain, it's a bad idea._

_If the implementation is easy to explain, it may be a good idea._

_Namespaces are one honking great idea -- let's do more of those!_

</details>

Finally, it’s helpful to bookmark the [PEP 8 Style Guide `for` Python](https://peps.python.org/pep-0008/)  so you can reference it as needed. This reading is limited in scope, and PEP 8 is a more exhaustive resource `for` style-related matters. PEP stands `for` Python Enhancement Proposals. These are a running catalog of ways to improve or standardize Python as a language. Because Python is open source, PEP offers a framework to guide developers and build consensus around ideas. It’s a useful and trusted resource.

[**_&#x25B2; Go to Overview_**](#overview)

## Data Types

In Python, data types are used to represent different kinds of information. Understanding these types is fundamental `for` effective programming. Here are the common data types:

- **String:** Represents text enclosed in quotes.

```python
'hello'
print("hi")
# All the things enclosed in quotes are strings
```

```python
jadu = "hello"[4]
print(jadu)
# You can also print out a character at any place by reducing one from the number you want to get, because python starts counting from 0
```

- **Integer:** Represents real numbers (both positive and negative) without a decimal part.

```python
123
123_456_789
# Any number directly written is called as Interger (int), to write long number we can write it by including '_' it works the same as ','
```

- **Float:** Represents real numbers with a decimal part.

```python
123.45
# Any integer, with decimal is a float
```

**Mixing Data Types:** Python doesn't allow mixing different data types in calculations. Combining an integer and a string will result in an error.

**Using the Type Function:** The type() function is handy `for` determining the data type of a value.

**Error Messages:** Errors are common in programming and provide clues to help you fix mistakes. Carefully reading error messages helps in understanding the problem.

### f-String

In python f- string (f) is used to convert multiple types of data types like float, boolean and integer to string

For example:

```python
score = 0
height = 1.8
isWinning = True

print(f"your score is {score}, your height is {height}, and you are winning is {isWinning}")

# your score is 0, your height is 1.8, and you are winning is True
# you just need to add infront of the first " quote symbol
```

## Data Structure

Data Structure is a way of storing and organizing data in python

## Lists

Used to store data in a sequence and order, you can create list by

```python
listOfFruits = ["apple", "banana", "mango"]

#the list is created you can also print it
print(listOfFruits)

# This will print the whole list
```

You can get the items at a particular place by using the `[]` brackets, and the position of the elements start form zero `0`

```python
fruit1 = listOfFruits[0]

print(fruit1) # This will print apple
```

You can also get the items in the list from the last order, you just need to start it from `negative 1` ( -1 )

```python
lastFruit = listOfFruits[-1]

print(lastFruit)

# This will print mango
```

You can also add items to the lists by using the `.append()` function

```python
listOfFruits.append("kiwi")

# This will add kiwi to the list
```

**There are more built in function `for` list, you can see that all by [clicking here](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists)**

### Nested Lists

You can create lists inside lists which is called as nested lists, `for` example

```python
fruits = ["apple", "banana", "mango"]
vegetables = ["potato", "tomato", "brinjal", "cucumber"]

groceryItems = [fruits, vegetables]

print(groceryItems) # This will print both the list like this

# [["apple", "banana", "mango"],  ["potato", "tomato", "brinjal", "cucumber"]]
```

You can access the items in a particular list by the following way

```python
# if you want to print tomato which is at second place of second list you will use the below code

item = groceryItems[1][1]
print(item)

# The above code will print tomato
```

## Comment

```python
#This is a single line comment in python
"""
This is how you can
write Multiline comment in
Python
"""
```

Including comments in your code offers numerous benefits. They significantly improve readability by providing additional context and explanations, making it easier `for` developers to understand the purpose and functionality of different sections. Comments serve as invaluable documentation, clarifying the logic, algorithms, and complex operations performed, thus aiding in debugging and troubleshooting.

- So use comments in your code, it makes your code better.

[**_&#x25B2; Go to Overview_**](#overview)

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

### Defining Functions

Functions in Python are defined using the `def` keyword followed by the function name and parentheses containing any parameters `(parameter (argument) -  a value passed into a function `for` use within the function)`. The function body is indented beneath the function definition.

Examples:

```python
def greet(name):
    print("Hello, " + name + "!")

greet(Raj)
```

The above code will output `Hello Raj!`

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

You must use `functions` to save space and time as shown in the below example of code reusability

```python
name = "Kay"
number = len(name) * 9

print("Hello " + name + ". Your lucky number is " + str(number))

name = "Cameron"
number = len(name) * 9

print("Hello " + name + ". Your lucky number is " + str(number))
```

Below is the same alternative `for` the above code using functions!

```python
def lucky_number(name):
    number = len(name) * 9
    print("Hello " + name + ". Your lucky number is " + str(number))

lucky_number("Kay")
lucky_number("Cameron")
```

The both code example output the same thing, but using a function is more helpful and reusable than the whole code written again and again

**You could learn more about `return` keyword by [Clicking Here](#return)**

[**_&#x25B2; Go to Overview_**](#overview)

### lower()

lower() is a built in function in python, which lowercases the whole string. For example:

```python
txt = "Hello my FRIENDS"

x = txt.lower()

print(x)
# This will print "hello my friends"
```

[**_&#x25B2; Go to Overview_**](#overview)

### count()

count() is a built in function in python, which is used to count the number of item in particular list, string, tuple, number etc. . For Example:

```python
fruits = ['apple', 'banana', 'cherry']

x = fruits.count("cherry") # This will count the number of cherry's
```

```python
points = [1, 4, 2, 9, 7, 8, 9, 3, 1]

x = points.count(9)
# This will count the number of 9 in this whole list
```

```python
name = "Mark Zukerberg"
e = name.count("e")
print(e)

#This will count the number of e in the name
```

Here's a little `love calculator` made using lower(), count(), and if, else statement along with input

```python
name1 = input("what is your name?")
name2 = input("what is your partner's or crush's name?")

combinedName = name1 + name2
lowerNames = combinedName.lower()

t = lowerNames.count("t")
r = lowerNames.count("r")
u = lowerNames.count("u")
e = lowerNames.count("e")

firstLetter = t + r + u + e

l = lowerNames.count("l")
o = lowerNames.count("o")
v = lowerNames.count("v")
e = lowerNames.count("e")
secondLetter = l + o + v + e

score = int(str(firstLetter) + str(secondLetter))


if score < 10 or score > 90:
  print(f"Your score is {score}, you go together like coke and mentos.")
elif score < 50 and score > 40:
  print(f"Your score is {score}, you are alright together.")
else:
  print(f"Your score is {score}.")
```



[**_&#x25B2; Go to Overview_**](#overview)

### len()

The len function is used to get the number of characters in a string

```python
print(len("Where do you work"))
# This will print out the number of characters (including spaces)
```

[**_&#x25B2; Go to Overview_**](#overview)

### round()

The round function rounds up the number, it directly rounds up the number to a integer but you can use it to round up to decimal places too

```python
print(round(8 / 3)) # This will print 2
print(round(8 /3 , 3))  # This will round it to 3 decimal places
```

[**_&#x25B2; Go to Overview_**](#overview)

### type()

The type() function returns the data type of its argument. The type() function helps you keep track of the data types of variables to avoid errors throughout your code.

To use it, you pass the object as an argument, and it returns its data type. It only accepts one argument. For example, you could specify type("security") or type(7).

Passing one function into another
When working with functions, you often need to pass them through print() if you want to output the data type to the screen. This is the case when using a function like type(). Consider the following code:

```python
print(type("This is a string"))
print(type(8))
print(type(7.233))
```

The above code will print `<class 'str'>` `for` first one, `<class 'int'>` `for` second, and `<class 'float'>` `for` the last one.

[**_&#x25B2; Go to Overview_**](#overview)

### str()

The str() function can be used to convert any data type to a string. The str()function takes a single argument, which is the value that you want to convert to a string. The str() function will then return a string representation of the value.

In this example, the str() function will convert the number 12 to a string. This will run the code and print the string representation of the number.

```python
number = 12
string_representation = str(number)
print(string_representation)
```

same can be done and you can use `float` and `int` to change some numeral strings into integers or floats which means decimals

[**_&#x25B2; Go to Overview_**](#overview)

### sorted()

The sorted() function sorts the components of a list. The sorted() function also works on any iterable, like a string, and returns the sorted elements in a list. By default, it sorts them in ascending order. When given an iterable that contains numbers, it sorts them from smallest to largest; this includes iterables that contain numeric data as well as iterables that contain string data beginning with numbers. An iterable that contains strings that begin with alphabetic characters will be sorted alphabetically.

The sorted() function takes an iterable, like a list or a string, as an input. So, `for` example, you can use the following code to sort the list of login sessions from shortest to longest:

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

This will output `[2, 12, 14, 19, 22, 32, 57]` `for` first and `
[12, 2, 32, 19, 57, 22, 14]` `for` second print statement.

The first print() function displays the sorted list. However, the second print() function, which does not include the sorted() function, displays the list as assigned to time_list in the first line of code.

One more important detail about the sorted() function is that it cannot take lists or strings that have elements of more than one data type. For example, you can’t use the list [1, 2, "hello"].

[**_&#x25B2; Go to Overview_**](#overview)

### max() and min()

The max() function returns the largest numeric input passed into it. The min() function returns the smallest numeric input passed into it.

The max() and min() functions accept arguments of either multiple numeric values or of an iterable like a list, and they return the largest or smallest value respectively.

For example, you could use these functions to identify the longest or shortest session that a user logged in `for`. If a specific user logged in seven times during a week, and you stored their access times in minutes in a list, you can use the max() and min() functions to find and print their longest and shortest sessions:

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(min(time_list))
print(max(time_list))
```

This will print `2` as minimum from list and `57` as maximum from list.

[**_&#x25B2; Go to Overview_**](#overview)

- ## [This is a link `for` all built in functions in python](https://docs.python.org/3/library/functions.html)

## Writing Good Code

Now, you can understand a good level of code so here's a note from a Great Coder **[Matin Folwer](https://en.wikipedia.org/wiki/Martin_Fowler_(software_engineer))**:

**_`Any fool can write code that a computer can understand, Good Programmers write code that humans can understand`_**

What I mean by that will be demonstrated with a small example

```python
def calculate(d):
    q = 3.14
    z = q * (d ** 2)
    print(z)

calculate(5)
#Output is 78.5
```

Now most of the people will not understand in the first time what this code is doing, so now read the below code

```python
def circle_area(radius):
    pi = 3.14
    area = pi * (radius ** 2)
    print(area)

circle_area(5)
#Output is 78.5
```

Now you can understand that the above code is used `for` measuring area of Circle! _This is what writing good code means `code which others can understand!!`_

[**_&#x25B2; Go to Overview_**](#overview)

## Return

The `return` statement is used to return a value from a function, causing the function to stop executing and return the specified value to the caller. Here are some key points about the `return` statement:

- It can return any type of value, including integers, floats, strings, lists, and dictionaries.
- If a function lacks a `return` statement, it will return `None` by default.
- Multiple `return` statements can be used within a function to return different values at different points in the execution.
- It can control the flow of execution within a function, allowing `for` early exits based on certain conditions.

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

[**_&#x25B2; Go to Overview_**](#overview)

## Mathematical Operators

You can use the mathematical operators as it is in python but `PEMDAS` is used to calculate the result

```python
3 + 5 #8
7 - 4 #3
3 * 2 #6
6 / 3 #2
2 ** 3 (2 ^ 3) #8
```

You can also use `floor division` to print out direct result when devided by numbers, `for` example:

```python
print(8 // 8) #This will directly print 2
print(15 // 4) #This will directly print 3
```

You can also devide, multiply, add or subtract the whole number after they are assigned, `for` example:

```python
result = 4
result /= 2 #Divide 4 again by 2
result += 1 #Adds 1 to the result
result *= 5 #Multiplies by 5
result -= 5 #Subtracts 5 from it
```

[**_&#x25B2; Go to Overview_**](#overview)

## Comparing Values

In this section, we'll explore how Python compares values and makes decisions based on those comparisons. This is a fundamental concept in programming, allowing us to control the flow of our code based on specific conditions.

`Comparisons`:
Python uses comparison operators to check relationships between values. These operators include:

- **Greater than (>):** Checks if the left operand is greater than the right operand.
- **Less than (<):** Checks if the left operand is less than the right operand.
- **Greater than or equal to (>=):** Checks if the left operand is greater than or equal to the right operand.
- **Less than or equal to (<=):** Checks if the left operand is less than or equal to the right operand.
- **Equal to (==):** Checks if the left operand is equal to the right operand.
- **Not equal to (!=):** Checks if the left operand is not equal to the right operand.
These operators return a Boolean value, either `True` or `False`, depending on the outcome of the comparison.

`Equality`:
Equality in Python is a bit more nuanced than simply comparing values. `While the == operator checks `for` value equality`, it's important to remember that different data types can have the same value but not be considered equal. For example, the integer 1 and the string "1" have the same numerical value, but they are different data types. `Therefore, 1 == "1" would evaluate to False`.

`Logical Operators`:
Python also provides logical operators that combine comparisons to create more complex conditions. These operators include:

- **And (and):** Returns True only if both operands are True.
- **Or (or):** Returns True if at least one operand is True.
- **Not (not):** Inverts the truth value of the operand.
These operators allow us to build intricate conditions that control the flow of our code based on multiple factors.

Real-World Examples

Here are some real-world examples of how comparisons and equality are used in Python:

- Checking if a user's age is greater than 18 to grant access to a website.
- Comparing two product prices to determine the cheaper option.
- Validating user input to ensure it meets specific criteria.
- Analyzing data to identify patterns and trends.

By understanding comparisons and equality, you can write more powerful and flexible Python code that can adapt to various situations and make intelligent decisions."

[**_&#x25B2; Go to Overview_**](#overview)

## Comparison Operators with Equations

The following examples demonstrate how to use comparison operators with the data types `int` (integers, whole numbers) and `float` (number with a decimal point or fractional value). Comparison operators return Boolean results. As you learned previously, Boolean is a data type that can hold only one of two values: `True` or `False`.

The comparison operators include:

- **==**    (equality)

- **!=**     (not equal to)

- **>**       (greater than)

- **<**      (less than)

- **>=**    (greater than or equal to)

- **<=**    (less than or equal to)

### PART 1: Equality == and Not Equal To != Operators

In Python, you can use comparison operators to compare values. When a comparison is made, Python returns a Boolean result: True or False. Note that Boolean data types are not string data types (Boolean True is not equal to the string "True").

- To check if two values are the same, use the **equality operator: ==**

- To check if two values are not the same, use the **not equal to operator: !=**

The print() function can be used to display the results of the comparisons.

**Examples:**

```python

print(32 == 30+2)   # The == operator checks if the 2 values are
True                # equal to each other. If they are equal,
                    # Python returns a True result.


print(5+10 == 6+7)  # If the two values are not equal, as in the
False               # expression 5+10 == 6+7 (or 15 == 13), Python
                    # returns a False result.


print(10-4 != 10+4) # The != operator checks if the 2 values are
True                # NOT equal to each other. If true, Python
                    # returns a True result.


print(9/3 != 3*1)   # In this last example, 9/3 != 3*1 (or 3 != 3)
False               # is false. So, Python returns a False value.
```

#### The equality == operator versus the equals = operator

It is important to note that the equality == comparison operator performs a different task than the equals = assignment operator. The equals = operator assigns the value on the right side of the equals = to the object (e.g., a variable) on the left side of the equals = operator.

**Examples:**

```python

# The = equals assignment operator is used to assign a value to a
# variable.

my_variable = 3*5           # Assigns a value to my_variable
print(my_variable)          # Printing the variable returns the
15                          # value assigned to the variable.



# The == equality comparison operator checks if the values of the two
# expressions on either side of the == operator are equivalent to one
# another.

print(my_variable == 3*5)   # Printing the variable returns a Boolean
True                        # True or False result.
```

[**_&#x25B2; Go to Overview_**](#overview)

### PART 2: Greater Than > and Less Than < Operators

The comparison operators greater than > and less than < also return a `True` or `False` Boolean result after comparing two values.

- To check if one value is larger than another value, use the greater than operator: >

- To check if one value is smaller than another value, use the less than operator: <

**Examples:**

```python
print(11 > 3*3)         # The > operator checks if the left value is
True                    # greater than the right value. If true, it
                        # returns a True result.


print(4/2 > 8-4)        # If the > operator finds that the left value
False                   # is NOT greater than the right value, the
                        # comparison will return a False result.


print(4/2 < 8-4)        # The < operator checks  if the left value is
True                    # less than the right side. If true, the
                        # comparison returns a True result.


print(11 < 3*3)         # If the < operator finds that the left side is False
                        # NOT less than the right value, Python returns
False                   # a False result.
```

[**_&#x25B2; Go to Overview_**](#overview)

### PART 3: Greater Than or Equal to >= and Less Than or Equal to <= Operators

Like the other comparison operators, the greater than or equal to >= and less than or equal to <= operators return a `True` or `False` Boolean result when a comparison is made.

- To check if one value is larger than or equal to another value, use the greater than or equal to operator: >=

- To check if one value is smaller than or equal to another value, use the less than or equal to operator: <=

**Examples:**

```python

print(12*2 >= 24)   # The >= operator checks if the left value is
True                # greater than or equal to the right value.
                    # If one of these conditions is true,
                    # Python returns a True result. In this case
                    # the two values are equal. So, the comparison
                    # returns a True result.


print(18/2 >= 15)   # If the >= comparison determines that the left
False               # value is NOT greater than or equal to the
                    # right, it returns a False result.

print(12*2 <= 30)   # The <= operator checks if the left value is
True                # less than or equal to the right value. In
                    # this case, the left value is less than the
                    # right value. Again, if one of the two
                    # conditions is true, Python returns a True
                    # result.


print(15 <= 18/2)   # If the <= comparison determines that the left
False               # value is NOT less than or equal to the right
                    # value, the comparison returns a False result.
```

**Python comparison operators return Boolean results: `True` or `False`.**

| Symbol | Name                            | Expression | Description                      |
|--------|---------------------------------|------------|----------------------------------|
| ==     | Equality operator               | a == b     | a is equal to b                  |
| !=     | Not equal to operator           | a != b     | a is not equal to b              |
| >      | Greater than operator           | a > b      | a is larger than b               |
| >=     | Greater than or equal to operator | a >= b   | a is larger than or equal to b   |
| <      | Less than operator              | a < b      | a is smaller than b              |
| <=     | Less than or equal to operator  | a <= b     | a is smaller than or equal to b  |

[Python Comparison Operators with Syntax and Example](https://data-flair.training/blogs/python-comparison-operators/) - Provides examples of more complex comparisons

[**_&#x25B2; Go to Overview_**](#overview)

## Comparison Operator with Strings

In this reading, you will learn more about what comparison operators can and cannot do. If you use the `==` (equality) and `!=` (not equal to) operators with strings, you can check if two strings contain the same text or not. You can also alphabetize strings using `>` (greater than), `<` (less than), `>=` (greater than or equal to), `<=` (less than or equal to) comparison operators. As with numeric data types, comparison operators used with strings will return Boolean (`True, False`) results.

[**_&#x25B2; Go to Overview_**](#overview)

### PART 1: Equality == and Not Equal to != Operators with Strings

In Python, you can use comparison operators to compare strings. The equality == and the not equal to `!=` operators are helpful when you need to search `for` a specific string in a body of text, a log file, a spreadsheet, a database, and more. You can also check user input strings to compare them to another string. Note that Boolean data types are not string data types (Boolean `True` is not equal to the string "True").

**Examples:**

```python
# The == operator can check if two strings are equal to each other.
# If they are equal, the Python interpreter returns a True result.
print("a string" == "a string")
True


# In this example, the equality == comparison is between "4 + 5" and
# 4 + 5. Since the left data type is a string and the right data type
# is an integer, the two values cannot be equal. So, the comparison
# returns a False result.
print("4 + 5" == 4 + 5)
False


# The != operator can check if the two strings are NOT equal to each
# other. If they are indeed not equal, then Python returns a True result.
print("rabbit" != "frog")
True


# In this example, the variable event_city has been assigned the string
# value "Shanghai". This variable is compared to a static string,
# "Shanghai", using the != operator. As, the strings "Shanghai" and
# "Shanghai" are the same, the comparison of "Shanghai" != "Shanghai"
# is false. Accordingly, Python will return a False result.
event_city = "Shanghai"
print(event_city != "Shanghai")
False

# This last example illustrates the result of trying to compare two
# items of different data types using the equality == operator. The
# two items are not equal, so the comparison returns False.
print("three" == 3)
False
```

[**_&#x25B2; Go to Overview_**](#overview)

### PART 2: The Greater Than > and Less Than < Operators

The comparison operators greater than > and less than < can be used to alphabetize words in Python. The letters of the alphabet have numeric codes in Unicode (also known as ASCII values). The uppercase letters A to Z are represented by the Unicode values 65 to 90. The lowercase letters a to z are represented by the Unicode values 97 to 122.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bDQ-ePOZTn-CPAUMGiUoRQ_9657c1d2872d485783633c5fe8fa47f1_Unicode_table.png?expiry=1715731200000&hmac=vkOTuD6TmqjCRn4amrdVrj5CcvMTiQ6tLMJOwFpUHFI)

- To check if the first letter(s) of a string have a larger Unicode value (meaning the letter is closer to 122 or lowercase z) than the first letter of another string, use the greater than operator: >

- To check if the first letter(s) of a string have a smaller Unicode value (meaning the letter is closer to 65 or uppercase A) than the first letter of another string, use the less than operator: <

Like numeric comparisons with the greater than `>` and less than `<` operators, comparisons between strings also return Boolean `True` or `False` results.

**Examples:**

```python
# The greater than > operator checks if the left string has a higher
# Unicode value than the right string. If true, the Python interpreter
# returns a True result. Since W has a Unicode value of 87, and you can
# easily calculate that F has a Unicode value of 70, this comparison is
# the same as 87 > 70. As this is true, Python will return a True
# result.
print("Wednesday" > "Friday")
True


# The less than < operator checks if the left string has a lower
# Unicode value than the right string. If you reference the Unicode
# chart above, you can see that all lowercase letters have higher
# Unicode values than uppercase letters. We can see that B has a
# Unicode value of 66 and b has a Unicode value of 98. This
# comparison is the same as 66 < 98, which is true. So, Python will
# return a True result.
print("Brown" < "brown")
True


# If the strings have the same first few letters, the comparison will
# cycle through each letter of each string, from left to right until it
# finds two letters that have different Unicode values. In this example,
# both strings share the initial substring "sun", but then have
# different letters with different Unicode values in the fourth place
# in each string. So, the fourth letters 'b' and 't' of the two
# strings are used `for` the comparison. Since 'b' does not have a higher
# Unicode value than 't', the comparison returns a False result.
print("sunbathe" > "suntan")
False


# If two identical strings are compared using the less than < comparison
# operator, this will produce a False result because they are equal.
print("Lima" < "Lima")
False


# This last example illustrates the result of trying to compare two
# items of different data types using the less than < operator. The
# greater than > and less than operators < cannot be used to compare
# two different data types.
print("Five" < 6)
'''
Error on line 1:
    print("Five" < 6)
TypeError: '<' not supported between instances of 'str' and 'int'
```

[**_&#x25B2; Go to Overview_**](#overview)

### PART 3: The Greater Than or Equal To >= and Less Than or Equal To <= Operators

The greater than or equal to `>=`  and less than or equal to `<=` operators can be used with strings as well. Like the other comparison operators, they will return a `True` or `False` Boolean result when a comparison is made between two strings.

- To check if a string has a larger or equal Unicode value than the first letter(s) of another string, use the greater than or equal to operator: `>=`

- To check if a string has a smaller or equal Unicode value than the first letter(s) of another string, use the less than or equal to operator: `<=`

At this point, you should be familiar with how comparison operators work in Python. Can you determine what the results will be from the comparisons listed below? When you are ready to check your answers, click Run.

1. "my computer" >= "my chair"

2. "Spring" <= "Winter"

3. "pineapple" >= "pineapple"

```python
# Use the Unicode chart in Part 2 to determine if the Unicode values of
# the first letters of each string are higher, lower, or equal to one
# another.


var1 = "my computer" >= "my chair"
var2 = "Spring" <= "Winter"
var3 = "pineapple" >= "pineapple"

print("Is \"my computer\" greater than or equal to \"my chair\"? Result: ", var1)
print("Is \"Spring\" less than or equal to \"Winter\"? Result: ", var2)
print("Is \"pineapple\" less than or equal to \"pineapple\"? Result: ", var3

# Output
# Is "my computer" greater than or equal to "my chair"? Result:  True
# Is "Spring" less than or equal to "Winter"? Result:  True
# Is "pineapple" less than or equal to "pineapple"? Result:  True
```

Key Takeways

| Expression | Description                                                                        |
|------------|------------------------------------------------------------------------------------|
| "a" == "a" | If string "a" is identical to string "a", returns True. Else, returns False.       |
| "a" != "b" | If string "a" is not identical to string "b"                                        |
| "a" > "b"  | If string "a" has a larger Unicode value than string "b"                            |
| "a" >= "b" | If the Unicode value `for` string "a" is greater than or equal to the Unicode value of string "b" |
| "a" < "b"  | If string "a" has a smaller Unicode value than string "b"                           |
| "a" <= "b" | If the Unicode value `for` string "a" is smaller than or equal to the Unicode value of string "b" |

[**_&#x25B2; Go to Overview_**](#overview)

## Exponentiation in Python

In mathematics, an exponent of a number says how many times that number is repeatedly multiplied with itself. We usually express that operation as bn, where b is the base and n is the `exponent` or power. We often call that type of operation “b raised to the n-th power”, “b raised to the power of n”, or most briefly as “b to the n” (Wikipedia, 2019).

Python has three ways to exponentiate values:

- The `** operator`. To program 2^5 we do `2 ** 5`.
- The built-in `pow()` function. 2^3 coded becomes `pow(2, 3)`.
- The `math.pow()` function. To calculate 3^5, we do `math.pow(3, 5)`.

### Python’s exponent operator: `**`

The first way to raise a number to a power is with Python’s `**` operator. This operator is also called the exponent operator or power operator.

The `**` operator works with two values, just like regular multiplication with `*` does. This time, however, we raise its left argument to the power of its right argument (Python Docs, n.d. c). Let’s say we want to calculate 33. We do that with `**` like so

```python
3 ** 3
# Returns: 27
```

> The `**` operator returns a ZeroDivisionError when we raise 0.0 to a negative power. And when we raise a negative number to a fractional power, it returns a complex number.

Example:

Let’s see how we can use the `**` operator in a Python program. The code below raises several values to a certain exponent, and then outputs the results:

```python
# Some random values
valueA = 3
valueB = 144
valueC = -987
valueD = 25
valueE = -0.25

# Calculate the exponent `for` the variables
aExp = valueA ** 2
bExp = valueB ** 3
cExp = valueC ** 4
dExp = valueD ** -5
eExp = valueE ** 0.125

# Output the results
print(valueA, "^2 = ", aExp, sep="")
print(valueB, "^3 = ", bExp, sep="")
print(valueC, "^4 = ", cExp, sep="")
print(valueD, "^-5 = ", dExp, sep="")
print(valueE, "^0.125 = ", eExp, sep="")
```

Here we first make five different variables. We name them `valueA` through `valueE`. They have positive, negative, and floating-point values.

Then we raise each variable to a certain exponent with the `**` operator. Those exponents range from -5 to 4. We store the results in new variables (`aExp` through `eExp`).

The last bit of code outputs the original and exponentiated value with Python’s `print()` function. As we can see from the output, most results are as expected (although -0.250.125 returned a complex number):

```python
3^2 = 9
144^3 = 2985984
-987^4 = 949005240561
25^-5 = 1.024e-07
-0.25^0.125 = (0.7768869870150186+0.3217971264527913j)
```

### Calculate Exponents with `pow()`

Another way to exponentiate values is with the built-in `pow()` function (Python.org, n.d. a). This function accepts two arguments. The first is the base, or the number that we want to raise to a particular power. The second is the exponent to use. `pow()` always calculates an exact integer power.

So to calculate 3^2, we use the `pow()` function like this

```python
pow(3, 2)
# Returns: 9
```

> `pow()` can also accept three arguments. In that case the third argument specifies the modulo of the exponentiation. That returns the remainder of exponentiation. Using `pow()` in that way is more efficient than the equivalent `pow(base, exp) % mod`.

By the way, the `pow()` function returns a complex number when we use it with a non-integer exponent. This differs from the `math.pow()` function, which errors in that case.

Examples:

Let’s look at a Python program that uses the `pow()` function. The code below raises 5 different numbers to as many different exponents

```python
# Some random values
valueA = 3
valueB = 144
valueC = -987
valueD = 25
valueE = -0.25

# Raise the variables to different powers
aExp = pow(valueA, 2)
bExp = pow(valueB, 3)
cExp = pow(valueC, 4)
dExp = pow(valueD, -5)
eExp = pow(valueE, 0.125)

# Output results
print(valueA, "^2 = ", aExp, sep="")
print(valueB, "^3 = ", bExp, sep="")
print(valueC, "^4 = ", cExp, sep="")
print(valueD, "^-5 = ", dExp, sep="")
print(valueE, "^0.125 = ", eExp, sep="")
```

First we make five different variables. They are positive, negative, and there’s a floating-point value. We name those variables valueA through valueE.

Then we raise each variable to a particular power. For that we call the `pow()` function with two arguments. The first is the value to exponentiate, the second the exponent. We put the outcome that `pow()` returns in variables `aExp` through `eExp`.

Next several `print()` statements output both the original and `pow()`outcome. Of note is the complex number that `pow()` returned `for` -0.25^0.125:

```python
3^2 = 9
144^3 = 2985984
-987^4 = 949005240561
25^-5 = 1.024e-07
-0.25^0.125 = (0.7768869870150186+0.3217971264527913)
```

### Compute exponents with `math.pow()`

Python’s `math.pow()` function provides yet another way to multiply a number several times with itself. For that the function accepts two arguments: the base number and exponent.

So why another way to exponentiate values? What makes `math.pow()` different is that it converts both arguments to floating-point values (Python Docs, n.d. b). As a result, the function always returns a float. (For exact integer powers use the `pow()` function or the `**` operator discussed above.)

A quick example of `math.pow()` is:

```python
import math

math.pow(3, 2)
# Returns: 9.0
```

> Here’s how `math.pow()` handles uncommon cases. `math.pow(1.0, x)` and `math.pow(x, 0.0)` always return 1.0. That happens even when `x` is zero or NaN.

Also, `math.pow()` raises a `ValueError` exception when: both arguments are finite, the first argument is negative, or the second argument is not an integer

Example:

To see how the math.pow() function works in practice, let’s consider the following example program. The following code raises 5 different values to various powers with math.pow().

```python
import math

# Some numerical values
valueA = 3
valueB = 144
valueC = -987
valueD = 25
valueE = -0.25

# Raise each variable to a certain power
aExp = math.pow(valueA, 2)
bExp = math.pow(valueB, 3)
cExp = math.pow(valueC, 4)
dExp = math.pow(valueD, -5)
eExp = math.pow(valueE, -45)

# Output the results
print(valueA, "^2 = ", aExp, sep="")
print(valueB, "^3 = ", bExp, sep="")
print(valueC, "^4 = ", cExp, sep="")
print(valueD, "^-5 = ", dExp, sep="")
print(valueE, "^-45 = ", eExp, sep="")
```

Before we can use the math.pow() function we have to import the math module. Then we make five different variables, each with a numerical value. We name them valueA through valueE.

Next we raise each variable to a certain power. For that we call math.pow() with two arguments. The first is the variable we made earlier. The second a positive or negative exponent. We store the function’s outcome in new variables, aExp through eExp.

Then we output the original and exponentiated value with Python’s print() function. This is what that displays:

```python
3^2 = 9.0
144^3 = 2985984.0
-987^4 = 949005240561.0
25^-5 = 1.024e-07
-0.25^-45 = -1.2379400392853803e+27
```

[**_&#x25B2; Go to Overview_**](#overview)

## Logical Operators

Logical operators are used to construct more complex expressions. You can make complex comparisons by joining comparison statements together using the logical operators: `and`, `or`, `not`. Complex comparisons return a Boolean (`True` or `False`) result.

- and
  - Both sides of the statement being evaluated must be True `for` the whole statement to be True.

  - Example: (5 > 1 and 5 < 10) = True

- or
  - If either side of the comparison is True, then the whole statement is True.

  - Example: (color = "blue" or color = "green") = True

- not

  - Inverts the Boolean result of the statement immediately following it. So, if a statement evaluates to True, and we put the not operator in front of it, it would become False.

  - Example: (not "A" == "A") = False

[**_&#x25B2; Go to Overview_**](#overview)

### PART 1: The `and` Logical Operator

In Python, you can use the logical operator and to connect more than one comparison. This type of complex comparison is used to check if two comparison statements are both True or not. You might use the and operator when you need to execute a block of code, but only if two different conditions are true. For example, you might want to write a script  that automates sending you an emergency alert if a server stops responding and there is an unusual increase in employees opening trouble tickets.

**Example 1:**

The following model demonstrates the use of the `and` logical operator to join comparisons between two mathematical expressions. The description below the example explains the order in which Python will process the line of code.

```python
# Example 1

print((6*3 >= 18) and (9+9 <= 36/2))

# True
```

 In the example above, the following activities were completed by Python in the following order:

1. Python solves the numerical expressions using the order of operations. (6*3 >= 18) and (9+9 <= 36/2) becomes (18 >= 18) and (18 <= 18)

2. Python compares the results of the numerical expressions using the comparison operators (in this case >= and <=). (18 >= 18) and (18 <= 18) becomes True and True

3. Python checks if both sides of the logical operator "and" are true. True and True become True

4. Python returns a Boolean value: True or False. The complex comparison returns a True result.

**Example 2:**

In this next example, "Nairobi" < "Milan" and "Nairobi" > "Hanoi", the `and` logical operator is connecting two string comparison statements. You learned previously that using the greater than and less than operators on strings will test the alphabetical order (technically Unicode values) of the strings. So, this complex comparison is checking if "Nairobi" is alphabetized before "Milan" (False) AND after "Hanoi" (True).

This comparison returns a False result because both sides of the logical operator are not True. A comparison statement like this might be used to iterate through a list of names to check if they are alphabetized in the correct order.

```python
# Example 2

print("Nairobi" < "Milan" and "Nairobi" > "Hanoi")

# False
```

[**_&#x25B2; Go to Overview_**](#overview)

### PART 2: The or Logical Operator

The or logical operator tests two conditions to determine if at least one side of the or logical operator is True. The result of the test can be used to trigger a block of code if at least one condition is present.

**Syntax:**

```python
Expression1 or Expression2
```

| Expression1 | Expression2 | Returns Result |
|-------------|-------------|----------------|
| True        | True        | True           |
| True        | False       | False          |
| False       | True        | False          |
| False       | False       | False          |

**Example:**

```python
# Define country and city variables
country = "United States"
city = "New York City"

# True or True returns True
print((15/3 < 2+4) or (0 >= 6-7))  # True or True = True

# False or True returns True
print(country == "New York City" or city == "New York City")  # False or True = True

# True or False returns True
print(16 <= 4**2 or 9**(0.5) != 3)  # True or False = True

# False or False returns False
print("B_name" > "C_name" or "B_name" < "A_name") # False or False = False
```

[**_&#x25B2; Go to Overview_**](#overview)

### PART 3: The not Logical Operator

The `not` logical operator inverts the value of the comparison expression. This is a helpful tool when you want to execute a block of code as long as a certain condition is not present.

- If the conditional  expression is True, the `not` logical operator can be added to make the expression `not` True (False).

- If the conditional  expression is False, the `not` logical operator can be added to make the expression `not` False (True).

**Syntax:**

```python
not expression
```

**Example 1:**

```python
x = 2*3 > 6
print("The value of x is:")
print(x)

print("")  # Prints a blank line

print("The inverse value of x is:")
print(not x)
```

**Example 2:**

```python
# What happens when you negate a False statement?
# Click Run when you are ready to check your answer.


today = "Monday"
print(not today == "Tuesday")


# The "today" variable states today is Monday. This makes the comparison
# "today == Tuesday" False. The logical operator "not" inverts the False
# result to become True. In other words, this expression asks if it is
# false that today is not Tuesday. More succinctly, "not False" means
# True."
```

Key Takeways

When Python logical operators are used with comparison operators, the interpreter will return Boolean results (`True` or `False`):

| Expression          | Description                                           |
|---------------------|-------------------------------------------------------|
| a **==** a and a **!=** b  | True if both sides are True, otherwise False.        |
| a **>** b or a **<=** c    | True if either side is True. False if both sides are False. |
| **not** a **==** b         | True if the statement is False, False if the statement is True. |

[**_&#x25B2; Go to Overview_**](#overview)

## Conditionals

### If

Runs the code if the condition given is true, For Example:

```python
name = "Raj"

if name == "Raj":
  print("Hello Raj, it's a great name")
```

[**_&#x25B2; Go to Overview_**](#overview)

### Else

Runs the code if the other conditions that are given are not true

```python
name = "Raj"
time = 10

if time > 8 and time < 15:
  print(f"Good Morning {name}")
else:
  print("Good Evening")
```

You can also use the if and else statements combined with other code to make complex things, For example:

```python
name1 = input("what is your name?")
name2 = input("what is your partner's or crush's name?")

combinedName = name1 + name2
lowerNames = combinedName.lower()

t = lowerNames.count("t")
r = lowerNames.count("r")
u = lowerNames.count("u")
e = lowerNames.count("e")

firstLetter = t + r + u + e

l = lowerNames.count("l")
o = lowerNames.count("o")
v = lowerNames.count("v")
e = lowerNames.count("e")
secondLetter = l + o + v + e

score = int(str(firstLetter) + str(secondLetter))


if score < 10 or score > 90:
  print(f"Your score is {score}, you go together like coke and mentos.")
else:
  print(f"Your score is {score}.")
```

[**_&#x25B2; Go to Overview_**](#overview)

### Elif

Used to add multiple conditions (Greater than 2)

```python
name = "Sahil"

if name == "Raj":
  print("Hello Raj")
elif name == "Sahil":
  print("Hello Sahil")
else:
  print("Hello")

# Please note that I can print the name directly by using print(f" Hello {name}"), but this is just to explain at a simple level
```

Below is a tressure hunt game made using this statements

```python
print("Welcome to Treasure Island, your mission is to find the treasure.")

q1 = input("You're at a cross road. Where do you want to go? Type \"left\" or \"right\". ").lower()

if q1 == "left":
    q2 = input('You are near a river, What would you like to do? Type "swim" or "wait".').lower()
    if q2 == "wait":
        q3 = input('Now there are three doors in front of you, which one will you choose? Type "Red", "Yellow" or "Blue".').lower()
        if q3 == "yellow":
            print("Congratulations, you win the treasure!")
        elif q3 == "red":
            print("You got burned by fire, Game Over!")
        elif q3 == "blue":
            print("You got eaten by beasts, Game Over!")
        else:
            print("Game Over")
    elif q2 == "swim":
        print("You got attacked by trout, Game Over!")
    else:
        print("Game Over!")
elif q1 == "right":
    print("You fall into a hole, Game Over!")
else:
    print("Game Over")
```

[**_&#x25B2; Go to Overview_**](#overview)

## Random Module

The random module is used to generate random integers and decimals. You can use it by importing it into your code by using the `import` statement

```python
import random

randomNumber = random.randint(0, 5)
#The above code will generate random integer from 0 to 5, you can also replace them as you wish
```

By this you can also create a small heads or toss probability game.

```python
import random

coinToss = random.randint(0, 1)

if coinToss == 1:
    print("Heads")
else:
    print("Tails")

```

You can also generate ramdom float number by using the random.random. The below code will print from `[0, 1)`

```python
import random

number = random.random
print(number)

# This will print any random number from 0 till 1 (1 not included)
```

You can learn more about it by [Clicking Here](https://www.askpython.com/?s=random+module)

[**_&#x25B2; Go to Overview_**](#overview)

## Loops

### For Loop

A `for` loop is used `for` iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

This is less like the `for` keyword in other programming languages, and works more like an iterator method as found in other object-orientated programming languages.
With the `for` loop we can execute a set of statements, once `for` each item in a list, tuple, set etc.

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)

# This will print out each item in the list
```

You can also loop through strings too print out all the word in an order, for example

```python
for x in "banana":
  print(x)
```

You can also use for loop with in range to do the task for a particular number of times, for example

```python
for k in range(0, 8):
  print(k)
# This will print out k from 0 to 7
```

[**_&#x25B2; Go to Overview_**](#overview)

### While Loop

While loop operates somewhat similar to for loop, but it takes a condition to work first, for example:

```python
total = 5

while total > 0:
  print(total) # This loop will run whenever the total is greater than 0
  total -= 1 # This will subtract one each time the loop runs.

# This will print number from 5 to 1, and when the total becomes 0, the while loop will stop running.
```

[**_&#x25B2; Go to Overview_**](#overview)

### Nested Loops

[**_&#x25B2; Go to Overview_**](#overview)
