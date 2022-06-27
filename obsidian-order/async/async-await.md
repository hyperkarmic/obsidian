# async/await
Async:Async/Await is a new feature of JavaScript that make handling asynchronous easy, we can mark a function to be asynchronous using the `async` keyword and then we use the `await` keyword to await some asynchronous task and continue writing other logic inside our function. async/await is a much-improved way of dealing with promises,
<hr>
Async:Await:Funny enough, Async/Await: is made out of promises combined with another scary concept in JavaScript, generators.
<hr>
Async/Await is a new feature of JavaScript that make handling asynchronous easy, we can mark a function to be asynchronous using the `async` keyword and then we use the `await` keyword to await some asynchronous task and continue writing other logic inside our function.
<hr>
Async/Await:The `async`/`await` pattern allows non-blocking code to be written as though it’s blocking code.
<hr>
  Async = An async function is a function declared with the `async` keyword, and the `await` keyword is permitted within them. The `async` and `await` keywords enable asynchronous, promise-based behavior to be written in a cleaner style, avoiding the need to explicitly configure promise chains.
<hr>
  Async = The word “async” before a function means one simple thing: a function always returns a promise. Other values are wrapped in a resolved promise automatically.( `async` ensures that the function returns a promise, and wraps non-promises in it.) 
<hr>
  Async/Await: The word “async” before a function means one simple thing: a function always returns a promise. The keyword “await” makes JavaScript wait until that promise settles and returns its result.
<hr>
  Await: The keyword `await` makes JavaScript wait until that promise settles and returns its result.
  ***
  ## Async/Await

1. Async await is syntactic sugar for promises. Making code looks like executed synchronously.

2. Async await does not have states. Async functions return a promise. This promise state can be either resolved or rejected.

3. Await suspends the called function execution until the promise returns a result for that execution. If there are other functions been called after await, these executions wait until the promise finishes.

4. Error handling can be done with a try-catch block.

5. Async/Await makes reading the promises flow much easier. Understanding the functionality is also very easy compared to promises.

6. Debugging is much easier with async/await.

7. Await can be used for a single promise or promise.all()
***
## What is async/await?

Async/await allows your asynchronous JavaScript code to execute without blocking the main thread.

The async keyword specifies the function as an asynchronous operation. This makes sure that the function will **always** return a promise.
***

#async #await
