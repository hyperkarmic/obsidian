# handle promises
**How to handle once promises you are created it**

A promise uses an executor function to complete a task (mostly asynchronously).A consumer function should get notified when the executor function is done. The handler methods, `.then()`, `.catch()` and `.finally()`, help to create the link between the executor and the consumer functions so that they can be in sync when a promise `resolve`s or `reject`s.

If the promise is fulfilled then the response goes to the .then() method for further actions .The promise is rejected the response goes to .catch() function.

#promises #handle #react 