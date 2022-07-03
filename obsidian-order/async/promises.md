# Promises
### -   Promises: wrap an asynchronous action in an object, which can be passed around and told to do certain things when the action finishes or fails
<hr>
### The **Promise** object represents the **eventual completion (or failure) of an asynchronous operation** and its resulting value.
<hr>
Promises represent a cleaner way of performing asynchronous tasks, a promise basically will return the result of an asynchronous process and you can access that using a then method to handle the data, or a catch method to handle errors
***
Promise:A promise is an object that represents the result of an asynchronous operation. Promises are used to handle asynchronous operations in a more synchronous way. When an asynchronous operation is started, a promise is created. The promise is then waiting for the asynchronous operation to finish. Once the asynchronous operation finishes, the promise is either resolved ( fulfilled) or rejected.
***
Promises represent a cleaner way of performing asynchronous tasks, a promise basically will return the result of an asynchronous process and you can access that using a then method to handle the data, or a catch method to handle errors,
***
Promise:In JavaScript (ES6 and above), a `Promise` is an object representing the state and result of asynchronous operations such as an API call, or IO read/write. The states include _pending_, _fulfilled_, and _rejected_.
***
Promises: A JavaScript Promise object contains both the producing code and calls to the consuming code:

  Consumers: then, catch, finally
  ***
  Promise: A `[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)` is an object representing the eventual completion or failure of an asynchronous operation. Essentially, a promise is a returned object to which you attach callbacks, instead of passing callbacks into a function.

  ***
  
Promise: A promise in JavaScript is an assurance that an asynchronous operation will be completed eventually (either a success or a failure).
***

Promise:The Promise object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
***
A promise is an object that can produce a certain value at some point in the future or a reason why it couldn’t produce the value. Promises are used in cases where we can’t predict when the result if any will be returned.
***

Promise:“_A Promise is an object representing the eventual completion or failure of an asynchronous operation. Essentially, a promise is a returned object to which you attach callbacks, instead of passing callbacks into a function.”_
***
## **Promises**

1. A promise represents a process that guaranteed to complete the execution.

2. Promises have 3 states, these states are **pending, resolved,** and **rejected.**

3. If the promise is chained with **.then(),** that continues the execution after adding the function to the callback chain.

4. Error handling can be done with **.then()** and **.catch()** methods.

5. Promise chaining can be difficult to understand and follow.

6. Debugging can be very tricky with multiple promise chaining.

7. Promises can be used for multiple promises in the promise chaining.

***
The promise is a JS special object. It produces value after an asynchronous operation is completed successfully or not. If it’s successful then perform a task which is defined resolve part. other hands, operation not successful code will be executed from the reject part.

**Simply Promises is a JavaScript Object that links producing code and consuming code.**
***
![[promise.png]]
***
![[promise2.jpg]]
***
![[promise-mdn.jpg]]
***
![[promises.png]]
#asynchronous
#promises
#definition
#promise 
