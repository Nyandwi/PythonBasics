# Basic of Python Programming Language

*[Status: Under Revision]*

This is a practical introduction to Python Programming Language. Python is an interpreted, high-level, and general purpose programming language that was designed for efficiency, readability, and simplicity.

Python design philosophy emphasizes simplicity and code readability. There are about 19 Python design guiding principles, the top 5 being:

* Beautiful is better than ugly. 
* Explicit is better than implicit
* Simple is better than complex
* Complex is better than complicated
* Readability counts
* Now is better than ever
* If the implementation is hard to explain, it's a bad idea.
* If the implementation is easy to explain, it may be a good idea.

More design rules can be found in the [Zen of Python](https://en.wikipedia.org/wiki/Zen_of_Python). You can also display them by importing this(`import this`) in any Python interpreter. 
```
import this
>>> The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!

```

Python is a popular and go-to programming language in different tech communities, most notable in machine learning and data science. It is sometimes referred to as [“batteries included”](https://docs.python.org/3/tutorial/stdlib.html) due to its rich standard library. Below are more elaborated advantages of Python:

* It is simple to read and write: Python syntaxes are very easy to write and easy to recall as well. 
* It has a beautiful design and built-in data types. 
* It has thousands of great libraries in many disciplines.
* Supportive communities: Good documentation, courses, tutorials, social groups.
* Easy to learn and use due to its simple syntaxes which feel like a natural language. 

This introduction will cover the following: 

* [1. Variables, Numbers and Strings](#1)
    * [1.1 Numbers](#1-1)
    * [1.2 Strings](#1-2)
* [2. Data Structures](#2)
    * [2.1 Lists](#2-1)
    * [2.2 Dictionaries](#2-2)
    * [2.3 Tuples](#2-3)
    * [2.4 Sets](#2-4)
* [3. Comparison and Logic Operators](#3)
* [4. Control Flow](#4)
    * [4.1 If Condition](#4-1)
    * [4.2 For Loop](#4-2)
    * [4.3 While Loop](#4-3)
* [5. Functions](#5)
* [6. Lambda Functions](#6)
* [7. Built in functions](#7)
    * [7.1 Map Function](#7-1)
    * [7.2 Filter Function](#7-2)

* [8. More Useful Python Functions](#8)
    * [8.1 List Comprehension](#8-1)
    * [8.2 Enumerate Function](#8-2)
    * [8.3 Zip Function](#8-3)

## 1. Variables, Numbers, and Strings

### 1.1 Variables

Below are quick notes about Python variables and other most important things to know before writing actual Python code:

* `A Variable` is a location in memory where we store the data. 
* `A variable` in Python can either be of 3 data types: `integer`, `float`, or a `string`.  Data type specifies the category of the variables.
* We can use `type(variable_name)` to find the type of given `variable_name`.
* In Python, we use `#` to add `comments`. Comments do not change anything and are not compiled.
* If your comment is longer than one line, you can use triple quotes. The lines inside triple quotes are ignore during runtime.

```
"""
In Python, there is no official way to write long comments, but you can use triple quotes.
The sentence between triple quote are ignored at runtime. You can also use single quote('''....'''). Python treats single quote as double quotes in many scanerios such as strings representation.

Guido also agreed it works: https://twitter.com/gvanrossum/status/112670605505077248 
"""
```

* We also use `=` to assign a value to the name of variable. Example: `var_name = 1`. Note that it's different to comparison operator of equal to (`==`).
* We can use `print()` to display the value of variable or the results of any expression.
* Each line of the code start on the new line.
* Be aware of indentations. Python is serious about them.
```
# EXAMPLE OF CREATING A VARIABLE

# We use # to add comment, it won’t run or affect the code
# You use = to assign a value to the name of the variable. 
# Each code starts on the new line. No semicolon or {}
# Python is awesome. You do not need to provide the data type of variable when creating it.

int_var = 1
str_var = 'Hundred'
```
### 1.2 Numbers

Numbers in Python can either be integers `int` or floats `float`. Integer are real, finite, natural or whole numbers. Take an example: `1`,`2`,`3`,`4` are integers. Floats are numbers that have decimal points such as`4.6`, `6.0`, `7.7`. Note that `4.0` is considered as a float data type too. Recently, Karpathy, AI Director at Tesla posted that [floats are not real](https://twitter.com/karpathy/status/1475317897660612617).

We can perform operations on numbers. The operations that we can perform include addition, multiplication, division, modular, etc...

```
int_var = 10
float_var = 12.8

type(int_var)
>>> int
```
```
type(float_var)
>>> float
```

#### Numeric Operations 

```
# Addition

1 + 100
>>> 101
```
```
# Multiplication

1 * 100
>>> 100
```
```
# Division

1 / 100
>>> 0.01

# Floor division 
7 / 2
>>> 3
```
```
# Modular (%)
# This is the remainder or a value remaining after dividing two numbers
# 100 / 1 = 100, remainder is 0

100 % 1
>>> 0

1 % 100
>>> 1

10 % 2
>>> 0
```
```
# Powers
# 1 power any number is 1 always

1 ** 100
>>> 1

2 ** 2
>>> 4
```
```
# We use print() to display the results of the operations or a variable

print(1 + 100)
>>> 101
```

### 1.3 Strings

Python supports strings. Strings are one of the commonly used and important data types. Most problems involve working with strings. Thus, knowing how to work with strings is an incredible thing.

Strings are expressed in either `"..."` or `'...'`.

```
"text inside here will be a string"
'text inside here will also be a string'
```

We can manipulate strings in many ways. A simple example is to concat the strings. 

```
str_var = 'One'
str_var2 = 'Hundred'

>>> 'OneHundred'
```
```
str_var + ' ' + 'and' + ' '+ str_var2+ '.'
>>> 'One and Hundred.'
```

```
## We can use print() to display a string

>>> print(" This is a string")
```

#### Strings Methods

Python provides many built-in methods for manipulating strings. As a programmer, knowing typical string methods and how to use them will give you a real leverage when working with strings.

There are many string methods. You can find them [here](https://docs.python.org/2.5/lib/string-methods.html). Let's see some common methods.
```
sentence = 'This IS A String'
>>> 'This is a string'
```

```
# Given a string, convert it into title (each word is capitalized)

# Given a string, convert it into title (each word is capitalized)

sentence_2 = 'this is a string to be titled'
sentence_2.title()
>>> 'This Is A String To Be Titled'
```

```
# Converting the string to upper case

sentence.upper()
>>> 'THIS IS A STRING'
```
```
# Converting the string to upper case

sentence.lower()
>>> 'this is a string'
```
```
# Splitting the string

sentence.split()
>>> ['This', 'IS', 'A', 'String']
```
Lastly, we can use `replace()` method to replace some characters in string with another characters. Replace method takes two inputs: characters to be replaced, and new characters to be inserted in string, `replace('characters to be replaced', 'new characters')`. 

Example, given the string "This movie was awesome", replace the world `movie` with `project`.  

```
stri = "This movie was awesome"
stri.replace('movie', 'project')
>>> 'This project was awesome'
```
```
# In the following string, replace all spaces with `%20'

stri_2 = "The future is great"
stri_2.replace(' ', '%20')
```
As you can see, strings methods are powerful and can save you time. Remember one of the Python philosophies that we saw in the beginning: `Simple is better than complex`.
