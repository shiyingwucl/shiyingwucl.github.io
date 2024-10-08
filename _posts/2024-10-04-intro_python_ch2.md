---
layout: post
title: notes
---

Chapter 2. covers Data: Types, Values, Variables, and Names

## Python basic data types

Name|Type|Mutable?|Examples
----|--------|-------|-------|
Boolean|bool|no|True,False
Interger|int|no|4,10,78_000
Floating point| float|no|3.14,0.9,2.7e5
Complex|complex|no|3j, 5+9j
Text string|str|no|"Humpty Dumpty", "Jack Sparrow"
List|list|yes|["Winken","Bliken","Nod"]
Tuple|tuple|no|(2,4,8)
Bytes|bytes|no|b'ab\xff'
ByteArray|bytearray|yes|bytearray(...)
Set|set|yes|set([3,5,7])
Frozen set|frozenset|no|frozenset({"Elsa,"Otto"})
Dictionary|dict|yes|{"game":"bingo","dog":"dingo","drummer":"ringo"}

## Mutability
mutable = data value contained can be changed
immutable = data value is constant(cannot be changed)

Python is strongly typed, which means that the type of an object does not change, even if its value is mutable

## Literal values

There are two ways of specifying data values in Python:

Literal

Variable

## Variables

Python variable name rules:

1. can contain only these characters:

- Lowercase letters (a through z)

- Uppercase letters (A through Z)

- Digits (0 through 9)

- Underscore (_)

2. case-sensitive: thing, Thing, and THING are different names.

3. They must begin with a letter or an underscore, not a digit.

4. Names that begin with an underscore are treated specially 

5. Cannot be one of python's reserved keywords