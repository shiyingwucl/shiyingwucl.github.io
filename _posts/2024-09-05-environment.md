---
layout: post
title: Intro to virtual environments
---

# Virtual Environment

An **environment** in Python is: 
>the context in which a Python program runs that consists of an interpreter and any number of installed packages 


## venv vs conda

There are two different virtual environments that can be created in vscode. 

> **.venv :**   
    - python's built in virtual environment     
    - primarily for Python packages
    - doesn’t manage other dependencies like system libraries   

> **conda :**    
    - more general purpose  
    - handles other non-Python dependencies like C libraries    
    - used when there is a need for virtual environment with complex dependencies    
    - cross-language
    - pre-built packages, separate from python(not tied to pip or venv, has its own package management system)

**Note:** 
- The command will also install necessary packages outlined in a requirements/dependencies file, such as requirements.txt, pyproject.toml, or environment.yml, located in the project folder. 

- It will also add a .gitignore file to the virtual environment to help prevent you from accidentally committing the virtual environment to source control

## Anaconda

To use .conda environment, I needed to install anacoda. which is avaliable [here](https://www.anaconda.com/download?utm_source=anacondadoc&utm_medium=documentation&utm_campaign=download&utm_content=topnavalldocs)

didn't really know what to configure for the installer, so I just went with the default setting.

after that, I wanted to create an environment within a folder, but I kept making the mistake of creating the environment in the parent folder instead( remember to open folder in the correct location)   
![pepega](/images/emotes/PeepoWhy.png)

conda is confusing to setup so I'll just leave it here for now, probably will come back to it later at some point...

## Stupid things that you shouldn't do (which I did):
```bash
conda init
# adds conda to path
```
