# Python-Fundamental


1. Python Download Link : https://www.python.org/downloads/
2. Microsoft Visual Studio Code : https://code.visualstudio.com/download
3. Imp Extensions for Visual Studio Code : Python, Pylance,Material Icon Theme, Live Server, DJango
4. After installation open cmd (or Window power shell if you are using Windows) & type 'python', to see version only type 'python --version'
5. Python is a high level, Poratable, Open Source & case sensitive language.


# Topics
1. [Module](#Module)
2. [dir()](#dir-Function)
3. [What is pip?](#What-is-pip)
4. [The REPL](#The-REPL)
5. [Comments](#Comments)


## Module
A module is a file containing Python definitions and statements. A module can define functions, classes, and variables. A module can also include executable code.  
A module can be categorizes into two type:
  1. Built-in modules: os,abc etc.
  2. Exteranl Modules: tensorflow, flask etc.

Note : We can use any Python source file as a module by executing an import statement in some other Python source file. 
```import calc```
#### Python’s from statement lets you import specific attributes from a module. The from .. import .. has the following syntax:
```diff
from math import sqrt, factorial
```
The * symbol used with the from import the statement is used to import all the names from a module to a current namespace.
```
from module_name import *
```
### dir Function
The dir() built-in function returns a sorted list of strings containing the names defined by a module. The list contains the names of all the modules, variables, and functions that are defined in a module.
```
from random import *
print(dir(random))
```

## What-is-pip
Rep Link : https://github.com/Gurudutt-Goswami/What-is-pip

### The REPL
REPL stands for Read, Evaluate, Print, Loop. The REPL is how you interact with the Python Interpreter. Its is also reffered as also termed an interactive toplevel or language shell. Unlike running a file containing Python code, in the REPL you can type commands and instantly see the output printed out.

### Comments 
1. Single Line ```#Code after hashtags are single line comments```
2. Multiline
```
'''
This is a 
multi
line 
comment
'''
```
