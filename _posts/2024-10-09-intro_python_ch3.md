---
layout: post
title: Intro to python ch3

---

# Chapter 3. Numbers

## Booleans

True or False

Nonzero numbers are True
are False

## Integers

- Whole numbers

- Literal Integers (can't have an initial 0 followed by digits 1-9, e.g. 02348), but you can start integer with 0b, 0o, or 0x to indicate the bases

- you can use underscore as a digit separator

### Integer operations
operator|description|example|result
----|----|-----|----|
+|addition| 5+2 |7
-|subtraction|10-7|3
*|mutiplication|20*5|100
/|floating-point division|10/4|2.5
//|Integer(truncating) division|7//3|
%|Modulus (remainder)|
\**|Exponentiation|3**4|81

divmod(divend,divisor) #returns a tuple containing quotient and remainder

## Bases
Integers are assumed base10
you can express literal integers in three bases besides decimal with:
- 0b or oB (base2/binary)
- 0o or 0O (base8/octal)
- 0x or 0X (base16/hex)

you can convert an integer to string with:

```python
value = 65
bin(value)
#outputs in base 2 form
oct(value)
#output in octal
hex(value)
#output in hexadecimal
```

You can also use char() or ord() to find the string/integer equivalent of something
```python
chr(65)
#returns "A",converts an integer to its single character string equivalent
ord("A")
#retuns "65",converts string to integer equivalent
```

bases are useful in bit-level operations
```python
int()
#this converts the datatype of the parsed in value to integer
int("10",2) # specifies base 2 
#you can pass in arguments which indicates what base it is in

"""example"""
int("10",8) #octal
int("10",16) # hexadecimal
```


In Python 2, int are limited to 32 or 64 bits.
In Python 3, int could be any size

## Floats

floats : short for **floating-point number**

floats can include decimal integer exponent after letter e
```python
5e0
#5.0
5e1
#50.0
5.0e1
#50.0

```

when mixing ints and floats, python automatically changes the int to float values