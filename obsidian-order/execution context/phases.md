The JavaScript engine goes through a series of phases to execute the code, these are:

-   **Creation Phase**: As previously discussed, during this phase, the engine sets up the environment for the code to be executed. It creates a new execution context, performs hoisting and creates the variable environment. For more details, [have a look at this article](https://medium.com/javascript-in-plain-english/javascript-advanced-creation-phase-b6dd92f2a45e).
-   **Execution Phase**: This is the phase where the code is actually executed. The JavaScript engine starts executing the code line by line, starting from the top of the script or function. During this phase, the engine processes function calls, assigns values to variables, performs operations and so on. We wrote a two part series about this phase. You can read [part 1](https://pandaquests.medium.com/javascript-advanced-execution-phase-part-1-18286cf82a6d) and [part 2](https://pandaquests.medium.com/javascript-advanced-execution-phase-part-2-550dff57a4bb) here.
-   **Garbage Collection**: After the execution phase, the engine starts the garbage collection phase, where it frees up memory that is no longer needed. If you want to know more about the [garbage collection phase, have a look at this article](https://pandaquests.medium.com/javascript-advanced-garbage-collection-2a49c08e6a2f).

These are the three main phases of the JavaScript engine, there are also other internal phases that are involved in the process, but these are the key ones that developers should be aware of. Understanding these phases and how the engine works can help you write better and more efficient code.


#phases #execution-context 