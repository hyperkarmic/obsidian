# callback
***This explains req/res err/data......argument structure.***

# Parameters Of A Callback Function

Since callback functions are called asynchronously and can neither supply a direct return value nor throw errors, appropriate parameters should be provided for at least these two cases:

1.  one parameter that contains information about the error that occurred in the event of an error,
2.  one parameter that normally contains the result of the asynchronous calculation.

Even if the order of these two parameters does not matter in principle, it has become a convention — especially when developing Node.js modules — to list the error as the first parameter and the result as the second parameter (if there is no error, the first parameters corresponding to zero).
<hr>

_Callback:_ _callback is a function passed as parameter that will be executed when a event is fired. They are usually used to listen for events as mouse click or button press._

_Callback:_ _A callback is a function or code that you pass into another function as an_ **argument** _to execute it_ **later**_._

_Callback: A call back is a function that is called back after something happened._
<hr>
Callback based code is usually the first solution to asynchronous programming and it involves passing a function as an argument to another function, the function we passed as an argument will delay execution until the initial function has finished running, then the function we passed as a callback will then run,
***
The Callback function is nothing but a function which is passed in another function as a parameter.
***
The callbacks are introduced to perform asynchronous activities in JavaScript. A function always waits for the callback function to complete execution before executing the code after the callback. In the above example function dog had to wait for the completion of the function animal before committing the third console. Callbacks make sure a function will not run before completing a specific task.
***
The callback function means A reference to executable code or a piece of executable code, that is passed as an argument to other code.

From the above definition, the callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
***

***


#callback
#js #javascript 