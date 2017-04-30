Rocket Propulsion Laboratory Python Style Guide
===============================================

*Author: Patrick Liu*

*Last Modified: April 30, 2017*

All Python code written for RPL purposes should follow
the guidelines outlined in this document.

All Python code written for RPL should be interpreted with Python 3.6+
For anything not covered in this guide, refer to the official Python style guide:

[Official Python Style Guide](https://www.python.org/dev/peps/pep-0008)

File Extensions and Naming
---------------

*   All Python source files should have the file extension .py
*   All Python sources files should be in all lowercase
  
Headers and Comments
--------------------

*   At the top of every Python source file, there should be a docstring
    with a file header, containing:
    +   Name of the file
    +   Date the file was last modified
    +   Author(s) of the file
    +   Team that the file is associated with
    +   Short description of the file
<!-- -->

    """
    Filename: example.py
    Last Modified: April 30, 2017
    Author: Patrick Liu
    Team: Launchy McLaunchface/Avionics
    Description: Example header for a Python source file
    """
*   Complex blocks of code should have a comment
    +   Function calls, loops, and if-statements should have a comment
        describing what they do
    +   Assume the reader knows Python, but doesn't know what your code does
<!-- -->
    Good:
    #if foo, inform user that foo happened
    if foo:
       print("Foo happened")
  
    Bad:
    #if foo
    if foo:
       #print "Foo happened"
    

*   Above each function, there should be a docstring with a function header, containing:
    +   Name of the function
    +   Description of the function
    +   Parameters expected by the function
    +   Expected return value

<!-- -->
    """
    Function name: foo
    Description: Example function header
    Parameters: None
    Return Value: none
    """
*   Above a block of tests, there should be a docstring, containing the name of
    the module to be tested

<!-- -->
    """
    Module to be tested: foo
    """

*   Above each test case, there should be a docstring, containing:
    +   Input
    +   Expected output

<!-- -->
    """
    Input: 5
    Expected output: true
    """

Organization and Whitespace
---------------------------

*   To indent blocks of code, use four spaces
    +   Do not use tabs, unless you configured your tab key to output spaces

*   Attempt to avoid parentheses, if possible
    +   Python is designed to be as readable as possible, and avoiding 
        parentheses vastly improves readability

<!-- -->
    Good:
    if foo:
        #code

    Bad:
    if(foo):
        #code

*   Avoid numbers that aren't 0, 1, -1 in your code. Instead, define 
    module-level constants to hold these values

<!-- -->.
    Good:
    FOO_CONSTANT = 5

    foo = FOO_CONSTANT

    Bad:
    foo = 5

*   Lines of code should be at most 80 characters long

Variables
---------

*   Variable names should be descriptive
    +   This means, in general, that single letter variable names should not be used
    +   Variables should be all lowercase, with words connected by spaces
    +   Variable names should not include leading or trailing underscores
    
<!-- -->
    Good:
    foo_counter = 1
    bar_counter = 2

    Bad: 
    x = 1
    fooCounter = 1
    Bar_Counter = 1
    _foobar_ = 1

*   Module-level constants should be in ALL_CAPS, separated by spaces

<!-- -->
    Good:
    FOO_CONSTANT = 5

    Bad:
    fooConstant = 5


Miscellaneous
------------

*   Close files explicitly after file operations are complete
