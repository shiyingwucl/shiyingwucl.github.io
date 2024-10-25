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

### Tuple unpacking

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

### tuple()

makes tuples from other data types

### Tuple comparisons

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

## 2.lists 
enclosed in square brackets

convert to list with list(), can convert strings into single character lists too

### .split() with list

You can split a string into a list by using .spit(",") the argument is the separator

### offset and slicing

similar with string, you can use offset to extract a part of the list

### .reverse()

you can reverse a list by using yourlist.reverse()

### .append()

you can add one item at a time to the end of the list with .append()

### .insert()

you can specify which index/offset you want to insert into like:    
my_list.insert(2,"something")

### duplicate all items with *

same concept as with string

### combine two list with .extend() or +

```python
marxes = ['Groucho', 'Chico', 'Harpo', 'Zeppo']
others = ['Gummo', 'Karl']
marxes.extend(others)
#or
marxes += others
```
Note: If you try using append to add multiple values, the values would be stored all in a single index rather than as separate items.

### change an item by offset

example:
```python
marxes[2] = "something"
```
### list slicing

```python
numbers = [1, 2, 3, 4]
numbers[1:3] = [8, 9]
print(numbers)
#output [1, 8, 9, 4]
```

### del

this deletes item by specifying the index of the item
example:
del my_list[-1] 

### .remove()

when you're not sure where the item is in the list, you can parse in the value. 

if you have duplicate values, it will only delete the first value it finds.

### .pop()

.pop() returns the value of the last item in the list, and removes it

you can specify an index and it will do the above but for that specified index only


### .clear()

removes all items in a list

### .index()

parse in the value of an item and returns the index, only the first value is returned if there are duplicate values

### in

checks if a value is in a list: returns true if value is in the list, else returns false
```python
>>> marxes = ['Groucho', 'Chico', 'Harpo', 'Zeppo']
>>> 'Groucho' in marxes
True
>>> 'Bob' in marxes
False
```

### .count()

you can count how many times a specific value appears in a list

### .join()

you can turn a list a back into string using .joing():

```python
>>> marxes = ['Groucho', 'Chico', 'Harpo']
>>> ', '.join(marxes) 
'Groucho, Chico, Harpo'
```

### sort() and sorted()

sort() sorts the orginal list, while sorted() returns a copy of the sorted list without sorting the original list.

you can also parse a kwarg: .sort(reverse = True) to sort the list in reverse

### len()

gets the length of the list

### copy()

you can 
```python
>>> a = [1, 2, 3]
>>> b = a.copy() # copy() method
>>> c = list(a) #list conversion method
>>> d = a[:] #slicing method
# all of these makes a copy independent of the original list, or when you makes changes to a, it won't be reflected in the copies.
```

### deepcopy()
copy() works if the values in the list are immutable, but for mutable values, changes would be reflected in both the copy and original copy

deepcopy() handles nested lists, dictionaries and other objects.

### comparing two lists

you can use comparison operators to compare two lists

### iteration

similar with tuples, you can use for loop to iterate over the items

### .zip()

by using .zip() you can iterate multiple lists at once:
``` python
>>> days = ['Monday', 'Tuesday', 'Wednesday']
>>> fruits = ['banana', 'orange', 'peach']
>>> drinks = ['coffee', 'tea', 'beer']
>>> desserts = ['tiramisu', 'ice cream', 'pie', 'pudding']
>>> for day, fruit, drink, dessert in zip(days, fruits, drinks, desserts):
    print(day, ": drink", drink, "- eat", fruit, "- enjoy", dessert)

Monday : drink coffee - eat banana - enjoy tiramisu
Tuesday : drink tea - eat orange - enjoy ice cream
Wednesday : drink beer - eat peach - enjoy pie
```
.zip() stops when it runs out of item to iterate in the shortest list, so the "pudding" in desserts doesn't get iterated

you can also use .zip() to pair up tuples:

```python
>>> english = 'Monday', 'Tuesday', 'Wednesday'
>>> french = 'Lundi', 'Mardi', 'Mercredi'
>>> list( zip(english, french) )
[('Monday', 'Lundi'), ('Tuesday', 'Mardi'), ('Wednesday', 'Mercredi')]
```
it can be done to turn it into a dictionary too
```python
>>> dict( zip(english, french) )
{'Monday': 'Lundi', 'Tuesday': 'Mardi', 'Wednesday': 'Mercredi'}
```

### list comprehension

It is a faster way to build a list: 

```python
# syntax:
[expression for item in iterable]

#you can include a conditional
[expression for item
in iterable if condition]
```

there can be more than one set of for... clauses
```python
>>> rows = range(1,4)
>>> cols = range(1,3)
>>> cells = [(row, col) for row in rows for col in cols]
>>> for cell in cells:
...     print(cell)
...
(1, 1)
(1, 2)
(2, 1)
(2, 2)
(3, 1)
(3, 2)
```

### nested lists

you can have a value that is a list within a list

```python
>>> small_birds = ['hummingbird', 'finch']
>>> extinct_birds = ['dodo', 'passenger pigeon', 'Norwegian Blue']
>>> carol_birds = [3, 'French hens', 2, 'turtledoves']
>>> all_birds = [small_birds, extinct_birds, 'macaw', carol_birds]
```

and you can get the value of the nested list by doing:

```python
my_list[0][1]
#access the second item in the first item(the nested list) in mylist
```

## 3.Tuples vs lists

Diadvantage of tuples:
- tuples have few functions: no append() or insert()
- no tuple comprehension

Advantage of tuples:
- tuple uses less space
- tuples can be used as dictionary keys