# Python-Fundamental


1. Python Download Link : https://www.python.org/downloads/
2. Microsoft Visual Studio Code : https://code.visualstudio.com/download
3. Imp Extensions for Visual Studio Code : Python, Pylance,Material Icon Theme, Live Server, DJango
4. After installation open cmd (or Window power shell if you are using Windows) & type 'python', to see version only type 'python --version'
5. Python is a high level, Poratable, Open Source & case sensitive language.


# Topics
1. [Module](#Module), [dir()](#dir-Function)
2. [What is pip?](#What-is-pip),[The REPL](#The-REPL),[Comments](#Comments)
3. [Variables In Python]


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

## Variables in Python
We do not need to declare variables before using them or declare their type. A variable is created the moment we first assign a value to it. A variable is a name given to a memory location. It is the basic unit of storage in a program. The value stored in a variable can be changed during program execution.A variable is only a name given to a memory location, all the operations done on the variable effects that memory location.

### Rules for creating variables in Python:
1. A variable name must start with a letter or the underscore character.
2. A variable name cannot start with a number.
3. A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ ).
4. Variable names are case-sensitive (name, Name and NAME are three different variables).
5. The reserved words(keywords) cannot be used naming the variable.

### Data Types
```
age = 45    #Integers
salary = 1456.8 # A floating point
name = "John"   # A string
AmIProgrammer = True  #Boolean value
WantToSaySomething = None

print(f"Age : {age}\nSalary :{salary}\nName : {name}\nAmIProgrammer : {AmIProgrammer} \nWantToSaySomething : {WantToSaySomething}")
```

### Re-declare the Variable:
We can re-declare the python variable once we have declared the variable already.
```
Number = 100
print("Before declare: ", Number)
Number = 120.3    # re-declare the var
print("After re-declare:", Number)
```
### Assigning a single value to multiple variables
```
a = b = c = 10
print(f"a : {a}\nb : {b}\nc : {c} ")
```
### Assigning different values to multiple variables
```
a, b, c = 1, 20.2, "Something is looking simple"
print(f"a : {a}\nb : {b}\nc : {c} ")
```
### Can we use the same name for different types? : Yes 
```
a = 10
a = "Okay I got it"
print(a)
```
