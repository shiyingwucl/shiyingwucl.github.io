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

## 4. print() vs automatic echo from interpreter
## 4. print() vs automatic echo from interpreter

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

## 11. String slicing

- you can input an offset/index inside a square bracket [] to get a character from a string

- putting a minus like: [-1] counts from the last character

- you will get an IndexError if the index is longer than the length of string

### replace()
``` python
name = 'Henny'
name.replace('H', 'P')
#output: 'Penny'

# slicing could yield same result
'P' + name[1:]
#output: 'Penny'
```

you could also add an additional argument in name.replace("H","P") to specify how many times you want to replace the item. 

you could also add an additional argument in name.replace("H","P") to specify how many times you want to replace the item. 

### create a substring with slice
format: "your_string"[start:end:step]

- start: the index you want to begin from (inclusive)
- end: the index which you want to end at (exclusive)
- step: the number of characters you skip each step

putting a minus sign before index makes the count start from the end

## 12. len()

counts the number of character in a string, could be used with other sequence types too

## 13. split()

returns a list of separated items from a string
returns a list of separated items from a string
```python
tasks = 'get gloves,get mask,give cat vitamins,call ambulance'
tasks.split(',') #if delimiter is not specified, python uses any sequence of white space characters
```

## 14.join()

join() is like opposite of split, returns a list of strings back into a single string.

```python
crypto_list = ['Yeti', 'Bigfoot', 'Loch Ness Monster']
crypto_string = ', '.join(crypto_list)
print('Found and signing book deals:', crypto_string)
# output: Found and signing book deals: Yeti, Bigfoot, Loch Ness Monster
```

## 15. strip()

you can use this function to remove certain character, especially spaces:

- lstrip(): remove from the left of string
- rstrip(): remove from right of string

## 16. Search

these checks returns True/False:

.startswith()
.endswith()
.isalnum() :is all characters either numbers or letter

.count() : counts how many times the substring occurs in the string

## 17. find() vs index()

.find()
.index()

if substring isn't found, .find() returns -1 whereas .index() raises an exception

## 18. Case

.capitalize() :capitalize the string
.title() :capitalize all the words
.upper() :uppercase all the words
.lower() :lowercase all the words
.swapcase() :swaps uppercase and lowercase

## 19. Alignment

you can input arguments for  how many spaces to:
.center() 
.ljust()
.rjust()

## 20. formatting

interpolating data values:
old style, new style, f-string

### old style: %

Format and examples:
```python
#format_string % data
"%s" % 34
```

syntax|name
------|----
%s| string
%d| decimal integer
%x| hex integer
%o| octal integer
%f| decimal float
%e| exponential float
%g| decimal or exponential float
%%| a literal %

%s for any data type and Python will format it as a string with no spaces

String and integer interpolation:
```python
"Our cat %s weighs %s pounds" % (cat, weight)
```
### new style: {} and format

```python
#format_string.format(data)
thing = "something"
"{}".format(thing)

#output: something

thing = 'woodchuck'
place = 'lake'
'The {} is in the {}.'.format(thing, place)
#output: The woodchuck is in the lake.
```

you can also specify the arguments' position:

```python
'The {1} is in the {0}.'.format(place, thing)

#output: The woodchuck is in the lake
```

### f strings

Format:
```python
f"The {thing} is in the {positon}
```

## Exercise 