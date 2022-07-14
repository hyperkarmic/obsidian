# execution context definition

.Execution Context:_Execution context is an environment where JavaScript code is executed and evaluated. Simply put, Everything inside JavaScript happens inside the Execution context._

_Execution Context:__Execution Context_

Execution Context (EC) is the environment where the information of the currently executing code is held. EC contains two parts, **Variable Environment**, which

stores all variables with their values, and **Thread of Execution** which includes code related to the particular context.

Initially, a **Global Execution Context** (GEC) will be created before the execution of the code. Then once a function is called, a **Functional Execution Context** (FEC) related to that function will be created, including the variables and the code. JS engine will create an EC (GEC and FEC) in two stages, the **Creation phase**, and the **Execution phase**.

**Creation phase** — In this phase, the JS engine will allocate memory to the variables and functions in the EC. For variables, it will store the spatial value _undefined_ and the complete function code for functions in the allocated memory. If a function is declared as an arrow function, it will not store the function code, but it will be assigned undefined.
***

Execution Context:Any time you run a JavaScript file on your browser, an execution context is created. An execution context is just an environment created for a block of code that’s currently being executed. So on running the file, initially a “**Global execution context”** is created for the whole file. When the JS engine goes through the file and comes across a function, a separate **functional execution context** is created. The code inside these contexts is executed in essentially 2 phases. A “**Creation phase”** and an “**Execution Phase**”. 
*** 
Execution Context:is. In simple terms, it’s an environment created for a block of code and its dependencies.   JavaScript engine looks at a piece of code, checks what all resources it needs to execute, and then bundles them all together in a block. This block is an execution context created for that piece of code. There could be several such execution contexts in a script. Let’s take a look at an example to understand it better.
***
If we are wishing to learn Javascript, then we should be aware of one of the fundamental concepts of javascript which is whenever we run a javascript program an **_Execution Context_** is created and all the processes are completed within this execution context. Execution context on the other hand is created in two phases, one is the **Memory Creation** phase (_Variable Environment_) and the second one is **_Code Execution_** phase (_Thread of Execution_).
***
An `Execution Context` refers to the code that is currently running and everything else that helps run it.

It is possible to have lots of lexical environments, but the Execution Context manages the currently running one.

Each of the Execution Context comprises an `Environment Record`.
***
![[2 parts of xc.png]]
***
![[2xc phases.png]]
***
![[execution.png]]
***
**Global Execution context**: Global EC is the default Execution context. Why default? Well, because as soon as JS code runs, GEC is created.

_Try this out: create a .js file and run it. Even though the file doesn’t contain a single line of code, GEC is created._

GEC performs these two tasks:

-   It creates a global object for Node.js and Window object for the browsers.
-   Reference the Windows object to the ‘this’ keyword.

**Functional Execution context**: Whenever a function is invoked or called a brand new EC is created. Each function has its own EC, hence there can be any number of FEC.
**Eval function** **Execution context**: Code executed inside an eval function gets its own execution context.
***
**The execution context is created in two phases**

-   **Memory Creation phase**: In this phase memory is allocated to the variables and functions and is stored in key-value pairs.

**In the first phase**, JS skims through the code line by line and it allocates memory to variables and functions.

In the case of variables, JS assigned a special keyword undefined. In the case of functions whole code of the functions is copied and assigned.


-   **Code Execution phase**: In this phase code is executed line by line and values are assigned.

**In the second phase**, JS again runs through the code line by line. Now code is being executed, here all the calculations and evaluation will take place.

Now when JS encounters the return keyword, it returns the control of the program where the function was invoked which is GEC and we get the output as _John Doe_.

After the execution of the whole program, GEC is deleted. One important concept here to understand is the **Call stack**.

> Call stack maintains the order of execution of EC.

Call stack follows LIFO(Last in first out)
***
## What is the Execution Context?

Imagine your code is placed inside a box whenever you write JS code. That box is the Execution context, a conceptual environment created by JS for code evaluation and execution.
***
There are three types of Execution Context in JS.

1.  The Global Execution Context (GEC): This is the primary or base Execution Context. It is the highest level of abstraction for an execution context in JS. It has two main functions: (1) Create a global object, and (2) Attach the `this` value to the global object
2.  The Function Execution Context (FEC): An execution context is created for every function invocation. It is not created when the function is declared, only when called or invoked. When a function is called, it is executed through the execution stack (which we’ll discuss below).
3.  The `eval()` Execution Context: Due to the malicious nature of eval(), it is rarely used in JS so we won’t discuss it. However, an execution context is created whenever it is used.
***
## How the execution context is created.

The execution context is created in two stages: 1. Creation stage, and 2. Execution stage.

### CREATION STAGE

A lexical environment is created in the creation stage of the execution context. It is of two types:

1.  Lexical Environment: This is the primary Lexical Environment.
2.  Variable Environment: This is a Lexical Environment used explicitly by the `var` _VariableStatement_ within an Execution Context.
   ***
The Environment Record is of two types:

-   Declarative Environment Record: This is mainly used by a Lexical Environment created in the Function Execution Context. It records (store) function declarations and variable declarations. The Declarative Environment Record also stores an `arguments` object, which contains the length(number) of argument(s) passed to a function, and a map of the argument(s) and its index.
-   Object Environment Record: This is mainly used by a Lexical Environment created in the Global Execution Context. It stores function declarations, variable declarations, and a global binding object(window object in browsers).
***


#execution-context #xc #definition 
#execution-context #javascript #js
