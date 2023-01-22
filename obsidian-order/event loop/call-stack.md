# Call-stack aka call-back queue
Call-stack:_The call stack is responsible for keeping track of all the operations in line to be executed. Whenever a function is finished, it is popped from the stack._

_Call-Stack:_**Call Stack (Execution Context Stack)**

For the methodical execution of ECs, the JS engine uses a stack called **the execution context stack**, also known as **the call stack**. Before the execution of the code, the JS engine will create GEC and will be pushed to the call stack. While in execution, if it finds a function call, it will create a new FEC and will be pushed to the call stack. From your data structures knowledge, you know that a stack follows the _last in first out_ structure. So, the EC that pushes last will be executed first. After execution, the FEC will be popped from the call stack with a return value. Finally, GEC will be popped.
***
## Callback Queue

The Callback queue is a data structure that operates on the **FIFO (first-in-first-out)** principle.

Callback functions that need to be asynchronously executed, are pushed onto the callback queue.

These are later pushed to the Call stack to be executed (when the event loop finds an empty call stack).
***
![[callstack.jpg]]

#call-stack
#event-loop
#execution-context
#callback-queue