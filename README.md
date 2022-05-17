# Python-Fundamental


1. Python Download Link : https://www.python.org/downloads/
2. Microsoft Visual Studio Code : https://code.visualstudio.com/download
3. Imp Extensions for Visual Studio Code : Python, Pylance,Material Icon Theme, Live Server, DJango (VSCode is IDE cum source code Editor)
4. After installation open cmd (or Window power shell if you are using Windows) & type 'python', to see version only type 'python --version'
5. Python is a ```high level, Portable(Works on Linux/Windows/Mac) , Open Source & case sensitive language.```
6. To increase the font size using ctrl + mouse wheel, Go to VSCode Settings & type Zoom where you will get 'Mouse Wheel Zoom' Option, just check that.


# Topics
1. [What is Module](#Module) , [dir()](#dir-Function)
2. [What is pip?](#What-is-pip) , [The REPL](#The-REPL),[Comments](#Comments)
3. [Variables In Python](#Variables-in-Python) , [Operators](#Operators)
4. [Type() & Type Conversion](#Type-Function-and-Type-Conversion), [Implicit Type Conversion](#1-Implicit-Type-Conversion) , [Explicit Type Conversion](#2-Explicit-Type-Conversion)
5. [Input()](#Input-Function), [String](#Strings) , [Indexing](#Indexing) , [Slicing](#String-Slicing), [Escape Sequence](#Escape-Sequence) , [String Functions](#String-Functions)
6. [Lists](#Lists) , [Creating a list](#Creating-a-list) , [Size of List](#Size-of-List) , [Adding Elements to a List](#Adding-Elements-to-a-List), [List Functions](#List-Functions)
7. [Tuples](#Tuples), [Creating a Tuple](#Creating-a-Tuple), [Deleting a Tuple](#Deleting-a-Tuple), [Converting List into Tuple](#Converting-List-into-Tuple), [Tuples Functions](Tuple-Functions)

## Module
A module is a file containing Python definitions and statements. A module can define functions, classes, and variables. A module can also include executable code.  
A module can be categorizes into two type:
  1. Built-in modules: os,abc etc. (https://docs.python.org/3/py-modindex.html)
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
print(dir(random)) #Here instead of 'random' we can put any module name & its corresponding details will up as a list 
```

## What-is-pip
Rep Link : https://github.com/Gurudutt-Goswami/What-is-pip

### The REPL
REPL stands for Read, Evaluate, Print, Loop. The REPL is how you interact with the Python Interpreter. Its is also reffered as an interactive toplevel or language shell. Unlike running a file containing Python code, in the REPL you can type commands and instantly see the output printed out.

### Comments
Tip: To comment any line(/s) in VSCode just press 'Ctrl+/' (Forward Slash)
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

### Operators
1. Arithmatic Operators: +,-,/,*
2. Assignment Operators: =,+=,-=, etc
3. Comparison Operators: ==,>,<,>=,<=,!= (Returns Boolean)
4. Logical Operators: and, or , Not


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

## Input-Function
This function allows the user to take input from the keyboard as a string.
```
string = input()
name = input("Enter your name: ")
num = int(input("Enter a number: "))
flo =float(input("Enter a number "))
li =list(input("Enter a list "))
tup =tuple(input("Enter a tuple "))
set1 = set(input("Enter a set "))

print(f"{string}\n{name}\n{num}\n{flo}\n{li}\n{tup}\n{set1}")
```

## Strings
1. String is a ```sequence of characters enclosed in quotes```. (Quotes can be single, double or triple).
2. In other words, Strings are arrays of bytes representing Unicode characters.
3. Square brackets can be used to access elements of the string.
4. ```Strings are immutable (not changeable)```, hence elements of a String cannot be changed once it has been assigned. Only new strings can be reassigned to the same name. 

### Indexing
1. In Python, individual characters of a String can be accessed by using the method of Indexing. 
2. Indexing also allows negative address references to access characters from the back of the String, e.g. -1 refers to the last character, -2 refers to the second last character and so on. 
3. While accessing an index out of the range will cause an ```IndexError``` . Only Integers are allowed to be passed as an index, float or other types will cause a ```TypeError```. 
4. The index of a string ```from 0 to (Length-1)``` in python.

![strings](https://user-images.githubusercontent.com/86184439/131231705-b570ccde-5d1c-4522-9ad3-2e38bc5f27b4.jpg)
```
String1 = "Gurudutt Goswami"
print(f"\nFirst character of String is: {String1[0]}\nLast character of String is: {String1[-1]}")
```

### String Slicing
1. To access a range of characters in the String, method of slicing is used. Slicing in a String is done by using a Slicing operator (colon). 
2. In order to slice we use use : ```S1 = name_of_string [start_index : end_index : step-size]```
```
String1 = "Gurudutt Goswami"
print(String1[3:12])
print(String1[3:-2])
print(String1[:16]) #Equivalent to string1[0:16]
print(String1[0:])  #Equivalent to string1[0:16]
print(String1[1:6:2])   #Third parameter is Step size
```

### Escape Sequence
Escape sequences start with a backslash and can be interpreted differently.  
To ignore the escape sequences in a String, r or R is used, this implies that the string is a raw string and escape sequences inside it are to be ignored.

1. \'	Single Quote	
2. \\	Backslash	
3. \n	New Line	
4. \r	Carriage Return	
5. \t	Tab	
6. \b	Backspace	
7. \f	Form Feed	
8. \ooo	Octal value	
9. \xhh	Hex value
 
To check their implementation refer : https://www.w3schools.com/python/gloss_python_escape_characters.asp
```
String1 = "This is \x47\x65\x65\x6b\x73 in \x48\x45\x58"
print(f"\nPrinting in HEX with the use of Escape Sequences: {String1}")

# Using raw String to ignore Escape Sequences
String1 = r"This is \x47\x65\x65\x6b\x73 in \x48\x45\x58"
print(f"Printing Raw String in HEX Format: {String1}")
```

### String Functions
Some Examples : len(), string.endswith('dutt'), string.count("a"), string.capitalise(), string.find(), string.replace()
1. https://docs.python.org/2.5/lib/string-methods.html
2. https://www.w3schools.com/python/python_ref_string.asp


## Lists
Lists are just like dynamic sized arrays. Lists ```need not be homogeneous always``` which makes it a most powerful tool in Python. A single list may contain DataTypes like Integers, Strings, as well as Objects. ```Lists are mutable, and hence, they can be altered even after their creation.```

```List in Python are ordered and have a definite count.```The elements in a list are indexed according to a definite sequence and the indexing of a list is done with 0 being the first index. Each element in the list has its definite place in the list, which allows duplicating of elements in the list, with each element having its own distinct place and credibility.

Note- Lists are a useful tool for preserving a sequence of data and further iterating over it.

### Creating a list
Lists in Python can be created by just placing the sequence inside the square brackets[]
```
# Creating a List
Blank_List = []
print(f"Blank List: {Blank_List}")

#Accessing list using index
List = [1,34,5,67,6,"Geeks", "For", "Geeks",False,None,45]
print(f"5th Element of list :{List[4]}\n8th Element of list :{List[7]}") 

# Creating a Multi-Dimensional List (By Nesting a list inside a List)
Multi_Dim_List = [['Geeks', 'For'] , ['Geeks']]
print(F"\nMulti-Dimensional List: {Multi_Dim_List}")
```

### Size of List 
```
List2 = [10, 20, 14]
print(len(List2))
```

### Adding Elements to a List
1. Elements can be added to the List by using built-in ```append()``` function. 
2. Only one element at a time can be added to the list by using append() method, for addition of multiple elements with the append() method, loops are used. 
3. Tuples can also be added to the List with the use of append method because ```tuples are immutable.
4. Unlike Sets, Lists can also be added to the existing list with the use of append() method.```

```
# Creating a List
List = []
print(f"Initial blank List: {List}")
  
# Addition of Elements in the List
List.append(1)
List.append(2)
List.append(4)
print("\nList after Addition of Three elements: {List}")
  
# Adding elements to the List using Iterator
for i in range(1, 4):
    List.append(i)
print(f"\nList after Addition of elements from 1-3: {List}")
  
# Adding Tuples to the List
List.append((5, 6))
print(f"\nList after Addition of a Tuple: {List}")
  
# Addition of List to a List
List2 = ['For', 'Geeks']
List.append(List2)
print(f"\nList after Addition of a List: {List}")
```


### List Functions
1. https://docs.python.org/3/tutorial/datastructures.html
2. https://www.w3schools.com/python/python_ref_list.asp
```
b=[23,4,1,56,75,35,42]
b.sort()    #Sort the elements of list 
print(b)    #[1, 4, 23, 35, 42, 56, 75]
b.reverse() #Reverse the elements of list 
print(b)    #[75, 56, 42, 35, 23, 4, 1]
b.append(100) #Appends to the end of list
print(b)    #[75, 56, 42, 35, 23, 4, 1, 100]
b.insert(3,546) #Inserts 546 at index 3
print(b)    #75, 56, 42, 546, 35, 23, 4, 1, 100]  
b.pop(4)    #Removes element present at index 4
print(b)    #[75, 56, 42, 546, 23, 4, 1, 100]
b.remove(546)   #Remove 546 from list
print(b)    #[75, 56, 42, 23, 4, 1, 100]
print(sum(b))
```


### Tuples
1. A Tuple is a collection of Python objects separated by commas.
2. Like Lists Tuples can also contains different types of data type elements.
3. Unlike lists Tuples are immutable.
```
#This code will throw error
tuple1 = (0, 1, 2, 3)
tuple1[0] = 4
print(tuple1)
```

### Creating a Tuple
```
t1 = ()     #Empty tuple
t2 = (1,)   #Tuple with single element t2=(1) is wrong way
```

There are two ways for creating tuples
```
# One way of creation
tup = 'python', 'is','good'
print(tup)
 
# Another for doing the same
tup = ('python', 'is','good')
print(tup)
```

### Deleting a Tuple
```
tuple3 = ( 0, 1)
del tuple3
print(tuple3)
```

### Converting List into Tuple
```
list1 = [0, 1, 2]
print(tuple(list1))
print(tuple('python'))
```

### Tuple Functions
```
t = (1,45,23,56,"Guru",1,1,1,1)
print(t.count(1))   #Return number of occurrences of 1
print(t.index(23))  #Return index of 23 else will give error
print(len(t))       #Return length of the tuple
```

