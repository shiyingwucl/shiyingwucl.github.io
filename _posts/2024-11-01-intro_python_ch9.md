---
layout : posts
title : Intro to Python ch9
---

# Functions

A function is a named piece of code, in which it can receive input and return output

## 1. def

You can define a function by:

```python
def my_func():
    print("Hello World!")
```

## 2. calling a function

If you would like to use your function after defining it, just call it by typing the name of the function followed by a pair of parentheses:

```python
my_func()
```

## 3. arguments and paramenters

you can put in a parameter in the parentheses to take in arguments, the arguments can then by accessed inside the function.

## 4. None

None is a special Python placeholder value:

```python
>>> thing = None
>>> if thing:
...     print("It's something")
... else:
...     print("It's nothing")

# output: It's nothing
# It's False when evaluated as a boolean
```

but None is slightly different than False:

```python
>>> thing = None
>>> if thing is None:
...     print("It's nothing")
... else:
...     print("It's something")
...
# It's nothing
```

You need to use None to distinguish a missing value from an empty value.

## 5. positional arguments

the order in which arguments are parsed in matches the corresponding parameter:

```python
>>> def menu(wine, entree, dessert):
...     return {'wine': wine, 'entree': entree, 'dessert': dessert}
...
>>> menu('chardonnay', 'chicken', 'cake')
#output {'wine': 'chardonnay', 'entree': 'chicken', 'dessert': 'cake'}
```

## 6. keyword arguments

keyword arguments is when you fix a keyword to the corresponding parameter:

```python
>>> menu(entree='beef', dessert='bagel', wine='bordeaux')
# output: {'wine': 'bordeaux', 'entree': 'beef', 'dessert': 'bagel'}
```

you don't need to follow the order as to when you need to for positional arguments.

## 7. mix and match positional arguments and keyword arguments

```python
>>> menu('frontenac', dessert='flan', entree='fish')
{'wine': 'frontenac', 'entree': 'fish', 'dessert': 'flan'}
```

## 8. default parameter values

A default value can be set:

```python
def hi(greeting = "Goodmorning")
    return greeting
```

You can then call the function without arguments to use the default value, however - if you do parse in an argument, it will use that argument instead of the default.

*Note:*

Default parameter values are calculated when the function is defined, not when it is run. A common error with new (and sometimes not-so-new) Python programmers is to use a mutable data type such as a list or dictionary as a default parameter.

## 9. buggy()

```python
def buggy(arg,result =[]):
    result.append(arg)
    print(result)

>>> buggy('a')
# ['a']
>>> buggy('b')   # expect ['b']
# ['a', 'b']
```
as opposed to running each time with a fresh empty list, the function retains information from the previous call.

this can be fixed by writing the code like this:

```python
>>> def works(arg):
...     result = []
...     result.append(arg)
...     return result
...
>>> works('a')
# ['a']
>>> works('b')
# ['b']
```

or fixing it by specifying the default value of result to None each time we call the function:

```python
>>> def nonbuggy(arg, result=None):
...     if result is None:
...         result = []
...     result.append(arg)
...     print(result)
...
>>> nonbuggy('a')
# ['a']
>>> nonbuggy('b')
# ['b']
```

## 10. *args

You can gather positional arguments by prefixing an aterisk (*) and this will return a tuple

## 11. **kwargs

Gathers keywords argument into a dictionary by prefixing double aterisk (**)

## 12. argument order

1. Required positional arguments

2. Optional positional arguments (*args)

3. Optional keyword arguments (**kwargs)

## 13. keyword-only arguments

```python
>>> def print_data(data, *, start=0, end=100):
...     for value in (data[start:end]):
...         print(value)
```

the ```*``` indicates all the parameter after it must be passed in as keyword arguments only(name = value)

## 14. mutable and immutable arguments

values of mutable arguments can be changed from within the function,however, it's good practice to not do this. Instead, document this or return the new value.

## 15. docstrings

docstrings are strings at the beginning of the function. 

They can include rich formatting and be displayed with help(), or just help(func_name.__doc__) for the raw docstring.

## 16. Inner functions

you can define a function within a function:

```python
>>> def outer(a, b):
...     def inner(c, d):
...         return c + d
...     return inner(a, b)
```

this may be done to avoid code repetition

## 17. closure functions

an inner function can acts as a closure. It can access the local variables of the outer function it is defined in.

## 18. lambda

- single statement function

example:
```python
lambda word: word.capitalize() + '!'
```

## 19. Generator

- a Python sequence creation object
- can iterate through huge sequences without storing all of it in memory.
- generator keeps track of where it is at when iterating and returns the next value

## 20. Generator functions:

- use yield instead of return

```python
>>> def my_range(first=0, last=10, step=1):
...     number = first
...     while number < last:
...         yield number
...         number += step
# it is a normal function but it returns a generator object
```
Note
A generator can be run only once. Lists, sets, strings, and dictionaries exist in memory, but a generator creates its values on the fly and hands them out one at a time through an iterator. It doesn’t remember them, so you can’t restart or back up a generator.

## 21. Generator comprehension

- surrounded by parentheses ```()``` instead of square or curly bracketss
- similar syntax to other comprehensions

## 22. decorators

- modifying an existing function without changing its source code
- decorators are function that takes a function as input and return a new function
- you can use ```@decorator_name``` before the function instead of manually assignment
- multiple decorator can be applied to a single function, the run order of decorator depends is closest first and furtherest last   

example of decorator function:
```python
>>> def document_it(func):
...     def new_function(*args, **kwargs):
...         print('Running function:', func.__name__)
...         print('Positional arguments:', args)
...         print('Keyword arguments:', kwargs)
...         result = func(*args, **kwargs)
...         print('Result:', result)
...         return result
...     return new_function
```

## 23. Namespaces and scope

- namespace are sections where a name is unique and unrelated to same name in other namespaces
- each functions contains its own namespace
- the main part of a program have a global namespace, and its variables are global
- global variable is accessable from within a function

if you try to access AND change a global variable from within a function , an error would occur:

```python
animal = "cow"
def change_and_print_global():
    print('inside change_and_print_global:', animal)
    animal = 'wombat'
    print('after the change:', animal)

#output: UnboundLocalError: local variable 'animal' referenced before assignment
```

## 24. global() and local()

- you can explictly state which namespace varaible you want to access with global() and local()
- python defaults to using local namespace within a function
- without arguments, local() and global() returns a dictionary of contents in its respective namespaces

## 25. _ (underscore) and __ (double underscores) in names

- names begin and end with two underscores are reserved Python names, so it's good to avoid this format when naming things

examples:
```python
yourfunction.__name__ # name of the
yourfunction.__doc__ # docstring of the function 
```

## 26. recursion

- recursion happens when a functions calls itself
- to avoid infinite recursion, python automatically raises an error
- recursion is useful for dealing with uneven data


## 27. async functions

- ```async``` and ```await``` were added to python in 3.5
- details in section appendix C

## 28. Exceptions

- it's good practice to add expection handling to avoid programs abruptly shutting down
- try and except block are used to handle exceptions
- the following format can be used for except block to get the full exception object ```except exceptiontype as name```

you can define your own exceptions by using class:

```python
>>> class UppercaseException(Exception):
...     pass
...
>>> words = ['eenie', 'meenie', 'miny', 'MO']
>>> for word in words:
...     if word.isupper():
...         raise UppercaseException(word)
...
Traceback (most recent call last):
  File "<stdin>", line 3, in <module>
__main__.UppercaseException: MO
```













