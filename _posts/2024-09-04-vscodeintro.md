---
layout: post
title: Vscode intro
---

So for the first day, I followed the vscode python tutorial [here](https://code.visualstudio.com/docs/python/python-tutorial)

Learnt about how to use vscode (properly this time, instead of just using it as a plain text editor), and how to install the .venv environment

> ctrl+shift+p : command palette    
> very useful shortcut  

and then I continued with using the debugging tool:     
![debugging tool bar](/images/debugging%20tool%20bar.png)   
from left to right: continue/pause, stepover, step into, step out, restart and stop. 

> Useful shortcuts:    
> - breakpoint : f9   
> - f5 : continue     
> - f6 : pause    
> - f10 : step over   
> - f11 : step into   
> - shift+f11 : step out  

Below is simple code I wrote to use to practice debugging 

```python
def euros(pound):
    pound = float(pound)*1.19
    euro = round(pound,2)
    return euro

value = input("enter the value in £:")
print(f"£{value} is equal to €{euros(value)}")
```

I found the step into, and step out quite useful, bc it lets you see the process when you're calling that func/method.

There is also the side bar:

![debugging_sidebar](/images/debugging_sidebar.png)

which you can use to track variable changes and see what functions/methods is called.

And thats about it    
<img src="https://tenor.com/en-GB/view/sad-cat-sunakook-tired-exhausted-gif-10606272476729293300.gif" width="50%" height="50%" />