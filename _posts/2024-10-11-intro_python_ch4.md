---
layout: post
title: Intro to python ch4

---

# Keypoints

## 1. Indentation
Guido van Rossum designed python with the idea that indentation would act as structure to a program.

four spaces are the norm for each sub section

## 2. Comment/docstring
using # to comment or triple quotes to docstring

```python
#this is a comment
"""this is a docstring"""
```
## 3. Continue lines with \ (backslash)
the recommended maximum line length in a program is 80 chars, it is not required but makes the code more readable

if you can't fit everything under 80 chars, you can use backslash to continue over the line

contents in parentheses, square/curly brackets also continues as if they are on a single line, even if they are on a different line

## 4. If, elif and else

if statement checks if a condition is boolean value of True, or can be interpreted as True

```python
red = True
if red:
    print("The colour is red")
else:
    print("I'm colour blind")

```

elif statement are only checked when if statement are not met. When if statement conditions are met before elif statements, it will skip over elif  

## 5. Comparison operators

|Name | Symbol|
|:----:|:------:|
|equality| == |
|inequality| !=|
|less than|<|
|less than or equal|<=|
|greater than|>|
|greater than or equal|>=|

These operators return boolean values

## 6. Logical(boolean) operators

and| if both statements are True
or| if either one statements are True
not| returns True if statement are False and vice versa

when logical operators are used in conjunction with comparison operators, logical operators takes lower prescendence. 

## 7. True and False elements

things python considers false:

|datatype|value|
|:------:|:------:|
|boolean |False|
|null|None|
|zero integer|0|
|zero float|0.0|
|empty string|""|
|empty list|[]|
|empty tuple|()|
|empty dict|{}|
|empty set|set()|

anything else are True

## 8. Multiple comparisons

using Python's membership operator "in", you can chec

## 9. Walrus operator

assigns the expression and combine that expression to use as a part of a larger expression 

```python
tweet_limit = 280
tweet_string = "Blah" * 50
if diff := tweet_limit - len(tweet_string) >= 0:
    print("A fitting tweet")
```

## 10. Exercise Answers

4.1:
```python
secret = 10
guess = 6
if guess < secret:
    print("too low")
elif guess > secret:
    print("too high")
elif: guess == secret:
    print("just right")
```

4.2:
```python
small = True
green = False
if small == True:
    if green == False:
        print("cherry")
    if green == True:
        print("pea")
else:
    if green == False:
        print("pumpkin")
    if green == True:
        print("watermelon")
```