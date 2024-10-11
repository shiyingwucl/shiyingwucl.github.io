---
layout: post
title: Intro to python ch5
---

# Keypoints
## 1. String

- strings are a python sequence of characters
- a character is the smallest unit in writing 
- whitespace or directives like line-feeds counts as a character too
- strings are immutable
- enclosed in quotes

## 2. Special types of strings

you can indicate special types of string with a letter before the first quote

```python
f"Hello world"
```
f : used for formatting  
fr : starts a raw f-string  
u : starts a unicode string  
b : starts a value of bytes

## 3. Single and double quotes

String can be enclosed in single and double quotes, this is because you could have:

```python
"She said:'No'"
```

You can also have three single or three double quotes to create a docstring/ multi-line string

Note:(I thought docstring is another way of commenting but it seems like python interprets the docstring and does not ignore it)

## 4. Print() vs automatic echo from interpreter

print() strips the quotes from string and keeps the line break for multi-line string

interpreter echos the string with quotes and escape characters ```\n```

## 5. Empty string

You could create a string with no characters 

## 6. str()

str() takes another datatype value and makes a string from it, print() does this internally when you parse in objects that are not strings or in string formatting.

## 7. Escape character \ (backslash)

```\n```: begins a new line
 ```\t```: (tab) used to align text

you might also use \' or \" to specify a literal quote, same could be done with backslash by using \\\


## 8. Raw string
In raw string, the escape character is negated:
```python
info = r'Type a \n to get a new line in a normal string'
>>> info
# output: 'Type a \\n to get a new line in a normal string'
>>> print(info)
# output: Type a \n to get a new line in a normal string
```
However, new lines that are not started with \n in rawstring does not change

## 9. String concatenation

- You can combine literal strings/ string variables by using the operator "+"
- You can also put one literal string after another which achieves the same result, this however, does not apply to string variables.
- python doesn't automatically add spaces when concatenating string, but it does add space between each argument in a print() statement 

## 10. Duplication

- * operator can be used to duplicate string:

```python
start = 'Na ' * 4 + '\n'
middle = 'Hey ' * 3 + '\n'
end = 'Goodbye.'
print(start + start + middle + end)
# outputs:     
# Na Na Na Na 
# Na Na Na Na 
# Hey Hey Hey 
# Goodbye.
```

## String slicing

you can input an offset/index inside a square bracket []:

```python


```



