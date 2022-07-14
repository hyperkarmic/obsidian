# call stack
Call stack:In order to manage execution contexts (Global Execution Context and Function Execution Context), JavaScript employs a ****call stack****. This call stack utilizes the concept of LIFO — Last In First Out. When executing a script, JavaScript creates a Global Execution Context and pushes it to the top of the call stack.

Every time that a function is called, JavaScript creates a Function Execution Context for the function, pushes this function to the top of the call stack and begins executing the function.

When a functions calls another function, JavaScript creates a new Function Execution Context for this function and pushes it to the top of the call stack. When the current function is resolved it is popped off the call stack and execution is resumed where it left off. The script will conclude when the call stack is empty.
***
## The Call (Execution) Stack

A stack is a data structure that follows the Last in First Out (LIFO) principle. However, the execution stack is a stack that keeps track of all the execution context created during code execution.

-   STEP 1: The global execution context is initially added(pushed) on the execution stack by default, in the form of the global() object.
-   STEP 2: A Function execution context is added to the stack when a function is invoked or called.
-   STEP 3: The Invoked function is executed and removed (popped) from the stack, along with its execution context.
***

  
#callstack #LIFO
#execution-context 



  

Callback Function:A callback function is a function passed as an argument to another function, which is then invoked inside the outer function. Callback functions are often executed once an event has occurred or a task has completed.