# call stack
Call stack:In order to manage execution contexts (Global Execution Context and Function Execution Context), JavaScript employs a ****call stack****. This call stack utilizes the concept of LIFO — Last In First Out. When executing a script, JavaScript creates a Global Execution Context and pushes it to the top of the call stack.

Every time that a function is called, JavaScript creates a Function Execution Context for the function, pushes this function to the top of the call stack and begins executing the function.

When a functions calls another function, JavaScript creates a new Function Execution Context for this function and pushes it to the top of the call stack. When the current function is resolved it is popped off the call stack and execution is resumed where it left off. The script will conclude when the call stack is empty.

  
#callstack #LIFO
#execution-context 



  

Callback Function:A callback function is a function passed as an argument to another function, which is then invoked inside the outer function. Callback functions are often executed once an event has occurred or a task has completed.