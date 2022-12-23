# Event-Loop
Finally, the **Event Loop** is a loop that keeps running and checks if the Call Stack is empty. It processes Tasks and Microtasks, by placing them in the Call Stack one at a time and also controls the rendering process. It's made up of four key steps:

1.  **Script evaluation:** Synchronously executes the script until the Call Stack is empty.
2.  **Task processing:** Select the first Task in the Task Queue and run it until the Call Stack is empty.
3.  **Microtask processing:** Select the first Microtask in the Microtask Queue and run it until the Call Stack is empty, repeating until the Microtask Queue is empty.
4.  **Rendering:** Re-render the UI and loop back to step 2.
***
###   
[](https://www.30secondsofcode.org/articles/s/javascript-event-loop-explained#summary)Summary

-   The **Event Loop** is responsible for executing the JavaScript code. It first evaluates and executes the script, then processes **Tasks** and **Microtasks**.
-   **Tasks** and **Microtasks** are scheduled, synchronous blocks of code. They are executed one at a time, and are placed in the **Task Queue** and **Microtask Queue**, respectively.
-   For all of these, the **Call Stack** is used to keep track of function calls.
-   Whenever **Microtasks** are executed, the **Microtask Queue** must be emptied out before the next **Task** can be executed.
-   **Rendering** occurs between **Tasks**, but not between **Microtasks**.

### [](https://www.30secondsofcode.org/articles/s/javascript-event-loop-explained#notes)Notes

-   The script evaluation step of the Event Loop is in itself treated similarly to a Task.
-   The second argument of `setTimeout()` indicates a minimum time until execution, not a guaranteed time. This is due to the fact that Tasks execute in order and that Microtasks may be executed in-between.
-   The behavior of the event loop in Node.js is similar, but has some differences. Most notably, there is no rendering step.
-   Older browser versions did not completely respect the order of operations, so Tasks and Microtasks may execute in different orders.
#event-loop 