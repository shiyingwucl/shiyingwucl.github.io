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
