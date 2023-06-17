### Execution Order of Code in an Event Loop

1.  In the initial step, `process.nextTick()` microtask callback queues and Promise microtask callback queues will be executed completely.
    
2.  Timers phase — It executes and handles `setTimeout()` and `setInterval()` callback inside an event loop.
    
3.  `process.nextTick()` microtask callback queues and Promise microtask callback queue will be executed completely.
    
4.  Input/Output Logic phase will execute all input output-related calls, database calls, and third-party API calls.
    
5.  `process.nextTick()` microtask callback queues and Promise microtask callback queue will be executed completely.
    
6.  Polling phase — It handles all the incoming requests in this phase.
    
7.  `process.nextTick()` microtask callback queues and Promise microtask callback queue will be executed completely.
    
8.  Check phase — In the check phase, it executes and handles the `setImmediate()` callback inside an event loop.
    
9.  `process.nextTick()` microtask callback queues and Promise microtask callback queue will be executed completely.
    
10.  Close phase — It will execute all the closing operations like `process.exit()`.

#event-loop 