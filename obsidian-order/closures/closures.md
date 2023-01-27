# Closures - definitions
### Closures are commonly used in JavaScript for things like creating functions that need to remember information about the environment they were created in. For example, when you create an event listener, the function that is called when the event occurs needs to remember what element it was attached to. This can be done using a closure:

### Closure: a function that closes over local variables. A function within another function. The inner function remembers the environment in which it was created and has access to the outer function's variables and parameters. The function 'freezes' the code in its body and wraps it into a package
## Closure:Did you know JavaScript keeps your function scope alive after execution? In JavaScript, closure is a feature that makes it possible for a function to access variables outside of its scope — even after the outer scope is destroyed.

Closure:The magic of the returned function is that it remembers its environment including local variables even after it’s destroyed and can continue to use them.

Closure Functions: __Closure functions__ have a magic ability. They’re able to encapsulate data that gets popped off the stack, keep them in a deeper level than what normal functions have in their __scope chain__

__Closure:__ _You create closures when you nest scopes and since every function has its own scope, nested functions will create function closures which are super powerful functions to do various things._

  
Closure: __You create closures when you nest scopes and since every function has its own scope, nested functions will create function closures which are super powerful functions to do various things.__

__Closure:__ _"…being able to reference a specific instance of a local binding in an enclosing scope is called closure." (Eloquent Javascript)._

_Closure:_ _Closures occur any time a function will access variables that are declared or initialized beyond the function’s scope. In other words, it is when they access variables found in the parent’s scope,_

_Closure:The closure function has access to the scope in which it was created, not the scope in which it was executed._

_Closure:_ _A_ **closure** _is a combination of a function bundled together (enclosed) with references to its surrounding state,_

_Closure:__"A function bundled together with reference to its lexical environment is known as closure."_

_Closure:__Closure is a function with its lexical environment. The closure of the function_ _inner_ _is the function itself and the variables declared in the EC of_ _outer__. This closure concept is very useful in function returns._

Closure:__, “Closures give us access to an outer function’s scope from an inner function.”

Closure: in simple terms, a closure is when a nested function uses variables from an outer function. The inner function has access to the variables in the outer function, even after the outer function has returned. This is possible because when you return a function, you are actually returning a reference to that function. The inner function still has access to the variables in the outer scope, even though the outer function is no longer running._

_Closure:Closures is the property of javascript that enables the inner function to use outer functions variables. This also restricts the outer functions to access inner functions variables._

_Closure:_ _A closure is a function that preserves access to vars and arguments (the scope) of the outer function, even after the outer function has finished executing_

Closure: A closure is a function having access to the parent scope, even after the parent function has closed.

  

Closure:A **closure** is the combination of a function bundled together (enclosed) with references to its surrounding state (the **lexical environment**). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

  

Closure: The closure is a function that accesses its lexical scope even executed outside of its lexical scope.

Closure: The closure is a function that remembers the variables from the place where it is defined, regardless of where it is executed later.

Closure: A closure is a function having access to the parent scope, even after the parent function has closed.

Closure:A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

Closure: The closure is a function that accesses its lexical scope even executed outside of its lexical scope.
Closure:  The closure is a function that remembers the variables from the place where it is defined, regardless of where it is executed later.
***
![[closure.png]]
***
# **Some advantages of closure:**

-   With a function closure, you can store data in a separate scope, and share it only where necessary.
-   Closure helps to hide the data which is called data encapsulation.
-   It is used in function currying in JavaScript.
-   It is also used to prevent code repetition.
***

# **Some disadvantages of closure:**

-   Need more memory to compile closure because every time closure is invoked it creates a new instance for every time.
-   Sometimes it will not be garbage collected, that’s why it consumes a lot of memory.
-   If we can’t handle closure properly it makes memory leak and sometimes it makes our browser hang.
***
According to [MDN](https://developer.mozilla.org/en-US/),  
_“A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time”_
#closures
#javascript 
***
# **Use cases of Closures**

1.  Data privacy
2.  Event handlers and callback functions
3.  Functional programming patterns
4.  Module design pattern
5.  Partial applications
6.  Currying
***
![[closure2.png]]
***
![[closure3.png]]
***
![[closure4.jpg]]
***
To simplify, inner functions always have access to the outer functions via _closure_. One important thing to note here is the _lexical environment._ Because of the _l_exical environment, the inner function has access to all the variables of its parent function.
***
## Use cases of closure

-   Currying
-   Encapsulation
-   Functions like memoize and once
-   setTimeouts
-   Module design pattern
***
The simplest possible explanation for a closure is an exported nested function.

We know that all variables and functions are only visible in a specific scope. But exported functions can remember their parent scope even when they’re used outside of it.
***
_A closure is the combination of a function and the lexical environment within which that function was declared._

It is an inner function that has access to the outer (enclosing) function’s variables — the scope chain. The closure has three scope chains: it has access to its scope (variables defined between its curly brackets), it has access to the outer function’s variables, and it has access to the global variables.
***
You have a closure when a function accesses variables defined outside of it.
***
![[closure.jpg]]
***
## Advantages of closures in JavaScript

-   Closures allow inner functions to retain access to the variables and functions of their parent scope, even after the parent function has finished executing. This can be useful for creating private variables and functions that can only be accessed by inner functions, or for creating functions that have access to a specific context or state.
-   Closures can be used to create function factories, which are functions that return new functions with a specific configuration or state. This can be useful for creating a set of functions that share common behavior, but have different configurations or states.
-   Closures can be used to create function decorators, which are functions that modify the behavior of other functions. This can be useful for adding common functionality to a set of functions, or for modifying the behavior of a function in a specific context.
***
## Disadvantages of closures in JavaScript

-   Closures can make code more difficult to understand, because they can create chains of nested functions and variables that are not immediately visible in the code. This can make it harder to trace the flow of a program and understand how it is working.
-   Closures can create memory leaks if they are not used correctly. For example, if a closure retains a reference to a large object, and that object is no longer needed, the closure will keep the object in memory and prevent it from being garbage collected. This can lead to performance issues and increased memory usage.
-   Closures can create problems with the this keyword, because the value of this is determined by the context in which a function is called, rather than where it is defined. This can lead to confusion when using the this keyword in a closure, because the value of this may not be what is expected.
***
## Usages

Closures have a wide range of uses. Here are a few common use cases for closures:

-   Encapsulating private data: Closures can be used to create private variables that can only be accessed by functions within the closure. This can be useful for maintaining the privacy of data and preventing unintended modification.
-   Partial function application: Closures can be used to create new functions that are based on existing functions, but with some of the arguments fixed. This is known as partial function application, and it can be useful for creating more specialized functions from a generic function.
-   Asynchronous programming: Closures are often used in asynchronous programming, such as with callbacks or Promises, to preserve the value of variables when a function is called at a later time.
-   Event handlers: Closures are frequently used to create event handlers in JavaScript. For example, when you add an event listener to a DOM element, the event handler function is likely to be a closure that captures the element and any other necessary data.
-   Iteration: Closures can be used to create functions that iterate over a sequence of values. For example, the Array.prototype.forEach() method uses a closure to execute a function for each element in an array.