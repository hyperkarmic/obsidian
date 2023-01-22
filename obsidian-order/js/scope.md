# scope

Scope: Scope stands for variable access. So, the question is, what variable do I have access to when a code is running? However, in Javascript, you are always in the root scope by default (the window scope). These boundaries restrict variables and determine whether or not you have access to them. It restricts a variable’s visibility or availability to other parts of the code
<hr>

Scope:In JavaScript, we have three scopes: global scope, function scope, and block scope. Global scope is that first-level, ancestor-to-all scope. There is only one global scope in the entire script. Function scope is a scope created every time a function is created. And block scope is a scope created for conditionals and loops.
***
Think of a database schema as a type of data structure. It represents the framework and arrangement of the contents of an organization’s data.
Scope:The area where a variable is recognised;
***
![[scope.png]]
***
-   The scope is the current context of execution in which values and expressions are "visible" or can be referenced. If a variable or expression is not in the current scope, it will not be available for use. Scopes can also be layered in a hierarchy, so that child scopes have access to parent scopes, but not vice versa.
-   In other words, scope refers to the boundary in which a variable or expression is relevant or holds certain meaning.
***
Scope is the visibility of functions and variables in the different parts of your code.

In other words, the scope of a variable or a function is the part of the code in which it is available. Working with variables and scope comes intuitively to most developers but knowing the rules will help you avoid some pitfalls.

In JavaScript, we have three types of scope - global, function, and block
***
In short, **“Where you can access your declaration in the code called Scope”.**
***
Scope is the accessibility of variables, functions, and objects in some particular part of your code during runtime. In other words, scope determines the visibility of variables and other resources in areas of your code.

As per the above definition of Scope, So, the point is limiting the visibility of variables and not having everything available everywhere in your code.

the scope is defined in main two ways,

-   Global Scope
-   Local Scope
***

Scope consists of a series of bubbles that each act as a container or bucket in which identifiers are declared , these bubbles nest inside each other and this nesting is defined at author time.

[Kyle Simpson](https://twitter.com/getify?ref=hackernoon.com) (Author of YDKJS series)#scope
***
![[scope.jpg]]
#js #javascript