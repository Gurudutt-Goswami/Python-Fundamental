# Python-Fundamental


1. Python Download Link : https://www.python.org/downloads/
2. Microsoft Visual Studio Code : https://code.visualstudio.com/download
3. Imp Extensions for Visual Studio Code : Python, Pylance,Material Icon Theme, Live Server, DJango
4. After installation open cmd (or Window power shell if you are using Windows) & type 'python', to see version only type 'python --version'
5. Python is a high level, Poratable, Open Source & case sensitive language.

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
### dir() Function
The dir() built-in function returns a sorted list of strings containing the names defined by a module. The list contains the names of all the modules, variables, and functions that are defined in a module.
```
from random import *
print(dir(random))
```

## What is pip?
Python pip is the package manager for Python packages. We can use pip to install packages that do not come with Python. The basic syntax of pip commands in command prompt is: 
```
pip install flask

##### Specifying Package Version
We can also install the package of a specific version by using the below command.
```
pip install package_name==version
```
##### List installed packages with pip
The Python pip list command displays a list of packages installed in the system. 
```
pip list
```
##### Uninstall packages with pip
The Python pip uninstall command uninstalls a particular existing package. 
```
pip uninstall numpy
```
##### Listing additional packages with pip
The Python pip freeze command is used to list packages that don’t come pre-installed with Python. 
```
pip freeze
```
##### Listing Outdated Packages with pip
Python pip list –outdated command is used to list all the packages that are outdated. This command cross-checks the installed package information with the pip repository.
```
pip list --outdated
```
##### Upgrading packages with pip
Python pip install –user –upgrade is used to update a package.
```
pip install --user --upgrade package_name
We can also upgrade any package to a specific version using the below command.
pip install --user --upgrade package_name==version
```
##### Downgrading packages with pip
The Python pip install –user command is used to downgrade a package to the specific version.
```
pip install --user package_name==version
```
