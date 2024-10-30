---
layout: post
title: Intro to Python ch8
---

# Keypoints:

## 1. Dictionary is:

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

## 3.