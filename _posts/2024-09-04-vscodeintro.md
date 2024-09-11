---
layout: post
title: vscode intro
---

I followed the vscode python tutorial [here](https://code.visualstudio.com/docs/python/python-tutorial)

I learnt about how to use vscode(properly), learnt how to install the .venv environment and also tried a simple debugging of a quick code in python. 

> ctrl+shift+p : command palette
> very useful shortcut  

I continued to learn about debugging:
![debugging tool bar](/images/debugging%20tool%20bar.png)
from left to right: continue/pause, stepover, step into, step out, restart and stop. 

> shortcuts:
> breakpoint : f9
> f5 : continue
> f6 : pause
> f10 : step over
> f11 : step into
> shift+f11 : step out

```python
def euros(pound):
    pound = float(pound)*1.19
    euro = round(pound,2) # no trailing zeros with round func
    return euro

value = input("enter the value in £:")
print(f"£{value} is equal to €{euros(value)}")
```

I found the step into(a function/method), and step out (a function/method) quite useful, bc it lets you see the process when you're calling that func/method.