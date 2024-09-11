---
layout: post
title: Intro to virtual environments (work in progress)
---

An "environment" in Python is the context in which a Python program runs that consists of an interpreter and any number of installed packages

venv vs conda

venv - python's built in virtual environment (primarily for Python packages, meaning it doesn’t manage other dependencies like system libraries)
conda - more general purpose, handles other non-Python dependencies like C libraries. used when there is a need for virtual environment with complex dependencies.
Cross-language, pre-built packages, separate from python(not tied to pip or venv, has its own package management system)

Note: The command will also install necessary packages outlined in a requirements/dependencies file, such as requirements.txt, pyproject.toml, or environment.yml, located in the project folder. It will also add a .gitignore file to the virtual environment to help prevent you from accidentally committing the virtual environment to source control
