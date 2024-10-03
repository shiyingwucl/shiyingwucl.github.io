---
layout: post
title: python project structure best practice
---

## Root directory

main folder contain your entire project

## Application directory

holds main source code of your application

components:
__init__.py
app.py
config.py

optional:
views.py

## static assets

## tests directory

## requirement.txt

created by running: pip freeze > requirements.txt
others can then use: pip install -r requirements.txt in their terminal to install all the dependencies

## readme.md

## setup.py

packaging your project so that it can be distributed with PyPI(with pip install)

## Best Practices for Organizing Code

Modular Code:  
Break down your code into smaller modules and packages, each handling a specific aspect of the application.

Separation of Concerns:  
Keep different parts of your application (like business logic, data models, configuration, and static files) in separate files or directories. This makes the codebase easier to maintain.

DRY Principle:  
Don't Repeat Yourself. Use utility functions and modularize your code to avoid duplicating logic.

Testing:  
Write test cases for your modules. Test-driven development (TDD) is encouraged, especially in large applications
