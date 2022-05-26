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
7. [Tuples](#Tuples), [Creating a Tuple](#Creating-a-Tuple), [Deleting a Tuple](#Deleting-a-Tuple), [Converting List into Tuple](#Converting-List-into-Tuple), [Tuple Functions](#Tuple-Functions)
8. [Dictionary](#Dictionary), [Dictionary Functions](#Dictionary-Functions), [Dictionary with in a dictionary using update function](#Dictionary-with-in-a-dictionary-using-update-function)
9. [Sets](#Sets), [Adding elements in a set](#Adding-elements-in-a-set), [Set Functions](#Set-Functions)
10. [Conditional Statements](#Conditional-Statements), [Is & in](#Is-In)
11. [Loops](#Loops), [Range](#Range), [else with for](#else-with-for), [break](#break), [continue](#continue), [pass](#pass)
12. [Functions](#Functions), [Default Argument](#Default-Arguments), [Recursion](#Recursion), [How to Generate Random Numbers in certain range ](#How-to-Generate-Random-Numbers-in-certain-range)
13. [File I/O](#File-Input-Output), [Reading a File](#Reading-a-File), [Readline Function](#Readline-Function), [Modes of opening a File](#Modes-of-Opening-a-File), [Writing to a File](#Writing-to-a-file), [Append mode](#Append-mode), [with clause](#with-clause)
14. [Classes](#Classes), [Changing Class & Instance Attributes](#Changing-Class-n-Instance-Attributes), [Class & Instance Attribute Preferences](#Class-n-Instance-Attribute-Preferences), [Self](#Self)
15. [StaticMethod](#Staticmethod), [Constructor](#Constructor), [OOP's Properties](#OOPs-Properties), [Modelling a problem in OOP's](#Modelling-a-problem-in-OOPs), [Function Overiding, New attributes in child class](#Function-Overiding-n-New-attributes-in-child-class)
16. [Types of Inheritance](#Types-of-Inheritance), [Single Inheritance](#Single-Inheritance), [Multiple Inheritance & Ambiguity](#Multiple-Inheritance-n-Ambiguity), [Multilevel Inheritance](#Multilevel-Inheritance)
17. [Super Method](#Super-Method), [Class Method](#Class-Method), [Property decorator or Getter & Setter](#Property-decorator-or-Getter-n-Setter), [Operator Overloading](#Operator-Overloading), [Dunder Function (str,len)](#Dunder-Function-str-n-len)
18. [Other](#Other)


### Module
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
3. You can simply access tuple elements just like a list elements, I mean indexing and slicing.
4. Unlike lists Tuples are immutable. Example 
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


### Dictionary

Dictionary: Collection of key value pairs 
1. It is unordered
2. It is mutable (Changeable)
3. It is Indexed
4. Cannot contain duplicate keys
5. A dictionary can contain other dictionaries

#### Note : Dictionary keys are case sensitive.

```
myDict = {
"Fast":"In a Quick Manner",
"Telegram": "Post Card",
"l1": [1,2,4,5,56],
"anotherdict": {'fun':'comedy'},    #Dict with in Dict
1:345
}

print(myDict)

#Indexing
print(myDict['l1']) 

#Dictionaries are mutable
myDict['l1'] = [23,4,56,67,78,89]
print(myDict)

#Printing Dict with in Dict elements
print(myDict['anotherdict']['fun']) 
```

### Dictionary Functions

Some Examples : Keys(), values(), items(), get()
```
myDict = {
"Fast":"In a Quick Manner",
"Telegram": "Post Card",
"l1": [1,2,4,5,56],
"anotherdict": {'fun':'comedy'},
1:345
}
print(myDict.keys())  #Prints the keys of dictionary
print(myDict.values()) #Prints the values of dictionary
print(myDict.items())   #Prints all dictionary elements as a 'DictItems' data types
print(type(myDict.keys())) #Prints type of dictionary i.e.,<class 'dict_keys'>
print(list(myDict.keys()))  #Printing dictionary keys as a list 
print(myDict.get("Something")) #This will return value is key if it exist else none
#print(myDict["Something"]) #But this will throw error if key is not present
print(myDict)
```

### Dictionary with in a dictionary using update function
```
myDict = {
"Fast":"In a Quick Manner",
"Telegram": "Post Card",
"l1": [1,2,4,5,56],
"anotherdict": {'fun':'comedy'},
1:345
}
updateDict = {
    "Life":"Nature",
    "Animal": "Dog"
}
myDict.update(updateDict)
print(myDict)
```
#### Note: If your new dictionary contains a key which is already present in the main dictionary then after update its existing key value is going to be updated with new value.



### Sets
1. Collection of non-repetitive elements that means sets can’t contain duplicate values even if you provide duplicate values it will still show a unique set of values.
2. Also this is hashable that means you can’t change its values just like a tuple & that's why you cannot add a list or dictionary in a set as they are unhashable.
3. Sets are unordered.
4. Sets are unindexed (you can’t access elements with index)
5. There are no ways to change items in a set

```
a = {1,2,5,3,5,3,67,78}
print(a)    #{1, 2, 3, 67, 5, 78}
print(type(a)) #<class 'set'>
```

Note: 
1. Following lines will create an empty dictionary not empty set.
```
b = {}
b = set()	#This Line will create an empty set
```
2. Set can have different types of values in it
```
set = {18,"18",18.1}
print(set)  #{18, 18.1, '18'}
```

### Adding elements in a set
```
a = set()
a.add(4)
a.add(6)
a.add((3,4,5)) 
print(a)	 #{(3, 4, 5), 4, 6}
```

### Set Functions
Some Examples : Remove(), Len(), Pop(), Union(), Intersection(), add()
```
#Remove 6 from 'a' set
a.remove(6)     

#Prints length of a set
print("Length of a : ",len(a))

#Remove an element from a set
print(a.pop())  

#Clears entire set 
print(a.clear())

print("Intersection : ",a.intersection({6,456}))

print("Union : ", a.union({8,11,45,37}))
```

### Conditional Statements

Note: If you write if, elif & else then it is called as if else ladder & only one statement will be executed but it is also possible to write if, else or if, if, if, else. In such cases where we have multiple if’s all the if’s is treated as individual entities & thus multiple output can be seen in multiple true if statements. Also it is not necessary to have if, else statement only if or if, elif statement can also be executed all alone.
```
a = 45
if (a>10):
    print ("The value is greater than 10")
elif (a>20):
    print ("The value is greater than 20")
else:
    print ("The value is",a)
```

### Is In
``` 
a = None
b = [12,23,45,4,57]
if (a is None):
    print("A is none")
print(23 in b)
```

### Loops
#### While Loop
```
list = ["Banana","Grapes","Mango","Chicku"]
i=0
while i<len(list):
    print(list[i])
    i+=1
```

#### For Loop
```
list = ["Banana","Grapes","Mango","Chicku"]
for item in list:
    print(item)
```


### Range
Range(Start , Stop, Step_Size)
```
for i in range(2,200,4):
    print(i)
```

### else with For 
```
for i in range(2,200,4):
    print(i)
else:
    print("This is inside else of for")
```

### break
Note: for loop else will only execute only once that too when for loop will executes till end in following case it will not because it will step out due to break.
```
for i in range(2,200,4):
    print(i)
    if (i==5):
        break
else:
    print("This is inside else of for")
```

### Continue
It basically skips for loop rather than going to next statement, so considering following case it will skip when i = 5 & print its next statement ie., 6 & so forth.
Tip: Best example of continue is to print two conditions like even/odd 
```
for i in range(10):
    if (i==5):
        continue
    print(i)
```


### Pass
It is a null statement in python. Can be used with in If, for & Function
Tip: It's best use is to define all functions first whatever you want to create without writing its entire body.
```
i=10
if (i>0):
    pass
print(i)
```

### Functions
1. The idea is to put some commonly or repeatedly done tasks together and make a function so that instead of writing the same code again and again for different inputs, we can do the function calls to reuse code contained in it over and over again. 
2. Functions can be both built-in or user-defined. It helps the program to be concise, non-repetitive, and organized.
```
#Function Definition
def percent(marks):                   
    per1 = ((marks[0] + marks[1] + marks[2] +marks[2])/400) * 100
    return per1

mark1 = [16,34,67,90]
mark2 = [45,31,79,42]
print(percent(mark1),percent(mark2))  #Function Call 
```

### Default Arguments
Python allows function arguments to have default values. If the function is called without the argument, the argument gets its default value.
```
def greet(name = "Stranger"):
    print("Hello ", name)
    
greet("Gurudutt Goswami")
greet()
```

### Recursion
1. The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. 
2. Using recursive algorithm, certain problems can be solved quite easily. Examples of such problems are Towers of Hanoi (TOH), Inorder/Preorder/Postorder Tree Traversals, DFS of Graph, etc
3. Some simpler problem are finding sum of first n natural number, factorial n etc.
```
def recursive(num):
    if(num==1 or num==0):
        return 1 
    return num *recursive(num-1)

a = recursive(int(input("Enter a number to see its factorial ")))
print(a)
```
#### How Recursion Works 
![Untitled-Diagram58](https://user-images.githubusercontent.com/86184439/169806985-c7c4a518-94ed-43bc-9cc8-110082932aaa.jpg)

### How to Generate Random Numbers in certain range 
```
import random
print(random.randint(1,50))
```


### File Input Output

### Reading a File
1. By default, the mode is ‘read’
2. In case you want to work on some file which is not there is your current directoy then instead of backlash you need to use forward slash like '/' to specify its path along with its extension.
#### Tip: Optional You can also specify the number of character you want to read from a file in read function like read (10).
```
f = open("something.txt", "r")
data = f.read()
print(data)
f.close()
```


### Readline Function
Readline function only read a single line at a time
```
f = open("something.txt","r")
#Read 1st line
data = f.readline()
print(data)
#Read 2nd line
data = f.readline()
print(data)
f.close()
```


### Modes of Opening a File
1. r : Open for reading
2. w : Open for writing
3. a : Open for appending
4. '+' : Open for Updaing
5. rb : Open for read in binary mode
6. rt : Open for read in text mode, though if don't mentioned mode python automatically takes this only.


### Writing to a file
Note : If you write multiple lines using seperate f.write() functions before closing the file with f.close() then all those statements are going to be written in file.
```
f = open("Important works.txt","w")
f.write("This is just an example of write function ")
f.close()
```


### Append mode
```
f = open('something.txt', 'a')
f.write("This is going to append not overwrite like write mode")
f.close()
```

### with clause 
1. Using with clause we don’t have to close a file 
#### Note : You can't pass a number directly into f.write() function it must be converted into string, so either you need to give that in quotes or convert that into string using str() function.
```
with open('something.txt', 'r') as f:
    a = f.read()
with open('something.txt', 'w') as f:
    a = f.write("me")
print(a)
```


### Classes 
1. Class creates a user-defined data structure, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. 
2. A class is like a blueprint (template) for an object.
3. Attributes are the variables that belong to a class.
4. Attributes are always public and can be accessed using the dot (.) operator. Eg.: Myclass.Myattribute

```
class RailwayForm():
    def Application(self):
        print(self.sno)
        print(self.Name)

applicant = RailwayForm()
applicant.sno = 245 
applicant.Name ="Gurudutt Goswami"
applicant.Application()
```

### Changing Class n Instance Attributes

#### Following is an example of instance/object attribute
```
class RailwayForm():
    CompanyName = "Google"
Gurudutt = RailwayForm()
Bhishma = RailwayForm()
Gurudutt.Salary = 300000
Bhishma.Salary = 500000
print(Gurudutt.Salary)
print(Bhishma.Salary)
```

#### Note: You can change an attribute of a class for an instance/Object or even a class attribute itself. Here ‘CompanyName’ is an example of class attribute.
```
class RailwayForm():
    CompanyName = "Google"

Gurudutt = RailwayForm()
Gurudutt.CompanyName = "Microsoft"  #Changing an attribute of a class for an instance basically changing instance attribute
Bhishma = RailwayForm()
print(Gurudutt.CompanyName)
print(Bhishma.CompanyName)

RailwayForm.CompanyName = "Oracle"  #Changing a class attribute
print(Gurudutt.CompanyName)
print(Bhishma.CompanyName)
```


### Class n Instance Attribute Preferences
#### Note: Note: Instance attributes take preference over class attributes during assignment & retrieval. Also if you have a class attributes & you are trying to change that class attribute for an instance then a new instance attribute will be created instead of modifying a class attribute.

```
class CompanyName():
    name = "Google"
obj = CompanyName()
obj.name= "Microsoft"
print(CompanyName.name)
print(obj.name)
```


### Self
#### Self represents the instance of the class. By using the “self”  we can access the attributes and methods of the class in python. It binds the attributes with the given arguments.

#### How to use both class & instance attributes using self
Note: In following example Harnam.getSalary() is equivalent to Employee.getSalary(Harnam) that’s why if you don’t mention ‘self’ in getSalary function as an argument you will get an error as indirectly it should take an argument which you are passing ie., Harnam.
```
class Employee:
    CompanyName = "Google"    #Class Attribute
    Salary = 100000
    def getSalary(self):
        print(f"The salary of {self.Name} Who is working in {self.CompanyName} is {self.Salary} ")

Harnam = Employee()
Harnam.Name = "Harnam Singh"  #Instance Attribute
Harnam.Salary = 200000        #Instance Attribute
Harnam.getSalary()            #Employee.getSalary(Harnam)
```


### Staticmethod
If you want to call a method without mentioning ‘self’ in the argument since it can be just a simple print statement, then you can use a decorator name as @Staticmethod.
```
class a:
    @staticmethod
    def greet():
        print("Good Morning !!")

Anurag = a()
Anurag.greet()
```

### Constructor

Note: Constructors got automatically invoked when an object of a class is created but it doesn’t mean it can’t have more arguments.
```
class Admission():
    def __init__(self,student_name,student_gender,student_ClassNo):
        self.name = student_name
        self.gender = student_gender
        self.classno = student_ClassNo
        print("New Student Enrolled  ")

    def admission_details(self):
        print(f"The name of student is {self.name}")
        print(f"The Gender student is {self.gender}")
        print(f"The Class of student is {self.classno}")

Gurudutt = Admission("Gurudutt Goswami","Male",12)
Gurudutt.admission_details()
```


### OOPs Properties
#### Data Abstraction :  is a process of providing only the essential details to the outside world without revealing its implementation details.
#### Encapsulation :  is defined as the wrapping up of data under a single unit. It is the mechanism that binds together code and the data it manipulates.




### Modelling a problem in OOPs
The scale/scope should be quite large as for smaller things like avarage of 4 numbers its not going to be that efficient.

1. Class Name : Noun : संज्ञा की परिभाषा:- वह शब्द जो किसी प्राणी, वस्तु, स्थान, गुण, अवस्था, भाव एवं विचार के नाम का बोध कराता है संज्ञा कहलाता है |
2. Attributes of Class : Adjective : (विशेषण):- जो शब्द वाक्य में noun या pronoun की विशेषता बतलाते है उसे हम adjective यानि की हिन्दी में विशेषण कहते है|
3. Methods of Class : Verb : जिन शब्दों से किसी कार्य का करना या होना व्यक्त हो उन्हें क्रिया कहते हैं। जैसे- रोया, खा रहा, जायेगा आदि।





### Inheritance
#### Inheritance is the capability of one class to derive or inherit the properties from another class. The benefits of inheritance are: 
 
1. It represents real-world relationships well.
2. It provides reusability of a code. Also, it allows us to add more features to a class without modifying it.
3. It is transitive in nature, which means that if class B inherits from another class A, then all the subclasses of B would automatically inherit from class A.

```
class a():
    def a_method(self):
        print("This is A class")
class b(a):
    pass
obj = b()
obj.a_method()
```


### Function Overiding n New attributes in child class
1. We can use the method attributes of parent class in child class. 
2. Also you can override, add new attributes & method in the child class, just like following example.
```
class Employee():
    CompanyName = "Google"

    def showDetails(self):
        print(f"This is base class")

class programmer(Employee):
    
    #New Attribute
    progLang = "c++" 

    #New Method of child
    def progLang(self): 
        print(f"The programming is {self.progLang}")

    #Overiding showDetails Method 
    def showDetails(self):  
        print("This is child class")

p1 = programmer()   # Object of programmer class
print(p1.CompanyName)   #How to access base class attributes that are not in child class
p1.showDetails()
```


### Types of Inheritance
#### Single Inheritance
![single](https://user-images.githubusercontent.com/86184439/170061507-d27ee282-cfd8-4b7e-a843-84f13f7ba84e.png)

```
class a():
    def a_method(self):
        print("This is A class")
class b(a):
    pass
obj = b()
obj.a_method()
```

#### Multiple Inheritance n Ambiguity
Note: Whenever these is an ambiguity child class will prioritize based on how classes names are given while inheriting, so in following example in ambiguity situation (commented code) you will get Google not Facebook since Employee is first while inheriting.
![multiple](https://user-images.githubusercontent.com/86184439/170061555-25ce9394-c0d2-4662-925a-6b258a1723f3.png)

```
class Employee():
    CompanyName = "Google"

class freeLancer():
    CoderLevel = 0
    CompanyName = "FaceBook"

    def levelUpgrade(self):
        self.CoderLevel = self.CoderLevel + 1

#This is multiple inheritance
class programmer(Employee,freeLancer): 
    name = "Gurudutt Goswami"

p1 = programmer()   
print("Starting Level : ",p1.CoderLevel)
p1.levelUpgrade()
print("New Upgraded Level : ", p1.CoderLevel)
print("Company Name is " , p1.CompanyName)  #Ambiguity Situation
```

#### Multilevel Inheritance
![Multilevel](https://user-images.githubusercontent.com/86184439/170061599-cfe2277b-dac0-4d12-b110-ee0bc4ffcc34.jpg)

```
class a():
    companyName = "xyz"

    def fun(self):
        print("I am having fun !!")

class b(a):
    companyName = "FightClub"
    invoice = 25

    def funny(self):
        print("I am very cool")

class c(b):
    animal = "horse"

    def happy(self):
        print("This is very cool !!")

obj_1 = c()

#It will first go to the nearest class rather than main class
print(obj_1.companyName)
#If nearest class don't have that attribute or method then it will go to the base class
obj_1.fun()
```


### Super Method 
```
class a():
    def fun(self):
        print("Grandfather")
class b(a):
    def fun(self):
        super().fun()
        print("Father")
class c(b):
    def fun(self):
        super().fun()
        print("Son")

obj_1 = c()
obj_1.fun()
```
Note: You can also use Super to run constructor of base classes, just like following:
```
class a():
    def __init__(self):
        print("I am First")

    def fun(self):
        print("Grandfather")
class b(a):
    def __init__(self):
        super().__init__()
        print("I am second")

    def fun(self):
        super().fun()
        print("Father")
class c(b):
    def __init__(self):
        super().__init__()
        print("I am Third")

    def fun(self):
        super().fun()
        print("Son")

obj_1 = c()
```




### Class Method
1. When you define any attribute of a class using object/instance of that class then instance attribute is created, class attribute remains as it is, so if you want to explicitly change or refer class attribute then you can use ClassMethod. 
2. Let’s suppose you want to change the class attribute (name) of following class rather than creating an instance attribute then there are 3 methods:
    1. Using @classmethod decorator
    2. Using a dunder method like '__class__'.
    3. Directly refering class attribute by class_name.attribute.
```
class a():
    name = "Gurudutt Goswami"
    
    # @classmethod                        #Using Class Decorator
    def print_name(self,name):
        # self.name = name
        self.__class__.name = name        #Using dunder method

object_1 = a()
print(object_1.name)
a.name = "horse rider"                    #3rd Way where we directly refer class attribute with class_name.attribute
print(object_1.name)
object_1.print_name("Anurag Basu")
print(object_1.name)
```



### Property decorator or Getter n Setter
1. In the following example we are controlling ‘Total’ as a function but in actual it’s an attribute & if you want to modify the value of b according to ‘Total’ value passed by you then you can use setter function & in that function you can basically define relationship between Total & b.
2. If you want to see this in action, try to change the value of ‘Total’ after object creation statement & check the value of b.
```
class a():
    a = 1000
    b = 200

    @property   #also call getter function
    def Total(self):
        return self.a + self.b

    @Total.setter
    def Total(self, num):
        self.b = num - self.a

obj1 = a()
print(f"Starting Value : {obj1.Total}")
obj1.Total = 1100                   #This assignment is invoking Total setter function
print(f"value of a : {obj1.a}")
print(f"Modified Value of b is : {obj1.b}")
```



### Operator Overloading
1. You can do anything on operator with the help of invoking some predefined dunder methods in python. Basically that means you can catch operator & thus can control what to do afterwards.
2. Following are examples of overloading +, -, *, /, //, str
```
class a():
    def __init__(self,num):
        self.num = num
    
    def __add__(self,val):
        return self.num + val.num
    
    def __sub__(self,val):
        return self.num - val.num
    
    def __mul__(self,val):
        return self.num * val.num
    
    def __truediv__(self,val):
        return self.num / val.num

    def __floordiv__(self,val):
        return self.num // val.num

obj1 = a(25)
obj2 = a(10)

sum = obj1 + obj2
sub = obj1 - obj2
mul = obj1 * obj2
div = obj1 / obj2
fdiv = obj1 // obj2

print(f"Sum {sum}")
print(f"Sub {sub}")
print(f"Mul {mul}")
print(f"Div {div}")
print(f"Floor Div {fdiv}")
```

### Dunder Function str n len
1. If you print an object in following way you will get something like 
      "<__main__.a object at 0x0000019ABFF2F6A0>" & this is primarily because you have’t configured string dunder. 
2. In order to print object’s value in correct way try to invoke string dunder function just like image following this.
```
class a():
    def __init__(self,num):
        self.num = num
obj = a(10)
print(obj)


class a():
    def __init__(self,num):
        self.num = num

    def __str__(self):
        return f"{self.num}"

    def __len__(self):
        return 467
obj = a(10)
print(obj)
print(len(obj))
```
#### Note: For more please refer: https://docs.python.org/3/reference/datamodel.html


### Try Except Clause
1. Errors are the problems in a program due to which the program will stop the execution. On the other hand, exceptions are raised when some internal events occur which changes the normal flow of the program.Try and Except statement is used to handle these errors
2. A try statement can have more than one except clause.
```
try:
    # Some Code which we to want to run but will throw an error in certain situations
except:
    # Executed if error in the
    # try block
```
### Note : Try block code will execute & run till the point its not throwing an error, once error occured only then it will go to the exception block. For example if there are 10 lines of code in try block & 5th line throws an error then output of above 4 lines will be excuted perfectly & then only except clause will run. Also if there other lines outside & below the except clause then after try block clause thing that will also run.

```
while(True):
    print("Enter q to quit!")
    num = (input("Enter a number "))
    try:
        if(num == 'q'):
            break
        else:
            num = int(num)
            if(num >= 10):
                print("You number is greater than or equal to 10")
            else:
                print("You number is less than 10")
    except Exception as e:
        print(f"Type a number !!\nError Details : '{e}'")
print("Exiting Program")
```


### How to catch different error to handle explicitly
```
try:
    num = int(input("Enter a Number : "))
    a = 1/num
    print(a)

except ValueError as e:
    print("Please type a numeric value !")

except ZeroDivisionError as e:
    print("a = 1/your entered number, so it can't be 0, try to enter a different number ")

except NameError as e:
    print(f"Error Occured \nError Details : {e}")

except Exception as e:
    print(f"This needs to be handled ! \nError Details : '{e}' ")

print("Exiting Program !")
```


### How to raise an exception?
```
def a(num):
    try:
        return int(num) + 1
    except:
        raise TypeError("This is a raised Exception !")
a = a('fun')
print(a)
```



### try with else
#### Note: Else things will only execute if try thing runs successfully
```
try:
    num = int(input("Enter a number "))
    c = 1/num
    print("1/your enter number is :",c)
except Exception as e:
    print(f"Exception Occured\nError Details :{e}")
else:
    print("Program Executed Successfully !")
```




### Finally

#### This piece of code will run in any condition even if you define exit() in exception and for this reason this is used to clear up things like close files, close database connection, close chat, session terminate etc.
```
try:
    num = int(input("Enter a number "))
    c = 1/num
    print("1/your enter number is :",c)
except Exception as e:
    print(f"Exception Occured\nError Details :{e}")
    exit()
finally:
    print("Program Executed Successfully !")
print("Thanks for using this program")
```




### Other
1. To see detail regarding any particular thing of a code in VSCode, just go to that word & click on that word while pressing ctrl.
