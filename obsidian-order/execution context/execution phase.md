# (code) execution phase
**Execution phase** — This is the phase where the code is executed. JS engine will run through the code, perform the specified calculations, and update the variables in the variable environment.
***
If we have initialized our variable with some value, then that value is stored only in the second phase i.e. Code Execution phase. This justifies why we are able to access a variable even before initializing it and the program not displaying any error while its execution.
***
The execution phase in JavaScript is the stage of the JavaScript engine’s process where code is executed and the instructions are carried out. This phase is crucial for the proper functioning of any JavaScript program, as it is during this phase that the code is interpreted and executed by the browser or JavaScript runtime.
***
During the execution phase, the JavaScript engine starts executing the code line by line, starting from the top of the script or function. It processes function calls, assigns values to variables, performs operations, and so on.

The execution process in JavaScript is made up of several components, including:

-   **The JavaScript Engine**: This is the program that interprets and executes the JavaScript code. Different browsers and JavaScript runtimes use different JavaScript engines, such as V8 in Chrome and Node.js, SpiderMonkey in Firefox, and JavaScriptCore in Safari.
-   **The Call Stack**: This is a data structure that keeps track of the function calls that are currently executing. Each time a function is called, an entry is added to the call stack, and when the function returns, the entry is removed.
-   **The Heap**: This is a region of memory where objects and data are stored. The heap is used for dynamic memory allocation, which means that objects are created and deleted as needed during the execution of the program.
-   **The Event Loop**: This is a mechanism that handles the execution of code in a non-blocking manner, i.e. asynchronous code execution. It monitors the call stack and the message queue, and when the call stack is empty, it takes the next message from the queue and adds it to the call stack to be executed.
-   **The Web APIs**: These are built-in browser APIs that provide access to web features such as the DOM, the network, and the browser’s history. JavaScript code can interact with these APIs by making function calls, and the results of these calls are passed back to the JavaScript code via the message queue.

Each of these components work together to execute the JavaScript code by interpreting the code, carrying out the instructions, and creating a representation of it in memory, It goes through the code and performs the following steps:

-   Initialize variable and function declarations: The engine assigns initial values to variables that were declared during the creation phase.
-   Evaluate expressions: The engine evaluates expressions and performs the appropriate actions, such as mathematical operations, string concatenation, and so on.
-   Execute function calls: It calls functions, passing in any arguments that were provided, and executes the code within the function.
-   Handle control flow: It handles control flow statements such as if-else, for loops, and so on, and jumps to the appropriate lines of code depending on the conditions.
-   Handle exceptions: The engine handles exceptions that may occur during the execution of the code, such as reference errors or type errors.

***
This phase is where the code’s logic and functionality are executed, and where the program produces output. The engine keeps track of the current state of the program, including the values of variables and the call stack, to manage the program flow and handle function calls. The call stack, on the other hand, keeps track of the function calls. The heap stores the objects and data. The event loop handles the execution of code in a non-blocking manner, and the Web APIs are used for interacting with the browser.

As you probably know, JavaScript is a single-threaded language, and during the execution phase, the engine processes one instruction at a time, in the order they appear in the code, this means that it can only perform one task at a time. During that time lots of things can go wrong. Understanding the execution phase and how the engine works can help you write better and more efficient code, by avoiding common pitfalls and identifying performance bottlenecks.
#execution-phase
#execution-context 