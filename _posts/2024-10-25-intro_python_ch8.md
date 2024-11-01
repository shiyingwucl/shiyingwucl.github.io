---
layout: post
title: Intro to Python ch8
---

# Keypoints:

# 1. Dictionary is:

```{key:value}```

key can be any immutable type

dictinoary itself is mutable

name in other language for dictionaries: associative array, hashes, hashmaps

## 2. dict()

```python
>>> acme_customer = dict(first="Wile", middle="E", last="Coyote")
>>> acme_customer
{'first': 'Wile', 'middle': 'E', 'last': 'Coyote'}
```
this is limited because keys will need to be valid variable names(no spaces, no reserved words etc.)

dict can be also used to convert two value sequences into dictionary. example to can be converted: ```[["a",1]["b",2]["c",3]["d",4]]```

## 3. Add/ changing items by its keys

```python
my_dict["food"] = "hamburger"
```

If a key called food doesn't exist, this will add a new key:value pair, but if it does exist, it will update the key value pair

## 4. Keys must be unique

If a key exist more than once in the dictionary, only the latest value would be reflected

## 5. Getting value by specifying key

```python
my_dict["food"]
# would return an error if key is not present in the dictionary

my_dict.get("food","Not in the dictionary")
# returns None or the specified optional value if key doesn't exist
```

## 6. keys()

.keys() gets all keys in the dictionary

Python 2: keys() returns a list

Python 3: keys() returns dict_keys() - which is an iterable view object, so you'd need to use list() to convert this if you need a list instead

## 7. values()

similarly to keys() this returns all values in a dictionary instead of keys.

## 8. items()

this returns both key value pairs in a tuple:
```("food","hamburger")```

## 9. len()

returns how many key:value pair are in the dictionary

## 10. combining dictionaries with **

```python
>>> first = {'a': 'agony', 'b': 'bliss'}
>>> second = {'b': 'bagels', 'c': 'candy'}
>>> {**first, **second}
{'a': 'agony', 'b': 'bagels', 'c': 'candy'}
```
you can parsed in more than two dictionaries to combine
**Using this method creates shallow copies!**

## 11. update()

```dict_1.update(dict_2)```

this adds the key:value pairs of dict_2 to dict_1, and if there is any duplicate keys, its will update it to represent dict_2's version instead.

## 12. del

removes the key:value pair from a dictionary

## 13. pop()

essentially a combination for get() followed by del

## 14. clear()

empties the dictionary

## 15. checking if key exists in a dictionary

use the membership operator ```in``` 

## 16. copy()

you can make a shallow copy of a dictionary with copy(), this works if the dictionary values are immutable. 

If the values are mutable, you would need to use deepcopy() to ensure that everything is standalone from the original.

## 17. comparing dictionaries

using comparison operators == and !=, you can compare one dictionary to another

however, other operators like <=, >= will not works

dictionaries are compared one by one by key:value, and order doesn't matter

## 18. dictionary iteration

iterating over a dictionary return the key:
```python
>>> accusation = {'room': 'ballroom', 'weapon': 'lead pipe',
...               'person': 'Col. Mustard'}
>>> for card in accusation:  #  or, for card in accusation.keys():
...     print(card)
...
room
weapon
person
```

for value, you need to iterate using .values()

## 19. dictionary comprehension

format:
{key_expression : value_expression for expression in iterable}

example:

```python
>>> word = 'letters'
>>> letter_counts = {letter: word.count(letter) for letter in set(word)}
>>> letter_counts
{'t': 2, 'l': 1, 'e': 2, 'r': 1, 's': 1}
```

# 20. Sets

each item in a set is unique, similarly to dictionary keys

sets are unordered

## 21. set()

python prints out an empty set as set(), because {} is used by dictionary

you can convert other sequences into a set to remove duplicate items

## 22. add()

## 23 remove()

## 24. & and intersection()
the ampersand(&) operator allows you to find the intersection(items that appears in both sets)

example:

```python
>>> for name, contents in drinks.items():
...     if contents & {'vermouth', 'orange juice'}:
...         print(name)
...
screwdriver
martini
manhattan
```

you can also use intersection() to achieve the same effect

## 25. | and union()

you can get the union(members of either set) with "|" (vertical bar) or union()

example:
```python
>>> a | b
{1, 2, 3}
>>> a.union(b)
{1, 2, 3}
```
## 26. - and difference()

you can obtain the difference of two sets (members of the first set but not the second) with - (minus) or difference()

```python
>>> a - b
{1}
>>> a.difference(b)
{1}
```

## 27. ^ and symmetric_difference()

using ^ (carrot) or symmetric_difference() returns the exclusive (items only in one set and not the other)

## 28. <= and issubset()

you can check if a set is a subset(all items in the first set also belong in the second) of another set

(interestingly, all sets is a subset of itself, but to be a proper subset, the second needs to have all items in the first and this can be check with "<")

## 29. >= and issuperset()

A superset is where all items of the second set also belongs in the first set - opposite of subset.

A proper superset can be checked with ">"

## 30. set comprehension

format: { expression for expression in iterable }

format with condition: { expression for expression in iterable if condition }

## 31. frozenset()

You could create an immutable set with any iterable

```python
>>> frozenset([3, 2, 1])
frozenset({1, 2, 3})
>>> frozenset(set([2, 1, 3]))
frozenset({1, 2, 3})
>>> frozenset({3, 1, 2})
frozenset({1, 2, 3})
>>> frozenset( (2, 3, 1) )
frozenset({1, 2, 3})
```

