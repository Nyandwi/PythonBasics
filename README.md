<a name='0'></a>
# Basic of Python Programming Language


This is a practical introduction to Python Programming Language. The style of this repo was inspired by [Chip Huyen Cool Python repo](https://github.com/chiphuyen/python-is-cool). You can find the companion notebook [here](https://github.com/Nyandwi/python_basics/blob/main/python-basics.ipynb). For advanced Python concepts, check [this repo](https://github.com/Nyandwi/PythonPro)(work in progress)!

Python is an interpreted, high-level, and general purpose programming language that was designed for efficiency, readability, and simplicity.

Python design philosophy emphasizes simplicity and code readability. There are about 19 Python design guiding principles, the top 8 being:

* Beautiful is better than ugly. 
* Explicit is better than implicit
* Simple is better than complex
* Complex is better than complicated
* Readability counts
* Now is better than ever
* If the implementation is hard to explain, it's a bad idea.
* If the implementation is easy to explain, it may be a good idea.

More design rules can be found in the [Zen of Python](https://en.wikipedia.org/wiki/Zen_of_Python). You can also display them by importing this(`import this`) in any Python interpreter. 


```python
import this
```

    The Zen of Python, by Tim Peters
    
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


Python is a popular and go-to programming language in different tech communities, most notable in machine learning and data science. It is sometimes referred to as [“batteries included”](https://docs.python.org/3/tutorial/stdlib.html) due to its rich standard library. Below are more elaborated advantages of Python:

* It is simple to read and write: Python syntaxes are very easy to write and easy to recall as well. 
* It has a beautiful design and built-in data types. 
* It has thousands of great libraries in many disciplines.
* Supportive communities: Good documentation, courses, tutorials, social groups.
* Easy to learn and use due to its simple syntaxes which feel like a natural language. 

This introduction will cover the following: 

* [1. Variables, Numbers and Strings](#1)
    * [1.1 Variables](#1-1)
    * [1.2 Numbers](#1-2)
    * [1.3 Strings](#1-3)
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

*******************
<a name='1'></a>

## 1. Variables, Numbers, and Strings

<a name='1-1'></a>


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


```python
# EXAMPLE OF CREATING A VARIABLE

# We use # to add comment, it won’t run or affect the code
# You use = to assign a value to the name of the variable. 
# Each code starts on the new line. No semicolon or {}
# Python is awesome. You do not need to provide the data type of variable when creating it.

int_var = 1
str_var = 'Hundred'
```
*******************
<a name='1-2'></a>

### 1.2 Numbers

Numbers in Python can either be integers `int` or floats `float`. Integer are real, finite, natural or whole numbers. Take an example: `1`,`2`,`3`,`4` are integers. Floats are numbers that have decimal points such as`4.6`, `6.0`, `7.7`. Note that `4.0` is considered as a float data type too. Recently, Karpathy, AI Director at Tesla posted that [floats are not real](https://twitter.com/karpathy/status/1475317897660612617).

We can perform operations on numbers. The operations that we can perform include addition, multiplication, division, modular, etc...


```python
int_var = 10
float_var = 12.8

type(int_var)
```




    int




```python
type(float_var)
```




    float




```python
# Numeric Operations 

# Addition

1 + 100
```




    101




```python
# Multiplication

1 * 100
```




    100




```python
# Division

1 / 100
```




    0.01




```python
# Floor division

7 // 2
```




    3




```python
# Modular (%)
# This is the remainder or a value remaining after dividing two numbers
# 100 / 1 = 100, remainder is 0

100 % 1
```




    0




```python
1 % 100
```




    1




```python
10 % 2
```




    0




```python
# Powers
# 1 power any number is 1 always

1 ** 100
```




    1




```python
2 ** 2
```




    4




```python
# We use print() to display the results of the operations or a variable

print(1 + 100)
```

    101

*******************
<a name='1-3'></a>

### 1.3 Strings

Python supports strings. String is a sequence of characters. 

Strings are one of the commonly used and important data types. Most problems involve working with strings. Thus, knowing how to work with strings is an incredible thing.

Strings are expressed in either `"..."` or `'...'`.

```
"text inside here will be a string"
'text inside here will also be a string'
```

We can manipulate strings in many ways. A simple example is to concat the strings. 


```python
str_var = 'One'
str_var2 = 'Hundred'
```


```python
str_var + str_var2
```




    'OneHundred'




```python
str_var + ' ' + 'and' + ' '+ str_var2 + '.'
```




    'One and Hundred.'




```python
# We can use print() to display a string

print(" This is a string")
```

     This is a string



```python
# We can also compare strings to check whether they are similar. 
# If they are similar, case by case, comparison operator returns true. Else false

"A string" == "a string"
```




    False




```python
"A string" == "A string"
```




    True


#### Strings Methods

Python provides many built-in methods for manipulating strings. As a programmer, knowing typical string methods and how to use them will give you a real leverage when working with strings.

There are many string methods. You can find them [here](https://docs.python.org/2.5/lib/string-methods.html). Let's see some common methods.


```python
sentence = 'This IS A String'
```


```python
# Case capitalization 
# It return the string with first letter capitalized and the rest being lower cases. 

sentence.capitalize()
```




    'This is a string'




```python
# Given a string, convert it into title (each word is capitalized)

sentence_2 = 'this is a string to be titled'
sentence_2.title()
```




    'This Is A String To Be Titled'




```python
# Converting the string to upper case

sentence.upper()
```




    'THIS IS A STRING'




```python
# Converting the string to upper case

sentence.lower()
```




    'this is a string'




```python
# Splitting the string

sentence.split()
```




    ['This', 'IS', 'A', 'String']



Lastly, we can use `replace()` method to replace some characters in string with another characters. Replace method takes two inputs: characters to be replaced, and new characters to be inserted in string, `replace('characters to be replaced', 'new characters')`. 

Example, given the string "This movie was awesome", replace the world `movie` with `project`. 


```python
stri = "This movie was awesome"
stri.replace('movie', 'project')
```




    'This project was awesome'




```python
# In the following string, replace all spaces with `%20'

stri_2 = "The future is great"
stri_2.replace(' ', '%20')
```




    'The%20future%20is%20great'



As you can see, strings methods are powerful and can save you time. Remember one of the Python philosophies that we saw in the beginning: `Simple is better than complex`. 

<a name='2'></a>
## 2. Data Structures

Data structures are used to organize and store the data. Algorithms supports operations on data.

Python has 4 main data structures: `Lists`, `Dictionaries`, `Tuples` and `Sets`. 

*******************
<a name='2-1'></a>

### 2.1 List

A list is a set of ordered values. Each value in a list is called an `element` or `item` and can be identified by an index. A list supports different data types, we can have a list of integers, strings, and floats. 

What we will see with Python lists:

- Creating a list
- Accessing elements in a list
- Slicing a list
- Changing elements in a list
- Traversing a list
- Operations on list
- Nested lists
- List methods
- List and strings

#### Creating a List

A python list can be created by enclosing elements of similar or different data type in square brackets `[...]`, or with `range()` function.


```python
# Creating a list

week_days = ['Mon', 'Tue', 'Wed', 'Thur','Fri']
even_numbers = [2, 4, 6, 8, 10]
mixed_list = ['Mon', 1, 'Tue', 2, 'Wed', 3]

# Displaying elements of a list
print(week_days)
```

    ['Mon', 'Tue', 'Wed', 'Thur', 'Fri']



```python
# Creating a list with range()

nums = range(5)

for i in nums:
    print(i)
```

    0
    1
    2
    3
    4


#### Accessing the elements of the list

We can access the a given element of the list by providing the index of the element in a bracket. The index starts at 0 in Python.


```python
# Accessing the first elements of the list

week_days[0]
```




    'Mon'




```python
even_numbers[2]
```




    6




```python
# Getting the last element of the list

print(even_numbers[-1])
```

    10


#### Slicing a list

Given a list, we can slice it to get any parts or combination of its elements forming another list.


```python
# Get the elements from index 0 to 2. Index 2 is not included.

week_days = ['Mon', 'Tue', 'Wed', 'Thur','Fri']
week_days[0:2]
```




    ['Mon', 'Tue']




```python
# Get elements from the last fourth elements to the first
# -1 starts at the last element 'Fri', -2 second last element `Thur'..... -4 to 'Tue'

week_days[-4:]
```




    ['Tue', 'Wed', 'Thur', 'Fri']




```python
# Get all elements up to the fourth index

week_days[:4]
```




    ['Mon', 'Tue', 'Wed', 'Thur']




```python
# Get all elements from the second to the last index

week_days[2:]
```




    ['Wed', 'Thur', 'Fri']



You can use `[:]` to copy the entire list. 


```python
week_days[:]
```




    ['Mon', 'Tue', 'Wed', 'Thur', 'Fri']



#### Changing elements in a list

Python lists are mutable. We can delete or change the elements of the list.


```python
names = ['James', 'Jean', 'Sebastian', 'Prit']
names
```




    ['James', 'Jean', 'Sebastian', 'Prit']




```python
# Change 'Jean' to 'Nyandwi' and 'Sebastian' to 'Ras'

names[1:3] = ['Nyandwi', 'Ras']
names
```




    ['James', 'Nyandwi', 'Ras', 'Prit']




```python
# Change 'Prit' to Sun

names[-1] = 'Sun'
names
```




    ['James', 'Nyandwi', 'Ras', 'Sun']




```python
# Change `James` to ``Francois`

names[0] = 'Francois'
names
```




    ['Francois', 'Nyandwi', 'Ras', 'Sun']



In order to delete a given element in a list, we can empty slice it but the better way to delete element is to use `del` keyword.


```python
# Delete Nyandwi in names list

del names[1]
names
```




    ['Francois', 'Ras', 'Sun']



If you know the index of the element you want to remove, you can use `pop()`. If you don't provide the index in pop(), the last element will be deleted.


```python
names = ['James', 'Jean', 'Sebastian', 'Prit']
names.pop(2)
names
```




    ['James', 'Jean', 'Prit']



Also, we can use `remove()` to delete the element provided inside the remove() method.


```python
names = ['James', 'Jean', 'Sebastian', 'Prit']
names.remove('James')
names
```




    ['Jean', 'Sebastian', 'Prit']



We can also use `append()` to add element to the list.


```python
# Adding the new elements in list

names = ['James', 'Jean', 'Sebastian', 'Prit']
names.append('Jac')
names.append('Jess')
names
```




    ['James', 'Jean', 'Sebastian', 'Prit', 'Jac', 'Jess']



#### Traversing a list

There are times that we may need to go over the list to read the elements of the list or perform iterative operations. We can use `for loop` to traverse through the list.


```python
# Given a list names, use for loop to display its elements

names = ['James', 'Jean', 'Sebastian', 'Prit']

for name in names:
    print(name)
```

    James
    Jean
    Sebastian
    Prit



```python
# Given a list nums, add 1 to the first element, 2 to the second, 3 to 3rd element, 4 to 4th element
# Example: nums = [1,2,3,6] will be nums_new = [2,4,6,10]

nums = [1, 2, 3, 6]
nums_new = []

for i in range(len(nums)): #len(nums) gives the length of the list
    num = nums[i] + i + 1
    nums_new.append(num)
    
nums_new
```




    [2, 4, 6, 10]



#### Operations on list


```python
# Concatenating two lists

a = [1,2,3]
b = [4,5,6]

c = a + b

c
```




    [1, 2, 3, 4, 5, 6]




```python
# We can also use * operator to repeat a list a number of times

[None] * 5
```




    [None, None, None, None, None]




```python
[True] * 4
```




    [True, True, True, True]




```python
[1,2,4,5] * 2
```




    [1, 2, 4, 5, 1, 2, 4, 5]



#### Nested lists


```python
# Creating a list in other list

nested_list = [1,2,3, ['a', 'b', 'c']]


# Get the ['a', 'b', 'c'] from the nested_list

nested_list[3]
```




    ['a', 'b', 'c']




```python
# Indexing and slicing a nested list is quite similar to normal list

nested_list[1]
```




    2



#### List Methods

Python also offers methods which make it easy to work with lists. We already have been using some list methods such as `pop()` and `append()` but let's review more other methods.


```python
# Sorting a list with sort()

even_numbers = [2,14,16,12,20,8,10]

even_numbers.sort()

even_numbers
```




    [2, 8, 10, 12, 14, 16, 20]




```python
# Reversing a string with reverse()

even_numbers.reverse()
even_numbers
```




    [20, 16, 14, 12, 10, 8, 2]




```python
# Adding other elements to a list with append()

even_numbers = [2,14,16,12,20,8,10]

even_numbers.append(40)
even_numbers
```




    [2, 14, 16, 12, 20, 8, 10, 40]




```python
# Removing the first element of a list

even_numbers.remove(2)
even_numbers
```




    [14, 16, 12, 20, 8, 10, 40]




```python
## Return the element of the list at index x

even_numbers = [2,14,16,12,20,8,10]

## Return the item at the 1st index

even_numbers.pop(1)
```




    14




```python
# pop() without index specified will return the last element of the list

even_numbers = [2,14,16,12,20,8,10]
even_numbers.pop()
```




    10




```python
# Count a number of times an element appear in a list

even_numbers = [2,2,4,6,8]
even_numbers.count(2)
```




    2



#### List and strings

We previously have learned about strings. Strings are sequence of characters. List is a sequence of values. 


```python
# We can convert a string into list

stri = 'Apple'

list(stri)
```




    ['A', 'p', 'p', 'l', 'e']




```python
# Splitting a string produces a list of individual words

stri_2 = "List and Strings"
stri_2.split()
```




    ['List', 'and', 'Strings']



The split() string method allows to specify the character to use a a boundary while splitting the string. It's called delimiter.


```python
stri_3 = "state-of-the-art"

stri_3.split('-')
```




    ['state', 'of', 'the', 'art']


*******************
<a name='2-2'></a>

### 2.2 Dictionaries

Dictionaries are powerful Python builtin data structure that are used to store data of key and values. A dictionary is like a list but rather than using integers as indices, indices in dictionary can be any data type. Also, unlike lists, dictionary are unordered. Dictionaries dont guarrantee keeping the order of the data.

Generally, a dictionary is a collection of key and values. A dictionary stores a mapping of keys and values. A key is what we can refer to index.

What we will see:

- Creating a dictionary
- Accessing values and keys in dictionary
- Solving counting problems with dictionary
- Traversing a dictionary
- The setdefault() method

#### Creating a dictionary

We can create with a `dict()` function and add items later, or insert keys and values right away in the curly brackets { }. Let's start with dict() function to create an empty dictionary. 


```python
# Creating a dictionary

countries_code = dict()
print(countries_code)
```

    {}


You can verify it's a dictionary by passing it through `type()`.


```python
type(countries_code)
```




    dict



Let's add items to the empty dictionary that we just created.


```python
# Adding items to the empty dictionary.

countries_code["United States"] = 1
```


```python
countries_code
```




    {'United States': 1}



Let's create a dictionary with {}. It's the common way to create a dictionary.


```python
countries_code = { 
        "United States": 1,
        "China": 86,
        "Rwanda":250,
        "Germany": 49,
        "India": 91,
}

countries_code
```




    {'United States': 1, 'China': 86, 'Rwanda': 250, 'Germany': 49, 'India': 91}



To add key and values to a dictionary, we just add the new key to [ ] and set its new value. See below for example...


```python
countries_code['Australia'] = 61
countries_code
```




    {'United States': 1,
     'China': 86,
     'Rwanda': 250,
     'Germany': 49,
     'India': 91,
     'Australia': 61}



#### Accessing the values and keys in a dictionary

Just like how we get values in a list by using their indices, in dictionary, we can use a key to get its corresponding value.


```python
# Getting the code of Rwanda

countries_code["Rwanda"]
```




    250



We can also check if a key exists in a dictionary by using a classic `in` operator.


```python
"India" in countries_code 
```




    True




```python
# Should be False

"Singapore" in countries_code
```




    False



To get all the keys, value, and items of the dictionary, we can respectively use `keys()`, `values()`, and `items()` methods.


```python
# Getting the keys and the values and items of the dictionary

dict_keys = countries_code.keys()
dict_values = countries_code.values()
dict_items = countries_code.items()

print(f"Keys: {dict_keys}\n Values:{dict_values}\n Items:{dict_items}")
```

    Keys: dict_keys(['United States', 'China', 'Rwanda', 'Germany', 'India', 'Australia'])
     Values:dict_values([1, 86, 250, 49, 91, 61])
     Items:dict_items([('United States', 1), ('China', 86), ('Rwanda', 250), ('Germany', 49), ('India', 91), ('Australia', 61)])


Lastly, we can use `get()` method to return the value of a specified key. Get method allows to also provide a value that will be returned in case the key doesn't exists. This is a cool feature!!


```python
# Get the value of the Australia

countries_code.get('Australia')
```




    61




```python
# In case a provided key is absent....

countries_code.get('UK', 41)
```




    41



#### Solving counting problems with dictionary

When solving real world problems, or perhaps doing interviews, most problems involve counting certain elements. Let's take a simple example: Given a string, write an algorithm that can count the occurence of each character. 

**Solution:**

The first approach would be to create a list of 128 elements given that the standard size of characters in ASCII is 128, convert each character to a number with `ord()` method(`char()` convert from number to string), use the number as the index of the string, and then increment it as you see a recurring character. The code would like like this....


```python
stri = 'aaaaajjj222@@@sss^^^888'

counts = [0] * 128 # Create a list of 128 elements, initially each character count is 0. 

for c in stri:
    c_num = ord(c)
    
    counts[c_num] = counts[c_num] + 1
        
counts
```




    [0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     3,
     0,
     0,
     0,
     0,
     0,
     3,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     3,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     3,
     0,
     0,
     5,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     3,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     3,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0,
     0]



Using dictionary, we would not have to worry about the size of the string or the nmber of characters to keep beforehand. We would just create a dictionary whose keys are characters and values are counts of corresponding characters. See character for the first time, add it to the dictionary with value of 1 since it's the first count, and then increment it if the character exists in dictionary.


```python
stri = "jdjjdjdjdjjdjdjdj"

counts_dict = {}

for c in stri:
    if c not in counts_dict:
        counts_dict[c] = 1
    
    else:
        counts_dict[c] += 1
        
print(counts_dict)
```

    {'j': 10, 'd': 7}


Also, we can use `get()` method that we saw above to simplify our solution. To make it a bit fancier, let's also assume that the string will be provided by the user at the beginning of the program.


```python
stri = input(str) #input must be a string

char_count = {}

for c in stri:
    char_count[c] = char_count.get(c,0) + 1
    
print(char_count)
```

    <class 'str'>ABBABABSHHSSH
    {'A': 3, 'B': 4, 'S': 3, 'H': 3}


#### Traversing a dictionary

We previously used for loop in dictionary to iterate through the values. Let's review it again.


```python
countries_code
```




    {'United States': 1,
     'China': 86,
     'Rwanda': 250,
     'Germany': 49,
     'India': 91,
     'Australia': 61}




```python
for country in countries_code:
    print(country)
```

    United States
    China
    Rwanda
    Germany
    India
    Australia


We can also iterate through the items(key, values) of the dictionary.


```python
for country, code in countries_code.items():
    print(country, code)
```

    United States 1
    China 86
    Rwanda 250
    Germany 49
    India 91
    Australia 61


#### The setdefault() Method

The setdefault() method allows you to set a value of a given key that does not already have a key. This can be helpful when you want to update the dictionary with a new value in case the key you are looking for does not exist.


```python
countries_code.setdefault("UK", 41)
```




    41




```python
countries_code
```




    {'United States': 1,
     'China': 86,
     'Rwanda': 250,
     'Germany': 49,
     'India': 91,
     'Australia': 61,
     'UK': 41}



Cool! The UK value is added to the dictionary because it was not in the dictionary before. The setdefault() method and get() method are different.

We can also use the setdefault() in the count program we wrote above.


```python
stri = input(str) #input must be a string

char_count = {}

for c in stri:
    char_count.setdefault(c,0) #If character doesn't exist in char_count, add it and set it to 0
    char_count[c] += 1
    
print(char_count)
```

    <class 'str'>AAAHHSHSHS
    {'A': 3, 'H': 4, 'S': 3}


***Summarizing dictionary***

* Dictionaries are not ordered and they can not be sorted - list are ordered (and unordered) and can be sorted.

* Dictionary can store data of different types: floats, integers and strings and can also store lists. 

*******************
<a name='2-3'></a>

### 2.3 Tuples

Tuple is similar to list but the difference is that you can't change the values once it is defined (termed as `immutability`). Due to this property it can be used to keep things that you do not want to change in your program. Example can be a country codes, zipcodes, etc...




```python
tup = (1,4,5,6,7,8)
```


```python
# Indexing

tup[4]
```




    7




```python
## Tuples are not changeable. Running below code will cause an error

# tup[2] = 10
```


```python
# You can not also add other values to the tuple. This will be error
#tup.append(12)
```

<a name='2-4'></a>

### 2.4 Sets

Sets are used to store the unique elements. They are not ordered like list. 


```python
set_1 = {1,2,3,4,5,6,7,8}

set_1
```




    {1, 2, 3, 4, 5, 6, 7, 8}




```python
set_2 = {1,1,2,3,5,3,2,2,4,5,7,8,8,5}
set_2
```




    {1, 2, 3, 4, 5, 7, 8}



As you can see, set only keep unique values. There can't be a repetition of values. 


```python
# List Vs Set

odd_numbers = [1,1,3,7,9,3,5,7,9,9]

print("List:{}".format(odd_numbers))

print("********")

set_odd_numbers = {1,1,3,7,9,3,5,7,9,9}

print("Set:{}".format(set_odd_numbers))
```

    List:[1, 1, 3, 7, 9, 3, 5, 7, 9, 9]
    ********
    Set:{1, 3, 5, 7, 9}

*******************
<a name='3'></a>

## 3. Comparison and Logic operators

`Comparison` operators are used to compare values. It will either return true or false. 


```python
## Greater than 
100 > 1
```




    True




```python
## Equal to

100 == 1
```




    False




```python
## Less than

100 < 1
```




    False




```python
## Greater or equal to

100 >= 1
```




    True




```python
## Less or equal to

100 <= 1
```




    False




```python
'Intro to Python' == 'intro to python'
```




    False




```python
'Intro to Python' == 'Intro to Python'
```




    True



`Logic` operators are used to compare two expressions made by comparison operators. 

* Logic `and` returns true only when both expressions are true, otherwise false. 

* Logic `or` returns true when either any of both expressions is true. Only false if both expressions are false.

* Logic `not` as you can guess, it will return false when given expression is true, vice versa. 


```python
100 == 100 and 100 == 100
```




    True




```python
100 <= 10 and 100 == 100
```




    False




```python
100 == 10 or 100 == 100
```




    True




```python
100 == 10 or 100 == 10
```




    False




```python
not 1 == 2
```




    True




```python
not 1 == 1
```




    False


*******************
<a name='4'></a>
## 4. Control Flow
As an engineer, you will need to make decisions depending on the particular situation. You will also need to control the flow of the program and this is where `Control Flow` comes in. 

We will cover:

* If statement
* For loop
* While loop


*******************
<a name='4-1'></a>

### 4.1 If, Elif, Else



Structure of If condition:

```
if condition:
  do something

else:
  do this
```



```python
if 100 < 2:

  print("As expected, no thing will be displayed")
```


```python
if 100 > 2:

  print("As expected, no thing will be displayed")
```

    As expected, no thing will be displayed



```python
if 100 < 2:

  print("As expected, no thing will be displayed")

else:
  print('Printed')
```

    Printed



```python
# Let's assign a number to a variable name 'jean_age' and 'yannick_age'

john_age = 30
luck_age = 20

if john_age > luck_age:
  print("John is older than Luck")

else:
  print(" John is younger than Luck")
```

    John is older than Luck



```python
# Let's use multiple conditions 

john_age = 30
luck_age = 20
yan_age = 30

if john_age < luck_age:
  print("John is older than Luck")

elif yan_age == luck_age:
  print(" Yan's Age is same as Luck")

elif luck_age > john_age:
  print("Luck is older than John")

else:
  print("John's age is same as Yan")
```

    John's age is same as Yan


We can also put if condition into one line of code. This can be useful when you want to make a quick decision between few choices. 

Here is the structure:

`'value_to_return_if_true' if condition else 'value_to_return_if_false'`

Let's take some examples...


```python
# Example 1: Return 'Even' if below num is 'Even' and `Odd` if not. 

num = 45

'Even' if num % 2 == 0 else 'Odd'
```




    'Odd'




```python
# Example 2: Return True if a given element is in a list and False if not

nums = [1,2,3,4,5,6]

True if 3 in nums else False
```




    True



<a name='4-2'></a>
### 4.2 For Loop

For loop is used to iterate over list, string, tuples, or dictionary. 

Structure of for loop:

```
for item in items:
  do something
```




```python
even_nums = [2,4,6,8,10]

for num in even_nums:
  print(num)
```

    2
    4
    6
    8
    10



```python
week_days = ['Mon', 'Tue', 'Wed', 'Thur','Fri']

for day in week_days:
  print(day)
```

    Mon
    Tue
    Wed
    Thur
    Fri



```python
sentence = "It's been a long time learning Python. I am revisiting the basics!!"

for letter in sentence:
  print(letter)
```

    I
    t
    '
    s
     
    b
    e
    e
    n
     
    a
     
    l
    o
    n
    g
     
    t
    i
    m
    e
     
    l
    e
    a
    r
    n
    i
    n
    g
     
    P
    y
    t
    h
    o
    n
    .
     
    I
     
    a
    m
     
    r
    e
    v
    i
    s
    i
    t
    i
    n
    g
     
    t
    h
    e
     
    b
    a
    s
    i
    c
    s
    !
    !



```python
sentence = "It's been a long time learning Python. I am revisiting the basics!!"

# split is a string method to split the words making the string

for letter in sentence.split():
  print(letter)
```

    It's
    been
    a
    long
    time
    learning
    Python.
    I
    am
    revisiting
    the
    basics!!



```python
# For loop in dictionary 

countries_code = { "United States": 1,
                 "India": 91,
                 "Germany": 49,
                 "China": 86,
                 "Rwanda":250
            }

for country in countries_code:
  print(country)
```

    United States
    India
    Germany
    China
    Rwanda



```python
for code in countries_code.values():
  print(code)
```

    1
    91
    49
    86
    250


For can also be used to iterate over an sequence of numbers. `Range` is used to generate the sequence of numbers. 



```
for number in range: 
  do something
```




```python
for number in range(10):
  print(number)
```

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9



```python
for number in range(10, 20):
  print(number)
```

    10
    11
    12
    13
    14
    15
    16
    17
    18
    19


One last thing about `for loop` is that we can use it to make a list. This is called list comprehension.


```python
letters = []

for letter in 'MachineLearning':
  letters.append(letter)

letters
```




    ['M', 'a', 'c', 'h', 'i', 'n', 'e', 'L', 'e', 'a', 'r', 'n', 'i', 'n', 'g']



The above code can be simplified to the following code:


```python
letters = [letter for letter in 'MachineLearning']

letters
```




    ['M', 'a', 'c', 'h', 'i', 'n', 'e', 'L', 'e', 'a', 'r', 'n', 'i', 'n', 'g']


*******************
<a name='4-3'></a>

### 4.3 While loop

While loop will executes the statement(s) as long as the condition is true.

Structure of while loop



```
while condition:
  statement(s)
```




```python
a = 10
while a < 20:
    print('a is: {}'.format(a))
    a = a + 1
```

    a is: 10
    a is: 11
    a is: 12
    a is: 13
    a is: 14
    a is: 15
    a is: 16
    a is: 17
    a is: 18
    a is: 19

*******************
<a name='5'></a>

## 5. Functions

Functions are used to write codes or statements that can be used multiple times with different parameters. 

One fundamental rule in programming is "DRY" or Do not Repeat Yourself. Functions will help to not repeat yourself. 

This is how you define a function in Python:

```
def function_name(parameters):

  """
  This is Doc String
  You can use it to notes about the functions
  """
  statements 

  return results
```
* `function_name` is the name of the function. It must not be similar to any built in functions. We will see built in functions later. 
* `parameters` are the values that are passed to the function.
* `Doc String` is used to add notes about the function. It is not a must to use it but it is a `good practice`. 

* `return` specify something or value that you want to return everytime you call or run your function. 




```python
# Function to add two numbers and return a sum

def add_nums(a,b):

  """
  Function to add two numbers given as inputs
  It will return a sum of these two numbers
  """

  sum = a+b
  
  return sum
```


```python
add_nums(2,4)
```




    6




```python
add_nums(4,5)
```




    9




```python
# Displaying the doc string noted early

print(add_nums.__doc__)
```

    
      Function to add two numbers given as inputs
      It will return a sum of these two numbers
      



```python
def activity(name_1, name_2):

  print("{} and {} are playing basketball!".format(name_1, name_2))
```


```python
activity("Chris", "Francois")
```

    Chris and Francois are playing basketball!



```python
activity("Kennedy", "Kleber")
```

    Kennedy and Kleber are playing basketball!


As you can see, functions do not need to always have `return`. When you only want to display the customized message (not involving expression), `print()` will be enough. 

*******************
<a name='6'></a>

## 6. Lamdba Functions

There are times that you want to create anonymous functions. These types of functions will only need to have one expressions. 



```python
## Sum of two numbers 

def add_nums(a,b):

  sum = a+b
  
  return sum

add_nums(1,3)
```




    4



We can use lambda to make the same function in just one line of code! Let's do it!!


```python
sum_of_two_nums = lambda c,d: c + d

sum_of_two_nums(4,5)
```




    9


*******************
## <a name='7'></a>

## 7. Built in Functions

Python being a high level programming language, it has bunch of built in functions which make it easy to get quick computations done. 

An example of built in functions we used is `len()` which gives the length of the string or the list givhttps://github.com/Nyandwi/python_basics/blob/main/n as the input to it. 

Here is a full preview on all [Python Built in functions](https://docs.python.org/3/library/functions.html).

![py_functions](https://github.com/Nyandwi/python_basics/blob/main/py-built-func.jpg)


```python
# using len() to count the length of the string

message = 'Do not give up!'
len(message)
```




    15




```python
odd_numbers = [1,3,5,7]
len(odd_numbers)
```




    4




```python
# Using max() to find the maximum number in a list

odd_numbers = [1,3,5,7]
max(odd_numbers)
```




    7




```python
# Using min() to find the minimum number in a list

min(odd_numbers)
```




    1




```python
# Sorting the list with sorted()

odd_numbers = [9,7,3,5,11,13,15,1]

sorted(odd_numbers)
```




    [1, 3, 5, 7, 9, 11, 13, 15]



Let's learn two more useful built functions: they are `map` and `filter`. You can try to explore or use more built in functions on your own. 

*******************
<a name='7-1'></a>

### 7.1 Map function 

Map gives you the ability to apply a function to an iterable structures such as list. When used with a list for example, you can apply the function to every element of the list. 

Let's see how it works. 



```python
def cubic(number):
  return number ** 3
```


```python
num_list = [0,1,2,3,4]
```


```python
# Applying `map` to the num_list to just return the list where each element is cubed...(xxx3)

list(map(cubic, num_list))
```




    [0, 1, 8, 27, 64]


*******************
<a name='7-2'></a>

### 7.2 Filter function

Let's say that you have a list of numbers and you want to filter the list and remain with odd numbers. Odd number is any number which can not be divided by 2. 

You can develop a function to calculate it but you would have to always pass single value or values but not entire list. 

Using `filter`, you can return `true` for every element of list evaluated by the function. 


```python
def odd_check(number):
  
  return number % 2 != 0 

# != is not equal to operation
```


```python
num_list = [1,2,4,5,6,7,8,9,10,11]

list(filter(odd_check, num_list))
```




    [1, 5, 7, 9, 11]

*******************

<a name='8'></a>

## 8. More Useful Python Stuff

Python is an awesome programming language that has a lot of useful functions.

Let's see more useful things you may need beyond what's we just saw already.

<a name='8-1'></a>
### 8.1 List Comprehension

List comprehension makes it easy to make a new list from an existing list based on a given conditions. It's very concise and readable.

Take an example for the following cases. 


```python
# Given a list of numbers, can you make a new list of even numbers from the list nums?
# Even numbers are numbers divisible by 2, and they give the remainder of 0

nums = range(1,20)
even_nums = []


# A traditional way to do it is:

for num in nums: 
  if num % 2 == 0: 
    even_nums.append(num)

print(even_nums)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18]


A more concise and easy way to do that is to use list comprehension. 


```python
even_nums = [num for num in nums if num % 2 == 0]
print(even_nums)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18]


You can see it's pretty simple. And more readable than the former. Let's take another example.


```python
days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday']
day_T = []

# Make a list of days that start with `T`

for day in days: 
  if day[0] == 'T':
    day_T.append(day)

print(day_T)
```

    ['Tuesday', 'Thursday']


A more concise way to do it would be: 


```python
day_T = [day for day in days if day[0] == 'T']
print(day_T)
```

    ['Tuesday', 'Thursday']

*******************
<a name='8-2'></a>
### 8.2 Enumerate Function

Enumerate function convert iterable objects into enumerate object. It basically returns a tuple that also contain a counter. 

That's sounds hard, but with examples, you can see how powerful this function is... 


```python
seasons = ['Spring', 'Summer', 'Fall', 'Winter']

list(enumerate(seasons))
```




    [(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]



As you can see, each element came with index counter automatically. The counter initially start at 0, but we can change it. 


```python
list(enumerate(seasons, start=1))
```




    [(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]



Here is another example: 


```python
class_names = ['Rock', 'Paper', 'Scissor']

for index, class_name in enumerate(class_names, start=0):
  print(index,'-',class_name)
```

    0 - Rock
    1 - Paper
    2 - Scissor

*******************
<a name='8-3'></a>
### 8.3 Zip Function

Zip is an incredible function that takes two iterators and returns a pair of corresponsing elements as a tuple. 


```python
name = ['Jessy', 'Joe', 'Jeannette']
role = ['ML Engineer', 'Web Developer', 'Data Engineer']

zipped_name_role = zip(name, role)
zipped_name_role
```




    <zip at 0x107ebc9c0>



The zip object return nothing. In order to show the zipped elements, we can use a list. It's also same thing for enumerate you saw above.


```python
list(zipped_name_role)
```




    [('Jessy', 'ML Engineer'),
     ('Joe', 'Web Developer'),
     ('Jeannette', 'Data Engineer')]


*This is the end. The basics of programming are always good to have, and hopefully this intro provided you with all the necessary things to know about Python.*

## [BACK TO TOP](#0)
