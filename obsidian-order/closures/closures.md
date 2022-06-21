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

#closures
#javascript 