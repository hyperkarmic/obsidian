# What Is a JavaScript Polyfill?

When you add a [polyfill](https://developer.mozilla.org/en-US/docs/Glossary/Polyfill), you are adding brand-new functionality to your JavaScript code that did not exist there before.

Polyfills are necessary for new features that have been added to JavaScript that cannot be duplicated in vanilla JavaScript code.

Polyfills are necessary for new properties that have been added to the global JavaScript namespace, as the compiler does not interpret those.
***
# When Do You Use Which?

It comes down to syntax versus properties. For example, arrow functions are syntax compiled, but `Array.from` is polyfilled.

Usually, you will need to use both polyfills and compilation to make your code backwards-compatible for older browsers.

Neither are necessary for ES6 features when supporting modern browsers, but it is good practice to know how to use the next great JavaScript feature as soon as it is released; compile and/or polyfill that new feature.
***
## The alliterative mnemonic

> “Compile your clean code, **but polyfill** your pretty properties.” —
> 
> [Dr. Derek Austin 🥳](https://medium.com/u/e5294c417caf?source=post_page-----6bbc5707a253--------------------------------)

***
# Examples: Polyfilled or Compiled

## Arrow functions

Babel can transform arrow functions into regular functions with the function keyword, which means **arrow functions can be compiled**.

## Classes

Classes, like arrow functions, can be transformed into regular functions (through the use of prototypes), so **classes can be compiled as well**.

## Promises

There’s nothing Babel will be able to do to transform promises into native JavaScript syntax that older browsers will understand.

More importantly, compiling won’t add new properties like `Promise` to the global namespace. That means **promises need to be polyfilled.**

## Destructuring

Because Babel can transform every structured object into normal variables using dot (`.`) notation, **destructuring will be compiled**.

## Includes

Includes could be transformed to use `indexof`, but compiling doesn’t add any new keywords, properties, or primitives, so **includes need to be polyfilled**.
***
# The Big List: Polyfilled or Compiled

This list only includes ES6 features, not more recent ECMAScript features like `flatMap`, which would also need to be compiled or polyfilled.

## Able to be compiled

-   Arrow functions
-   Async functions
-   Block scoped functions
-   Classes
-   Class properties
-   Computed property names
-   Constants
-   Decorators
-   Default parameters
-   Destructuring
-   Modules
-   Object rest/spread
-   Property Method assignment

## Need to be polyfilled

-   ArrayBuffer
-   Array.from
-   Array.of
-   Array#find
-   Array#findIndex
-   Function#name
-   Map
-   Number.isNan
-   Object.assign
-   Object.entries
-   Object.values
-   Promise
-   Set
-   String#includes
-   Symbol
-   WeakMap
-   WeakSet
***
# Too Much to Remember?

You’ll know something requires a polyfill if it requires new properties or primitives within JavaScript.

But if the change is simple syntactic sugar (like arrow functions), it can be compiled using a tool like Babel.

When in doubt, you can always simply Google what you want to do along with the keyword polyfill, such as [arrow functions polyfill](https://www.google.com/search?q=arrow+functions+polyfill) or [array.from polyfill](https://www.google.com/search?q=array.from+polyfill).
***

#polyfill #js #javascript 