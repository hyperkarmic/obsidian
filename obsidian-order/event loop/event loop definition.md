# event loop definition
_Event Loop:__The event loop is the secret behind JavaScript’s asynchronous programming. JS executes all operations on a single thread, but using a few smart data structures, it gives us the illusion of multi-threading._


_Event Loop:__In computer science, the event loop is_ **a programming construct or design pattern that waits for and dispatches events or messages in a program**_. — Wikipedia_

_Event Loop:__The event loop makes the code asynchronous. Making the code asynchronous will make your app interactive and do multiple things simultaneously. Otherwise, for each action, the whole app will freeze until the action is done, and that’s terrible for the user experience._
<hr>
Event Loop:JavaScript is a single threaded programming language. But JavaScript supports asynchronous feature. The event loop basically handles JavaScript’s asynchronous behavior. JS executes all operations on a single thread, but using a few smart data structures like webAPI in browser, it gives us the illusion of multi-threading.
***
Event Loop:The Event Loop has one simple job — to monitor the Call Stack and the Callback Queue. 
***
  **Event Loop:** An event loop is a programming design pattern that works in the background and processes multiple works. The event loop creates a connection between callback Stack and callBack queue.
***
  Event Loop:But JS in fact is a single thread, and the Js engine is abusing 2 memory data structures: __function__ __stack__ and __task__ __queue__. The interaction with __stack__ and __queue__ is also called the __event loop__.
***
Event Loop:Event-loop’s job is to act as a middleman between **queue** and **stack;** if there’s nothing in the stack then code in the queue will get pushed to the stack and start executing.   

***
Event Loop:The event loop is a mechanism with JavaScript runtime that is responsible for creating the illusion of synchronicity. JavaScript itself is single-threaded. The event loop handles the shuffling of instructions to make sure that the unpredictable tasks get run when the response is ready.
***
The node.js event loop is single threaded and hence it can perform one task at a time. If a time consuming task is requested from the event loop then it will offload this task to the kernel and the worker threads and continue to work on other requests. There are certain phases of the event loop which it traverses in a fixed order and hence it is able to perform asynchronous and non-blocking tasks.
***
![[event loop.png]]
***

### JavaScript is single-threaded, meaning only one action can be performed at a time. Event Loop is the queue of commands to be called.
***
The event loop determines the order in which the code will run. It brings the synchronous and asynchronous worlds together. If we do something in turn, we have access to it. If we delegate something, we would like to be able to keep the value from it later. For example, make a query to the server to retrieve data – not only do we want the data to be retrieved, but we also want to receive it. And since we have gone somewhere further with our code, we need to have some mechanism in place to pick up that data in the future.
***
To understand what an event loop is and to learn all its mechanisms, we need to distinguish between the two concepts, which are the synchronous and asynchronous code. The synchronous code is the one that, when called, calls itself line by line, has no side effects and will be executed from A to Z, exactly what was called. The asynchronous code, on the other hand, is a code that, at certain stages of the call, part of the code is delegated to be caljjjjjjjjjjjjjjjjjjjjjjjhe synchronous code, we would either have to wait for the data or show an animation. In the asynchronous code, we can alternate tasks at the same time. We will not notice this because it will be managed by the browser.![[web-loop.gif]]
***
![[runtime-env-js.jpeg]]
#event-loop #js #javascript 