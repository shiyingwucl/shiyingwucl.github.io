---
layout: post
title: Introducing Python chapter 1
---
[link to book](https://learning.oreilly.com/library/view/introducing-python-2nd/9781492051374/)

# Notes section

placeholder

## Example codes

### Example 1

```python
for countdown in 5, 4, 3, 2, 1, "hey!":
    print(countdown)
#for loop to iterate through every item
```

## Example 2

```python
spells = [
    "Riddikulus!",
    "Wingardium Leviosa!",
    "Avada Kedavra!",
    "Expecto Patronum!",
    "Nox!",
    "Lumos!",
    ]
print(spells[3])
#spell is a variable with the datatype of list, you can get an item from the list with indexing 
#python index counts from 0 

Example 3
```

```python
quotes = {
    "Moe": "A wise guy, huh?",
    "Larry": "Ow!",
    "Curly": "Nyuk nyuk!",
    }
stooge = "Curly"
print(stooge, "says:", quotes[stooge])
#
```