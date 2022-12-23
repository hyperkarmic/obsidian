# tasks
###   
Tasks and the Task Queue

**Tasks** are scheduled, synchronous blocks of code. While executing, they have exclusive access to the Call Stack and can also enqueue other tasks. Between Tasks, the browser can perform rendering updates. Tasks are stored in the **Task Queue**, waiting to be executed by their associated functions. The Task Queue, in turn, is a FIFO (First In, First Out) data structure. Examples of Tasks include the callback function of an event listener associated with an event and the callback of `setTimeout()`.

### [](https://www.30secondsofcode.org/articles/s/javascript-event-loop-explained#microtasks-an-the-microtask-queue)Microtasks an the Microtask Queue

**Microtasks** are similar to Tasks in that they're scheduled, synchronous blocks of code with exclusive access to the Call Stack while executing. Additionally, they are stored in their own FIFO (First In, First Out) data structure, the **Microtask Queue**. Microtasks differ from Tasks, however, in that the Microtask Queue must be emptied out after a Task completes and before re-rendering. Examples of Microtasks include `Promise` callbacks and `MutationObserver` callbacks.

#tasks #event-loop 