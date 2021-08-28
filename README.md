# Python-Fundamental


1. Python Download Link : https://www.python.org/downloads/
2. Microsoft Visual Studio Code : https://code.visualstudio.com/download
3. Imp Extensions for Visual Studio Code : Python, Pylance,Material Icon Theme, Live Server, DJango
4. After installation open cmd (or Window power shell if you are using Windows) & type 'python', to see version only type 'python --version'
5. Python is a high level, Poratable, Open Source & case sensitive language.


# Topics
1. [What is Module](#Module), [dir()](#dir-Function)
2. [What is pip?](#What-is-pip),[The REPL](#The-REPL),[Comments](#Comments)
3. [Variables In Python](#Variables-in-Python)
4. [Type() & Type Conversion](#Type-Function-and-Type-Conversion), [Implicit Type Conversion](#1-Implicit-Type-Conversion),[Explicit Type Conversion](#2-Explicit-Type-Conversion)


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

## Type Function and Type Conversion


### Type Function 
type() method returns class type of the argument(object) passed as parameter
```
List1 = [1,2,3,4,5,6,7,8,9,10]
Tuple = (1,2,3,4,5,6,7,8,9,10)
Dict = {1:'John', 2:'Wick',3:'Barry', 4:'Allen'}
print(f"{type(List1)}\n{type(tuple)}\n{type(Dict)}")
```

Python defines type conversion functions to directly convert one data type to another
There are two types of Type Conversion in Python:

### 1 Implicit Type Conversion
In Implicit type conversion of data types in Python, the Python interpreter automatically converts one data type to another without any user involvement.
```
x = 10 
print("x is of type:",type(x))
y = 10.6
print("y is of type:",type(y))
x = x + y
print(x)
print("x is of type:",type(x))
```
In above example, the type of ‘x’ got automatically changed to the “float” type from the “integer” type. this is a simple case of Implicit type conversion in python.

### 2 Explicit Type Conversion
In Explicit Type Conversion in Python, the data type is manually changed by the user as per their requirement.

   1. int(a, base): This function converts any data type to integer. 
    ‘Base’ specifies the base in which string is if the data type is a string.
   2. float(): This function is used to convert any data type to a floating-point number 
   3. ord() : This function is used to convert a character to integer.
   4. hex() : This function is to convert integer to hexadecimal string.
   5. oct() : This function is to convert integer to octal string.
   6. tuple() : This function is used to convert to a tuple.
   7. set() : This function returns the type after converting to set.
   8. list() : This function is used to convert any data type to a list type.
   9. dict() : This function is used to convert a tuple of order (key,value) into a dictionary.
   10. str() : Used to convert integer into a string.
   11. complex(real,imag) : : This function converts real numbers to complex(real,imag) number.
   12. chr(number) : : This function converts number to its corresponding ASCII character.

```
s = "10010"

#1
# printing string converting to int base 2
print (f"After converting to integer base 2 : {int(s,8)}")

#2
# printing string converting to float
print (f"After converting to float : {float(s)}")

s = '4'

#3
# printing character converting to integer
print (f"After converting character to integer : {ord(s)}")

#4
# printing integer converting to hexadecimal string
print (f"After converting 56 to hexadecimal string : {hex(56)}")

#5
# printing integer converting to octal string
print (f"After converting 56 to octal string : {oct(56)}")


s = 'Gurudutt Goswami'
#6
# printing string converting to tuple
print (f"After converting string to tuple : {tuple(s)}")

#7
# printing string converting to set
print (f"After converting string to set : {set(s)}")

#8
# printing string converting to list
print (f"After converting string to list : {list(s)}")

a = 1
b = 2
#9
# printing integer converting to complex number
print (f"After converting integer to complex number : {complex(1,2)}")

#10
# printing integer converting to string
print (f"After converting integer to string : {str(a)}")

#11
# initializing tuple
tup = (('a', 1) ,('f', 2), ('g', 3))
# printing tuple converting to expression dictionary
print (f"After converting tuple to dictionary : {dict(tup)}")

#12
# Convert ASCII value to characters
a = chr(76)
b = chr(77)
 
print(a)
print(b)
```
