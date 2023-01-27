Lexical Environment: The Lexical environment can be defined as the local memory of an EC with a reference to the lexical environment of its parent. The Lexical environment store the variable defined in that function during the execution of that function. It is important to understand what is a lexical environment to understand Closures in


***

In JavaScript, the lexical environment is the environment in which a piece  
of code is executed. It consists of two components:

-   the environment record and
-   the outer environment reference.

The **environment record** is a data structure that stores the variables and  
their values that are defined within the lexical environment. It also  
stores information about the bindings, or associations, between the  
variables and their values.

The **outer environment** reference is a reference to the lexical environment  
that surrounds the current lexical environment. It allows the current  
lexical environment to access the variables and values defined in the outer  
lexical environment, if they are not defined within the current environment.
***
When a function is defined or a code block is entered, a new lexical  
environment is created. The lexical environment is set to this new  
environment and the variables and values defined within it become  
accessible. When the function is called or the code block is exited, the  
lexical environment is restored to the environment that was in place before the function was called or the code block was entered.

The lexical environment is important in JavaScript because it determines  
the scope of variables. In JavaScript, the scope of a variable is the  
region of the code in which it is accessible. Variables that are defined  
within a lexical environment are only accessible within that lexical  
environment and any inner lexical environments.
***
## Lexical environment

Lexical environment is created when you enter a block of code or when a function is defined. It determines the scope of a variable or function, which is the part of the code where it can be accessed.

A lexical environment is associated with each execution context, and it is used to look up the values of variables and functions. When a variable or function is accessed, the JavaScript engine uses the current execution context’s lexical environment to determine its value.
***

#lexical-environment
#execution-context 
