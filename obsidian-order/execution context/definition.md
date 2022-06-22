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

#execution-context #javascript #js
