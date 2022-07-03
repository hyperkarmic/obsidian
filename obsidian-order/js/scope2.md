# scope 
# **What is Scope?**

Scope in JavaScript refers to the accessibility of variables, functions, and objects during runtime.

In JavaScript, there are three types of scopes:

-   Global Scope
-   Functional Scope
-   Block Scope

## **Global Scope:**

Global scope is the outermost scope, a variable is in global scope if it’s declared outside of a block.

`window` and `document` are global variables provided by the browser.
Variables inside the global scope can be accessed and altered in any other scope.

## **Functional Scope:**

Any variables or functions declared inside a function have local/functional scope, which means that they can be accessed within the function and not outside of it.

## **Block Scope:**

Block scope tells us that any variable declared inside a block **{}**, can be accessed only inside that block and cannot be accessed outside of it.  
Block scope is related to variables declared using `let` and `const` only, `var` do not have block scope.

#scope #js #javascript 