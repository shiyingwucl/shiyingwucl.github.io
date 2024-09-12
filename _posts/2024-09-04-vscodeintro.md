---
layout: post
title: Intro to VSCode
---

# Intro to VSCode
So to start off, I followed the VSCode python tutorial <a href="https://code.visualstudio.com/docs/python/python-tutorial" target="_blank">here</a>

It touches on topics like how to use VSCode (properly), setting up virtual environments, using the debugging tool and more.

### **Useful general shortcuts**  
> ctrl+shift+p : command palette    
> ctrl+k then ctrl+o : open folder  
> ctrl+o : open file    
> ctrl+shift+n : opens a new window     
> ctrl+shift+left/right_arrow_key : select the word

## Setting up virtual environment

> open command palette    
> python create new environment     
> select .venv

## Debugging
using the debugging tool:     
![debugging tool bar](/images/debugging%20tool%20bar.png)   
(From left to right:     
continue/pause, stepover, step into, step out, restart and stop) 

### **Useful debugging shortcuts:**    
> F9 : breakpoint   
> F5 : continue     
> F6 : pause    
> F10 : step over   
> F11 : step into   
> Shift+F11 : step out  

### The side panel:

![sidepanel](/images/debugging_sidebar.png)

> **Variable:** shows the variables in the current debugging scope, including value and types  
> **Watch:** tracks the value of specific expressions or variables you're interested in throughout the debugging session        
> **Call stack:** shows the hierachy of function calls, indicating the path the program took to reach the current point          
> **Loaded scripts:** lists all the scripts that have been loaded into the current debugging session, useful for navigating to different parts of the code or library being used
which you can use to track variable changes and see what functions/methods is called.   

### Writing some code to debug with
Below is python code I wrote to use to practice debugging 

```python
def euros(pound):
    pound = float(pound)*1.19
    euro = round(pound,2)
    return euro

value = input("enter the value in £:")
print(f"£{value} is equal to €{euros(value)}")

#code that converts pound to euros
```

Personally I really like the step into, and step out functionality, because it lets you see the process that happens internally when you're calling that func/method.   

(but why no step back... <img src= "https://shiyingwucl.github.io/blob/posts/images/PeepoWhy.png" alt="peepowhy" width="25" >)

And thats about it for today    
<img src="https://tenor.com/en-GB/view/sad-cat-sunakook-tired-exhausted-gif-10606272476729293300.gif" width="50%" height="50%" />