---
layout: post
title: Introducing Python chap 1
---
[link to book](https://learning.oreilly.com/library/view/introducing-python-2nd/9781492051374/)

# Chapter 1

placeholder

## Example codes

### Example 1

```python
for countdown in 5, 4, 3, 2, 1, "hey!":
    print(countdown)
#for loop to iterate through every item
```

### Example 2

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

```
### Example 3

```python
quotes = {
    "Moe": "A wise guy, huh?",
    "Larry": "Ow!",
    "Curly": "Nyuk nyuk!",
    }
stooge = "Curly"
print(stooge, "says:", quotes[stooge])
# quotes is a dictionary which stores data in key:value pairs, dictionary are contained in curly brackets. 
```

## Python VS other languages:

1. terminal shell(cmd/bash):
- simple logic
- save commands in shell scripts
- slow and don't scale well with hundreds of lines of code

2. C and C++:
- low level language
- faster performance wise
- hard to learn and maintain code
- poor memory management can lead to program crashes and problems 

3. Java and C#:
- successor to C and C++
- improve the memory management issue
- can be verbose

C, C++, and Java are examples of static languages( They require you to specify low-level details like data types)

dynamic languages (scripting languages) do not force you to declare variable types before using them.

4. Perl
- powerful dynamic language
- has extensive library
- syntax can be akward to grasp

5. Ruby
- popular due to  Ruby on Rails, a web development framework
- used in the same areas as python

6. PHP
- popular for web development
- makes it easy to combine html and code

7. Go (Golang)
- tries to combine efficiency and user friendliness

8. Rust
- alternative to C and C++

9. Python
- major programming language
- popular in data science and machine learning
- powerful general-purpose, high-level language
- easy to read
- may be slower if program is CPU-bound compared to if it is written in C,C++, C#, Jave, Rust or GO.

## Running python

codes for python are usually stored in .py files, you don't necessary need to use the .py extension but it makes it clear that the text file is in python.

```bash
python test.py
```

## Python Easter Egg
```python
import this
```