---
layout: post
title: Intro to python ch7
---

# Keypoints

## 1.Tuples

syntax:

```python

example1 = "apple", #you can make a tuple without parentheses

example2 = ("apple",) #this still returns a tuple too

example3 = ("apple") # however, without the comma, this will return only a string

my_tuple = ("apple","banana","orange")
```

## 2. Tuple unpacking

you can assign multiple variables at once with tuple unpacking:

```python
example = ("apple","banana","orange")
a,b,c = example

"""output"""
# a = "apple"
# b = "banana"
# c = "orange"
```

You can use tuples to exchange values in one statement without using a temporary variable:

```python
password = 'swordfish'
icecream = 'tuttifrutti'
password, icecream = icecream, password
```

## 3. tuple()

makes tuples from other data types

## 4. Tuple comparisons

```python
a = (7, 2)
b = (7, 2, 9)
a == b
# False
a <= b
# True
a < b
# True
```

#
