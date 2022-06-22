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

#event-loop #js #javascript 