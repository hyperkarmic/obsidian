# execution context definition

.Execution Context:_Execution context is an environment where JavaScript code is executed and evaluated. Simply put, Everything inside JavaScript happens inside the Execution context._

_Execution Context:__Execution Context_

Execution Context (EC) is the environment where the information of the currently executing code is held. EC contains two parts, **Variable Environment**, which

stores all variables with their values, and **Thread of Execution** which includes code related to the particular context.

Initially, a **Global Execution Context** (GEC) will be created before the execution of the code. Then once a function is called, a **Functional Execution Context** (FEC) related to that function will be created, including the variables and the code. JS engine will create an EC (GEC and FEC) in two stages, the **Creation phase**, and the **Execution phase**.

**Creation phase** — In this phase, the JS engine will allocate memory to the variables and functions in the EC. For variables, it will store the spatial value _undefined_ and the complete function code for functions in the allocated memory. If a function is declared as an arrow function, it will not store the function code, but it will be assigned undefined.

#execution-context #javascript #js
