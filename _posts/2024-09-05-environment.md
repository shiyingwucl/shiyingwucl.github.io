---
layout: post
title: Intro to virtual environments
---

# Virtual Environment

As a follow-up to yesterday's vscode tutorial, I tapped into virtual environments in vscode studio.

An "environment" in Python is the context in which a Python program runs that consists of an interpreter and any number of installed packages

There are two different virtual environments that can be created in vscode. 

## venv vs conda

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

**Note:** The command will also install necessary packages outlined in a requirements/dependencies file, such as requirements.txt, pyproject.toml, or environment.yml, located in the project folder. It will also add a .gitignore file to the virtual environment to help prevent you from accidentally committing the virtual environment to source control

## Installing anaconda

to use .conda environment, I needed to install anacoda. which i did from their site (link here)

didn't really know what to configure for the installer, so I just went will the default setting.

after that, I wanted to create an environment within a folder, but I kept making the mistake of creating the environment in the parent folder instead. <img src= "../images/Pepe/Pepega.png" alt="pepega" width="25"/>

