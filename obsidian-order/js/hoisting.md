# hoisting
**Hoisting** is a process that happens during the creation of execution context, which will move the declarations of variables and functions up to the top of the context. Let’s start with an example:
***
# Hoisting:

When executing a JavaScript code, the JavaScript engine goes through two phases:

-   **Parsing**:- JS engine moves all the variable declarations to the top of the page if the variable is global otherwise at top of the function if declared within a function.
-   **Execution**:- JS engine assigns values to the variable and executes it.

So, hoisting is a mechanism that the JavaScript engine moves all the variables, functions `declaration` to the top of their scope, before the execution of the code. It allows functions and variables to be used in code before they are declared.
***
# Variable Hoisting

In JavaScript, there are three different ways to declare a variable — `var`, `let`, and `const`. There are two steps: variable **declarations** and **initialization.**  
JavaScript Interpreter only moves the declaration to the top of the code and not initialization.

Variable Hoisting acts differently depending on how the variable is declared. Let’s first understand `var` hoisting.

## Var Hoisting

When JS interpreter hoist a variable declared with `var`, it initializes its value to `undefined`.

If we forgot the declaration and only initialize the value, the variable isn’t hoisted. Trying to read the variable before it is initialized and not hoisted will throw a `ReferenceError` exception.

However, initialization also causes declaration (if not already declared). The code below will work, as even though it isn’t hoisted, a variable is initialized and effectively declared before it is used.
***

## let and const hoisting

Variable declared with `let` and `const` are hoisted but not initialized with a default value, unlike `var`. Trying to read the variable before it’s declared will be thrown an exception of `ReferenceError`.

Notice that the interpreter still hoists the variable ‘data’: the error message indicates that the variable is initialized somewhere.

As we have seen above, variables are hoisted to the top of their scope. Next, let’s look at how function scoped variables are hoisted.

## Functional Hoisting

Function hoisting allows us to call a function before it is defined. Let’s take an example and try to guess the output
***
# Conclusion:

Let’s summarize this article:-

-   let and const are **block** scope whereas var is a **global** scope
-   var, let and const are all hoisted but unlike var, the other two are not initialized with a default value (**undefined**).
-   Function declarations are hoisted but not functional expressions

We should make it a habit to use `let` and `const` over `var` to avoid unnecessary errors.
#hoisting #js #javascript 