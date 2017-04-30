Rocket Propulsion Laboratory C Style Guide
==========================================

*Written by Patrick Liu*

*Last updated: April 30, 2017*

All C code written for RPL purposes should follow the guidelines outlined
in this document.

File extensions
---------------

*  All C source files should have the file extension .c
   Similarly, all C header files should have the file extension .h

        Good: foo.c, foo_header.h

        Bad: foo

*  All executable files should have the file extension .o, and 
   should not be the default name(a.out) 

        Good: foo.o

        Bad: foo


Headers and Comments
--------------------

*  All files should have a file header, containing at least:
   +   Name of the file
   +   Date the file was last modified
   +   Author(s) of the file
   +   Team that the file is associated with
   +   Short description of the file
<!-- -->
        /*
         * Filename: example.c
         * Last Modified: April 30, 2017
         * Author: Patrick Liu
         * Team: Launchy McLaunchface/Avionics
         * Description: Example of a file header for a C source file
         */

* Complex blocks of code should have a comment 
   +   Function calls, loops, and if-statements should have a 
       comment describing what they do
   +   Assume the reader knows C, but doesn't know what your code does

 <!-- -->
    Good: 
    //If the test succeeds, print a notification
    if(success){
        printf("Yay");
    }  

    Bad:
    if(success){
        printf("Yay");
    }
          
    Bad:
    //if success evaluates to true, print "Yay" to the terminal
    if(success){
        printf("Yay");
    }
  
Preprocessor Directives
-----------------------

*  Preprocessor directives should be at the top of the C source or header file,
   immediately below the file header
 
*  Preprocessor directives should be grouped by type, and different types
   of preprocessor directives should be separated by a blank line
<!-- -->
    Good:
    #include <stdio.h>
    #include <stdlib.h>

    #define FOO 10
    #define BAR 11

    Bad:
    #include <stdio.h>
    #define FOO 10
    #include <stdlib.h>
    #define BAR 11

Organization, Whitespace, and Indentation
-----------------------------------------

*   Nested blocks of code should be indented by four spaces per level of
    nesting
    +   This means that your header, preprocessor directives, and outer 
        functions should be left-justified, and each block of code inside
	curly braces should be indented by another four spaces
    +   Do NOT use tabs unless your tab key is configured to enter spaces
<!-- -->
    Good:
    #include <stdio.h>

    main(){      
        int bar;
        bar = 10;
        if(bar == 100){
            printf("Foo");
        }
    }

    Bad: 
    #include <stdio.h>

    main(){
    
      int bar;
 	bar = 10;
       if(bar == 100){
          printf("Foo");	}
    }

*   An opening curly brace should be placed immediately adjacent to 
    the statement requiring it, and a closing curly brace should be 
    by itself on a new line, with the same level of indentation as the 
    original statement
    +   Furthermore, the code inside that curly brace should start on the
        line immediately following the opening curly brace
    +   Curly braces should always be used when they can, even if they are 
        optional
<!-- -->

    Good:
    if(1){
         //something
    }

    Bad:
    if(1)
    { //something }
 
*   Each statement should be on its own line
    +   This means that multiple variable declarations should not be used
<!-- -->
    
    Good:
    int foo;
    int bar;

    Bad:
    int foo, bar;

*   Each line of code in a file should be a maximum of 80 characters long

Variables
--------

*   Variable names should be descriptive
    +   This means that single letter variable names should 
        generally not be used
    +   An exception to this rule is loop iteration variables named i and j,
        as those are generally expected practice, as well as fd for file
	descriptor
<!-- -->
    Good:
    int foo_count;
    int bar_count;

    Bad:
    int x;
    int y;

*   Variable names should be lowercase, with word separated by underscores,
    and should not have leading or trailing underscores
    +   Constants should be in ALL CAPS

<!-- -->
    Good:
    #define FOO_CONSTANT 10

    int foo_count;
    int bar_count;

    Bad:
    #define foo_constant 10

    int foocount;
    int BarCount;

Miscellaneous
-------------

*   Always close files explicitly when file operations are complete

*   Use stderr for error output or diagnostic output 
    +   This means using fprintf()


