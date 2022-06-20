# JavaScript: The Definitive Guide - David Flanagan

## Parker Klein Notes
-   An expression is a phrase that can be evaluated to produce a value
    
-   Statements are full sentences that end with a semicolon
    
-   A function is a named and parameterized block of JavaScript code we define once and can them invoke over and over again
    
-   Methods are functions within objects, properties of an object
    
-   The 'this' keyword refers to the object on which the method is defined
    
-   Variables allow a value to be referred to by name
    
-   An array is an ordered collection of numbered values
    
-   A function is an object that has executable code associated with it
    
-   Constructor: a function written to be used with the new operator to initialize a newly created object
    
-   The JavaScript interpreter performs automatic garbage collection for memory management. When an object is no longer referred to, the interpreter reclaims the memory
    
-   Strings are an array of characters, they are immutable
    
-   JavaScript converts values liberally from one type to another
    
-   Variables are untyped
    
-   Variables declared outside of a function are global variables and can be accessed anywhere
    
-   String methods return a new string, they do not modify the string they are invoked on
    
-   Undefined is not initialized or non existant
    
-   Null == undefined // true, null === undefined // false
    
-   We can copy or compare objects or arrays with for loops
    
-   === does not perform conversions when testing for equality
    
-   JavaScript has function scope, not block scope. Let keyword is block scoped
    
-   JavaScript objects are compared by reference, not by value
    
-   Short circuit: when an expression with && or || stops evaluating based on the first candidate
    
-   || (or) is often used in function bodies to supply default values for parameters
    
-   For (variable in object) loops through properties of an object
    
-   You cannot rely on a specific order with for/in on object properties
    
-   Scope chain: a list of objects that are searched, in order, to perform variable name resolution
    
-   The key feature of JavaScript is 'prototypal inheritance.' Each object has a prototype which it inherits properties from
    
-   Higher-order function: a function that operates on functions, taking one or more functions as arguments and returning a new function
    
-   Memoization: cache previously computed results
    
-   Classes define objects that share certain properties
    
-   Instances have their own state in properties and behavior in methods
    
-   Classes can be thought of as types
    
-   Enumerated type: type with a finite set of values
    
-   Modules export a public API: functions, classes, properties, and methods
    
-   For/each loop is like the for/in loop but it iterates over the values instead of the properties
    
-   An iterator is an object that allows iteration over some collection of values and keeps track of the current position in the collection
    
-   Next() method returns the next value from the collection
    
-   We often don't use iterator object directly, instead, we use iterable objects
    
-   You can call Iterator() to obtain an iterator object from an iterable object
    
-   You can call the iterators next() method which returns an array with two values, the first is a property name, the second is the value. for (let [k, v] in Iterator({ a: 1, b: 2 }))
    
-   Yield is used in generators to return values from a function
    
-   Generator: an object that represents the current state of a generator function
    
-   Return value of a nonblocking method cannot return the result. We need to provide a function to be invoked when the results are ready or the operation is complete. You can pass a function as an argument
    
-   The window object is the main entry point to all client-side JavaScript features and APIs
    
-   The document represents the content displayed in the window
    
-   JavaScript is commonly wrapped within a window.onload event handler
    
-   Web apps use XMLHttpRequest objects to make scripted HTTP requests to obtain new information from the server without a page reload
    
-   Embed JavaScript in HTML in 4 ways: 1. inline between script tags 2. external file in src attribute of script tag 3. in HTML event handler attribute, such as on click or onmouseover 4. in a URL that uses JavaScript
    
-   JavaScript code in a script is executed once, in order to be interactive, a JavaScript program must define event handlers
    
-   If a script defines a new global variable or function, that variable or function will be visible to any JavaScript code that runs after the script does
    
-   Defer async on a script tag is used to tell the browser the script won't be generating content and can continue to render the document while downloading the script
    
-   Defer is wait until the document is loaded and parsed
    
-   Async is run the scripts as soon as possible but do not block document parsing while the script is being downloaded
    
-   Events have a name (type, ex. 'click'), and a target (the object on which it occured)
    
-   JavaScript is single-threaded so you never need to worry about locks, deadlock, or race conditions
    
-   Use setTimeout or setInterval to run subtasks in the background while you update a progress indicator that displays feedback for the user
    
-   Web worker: background thread for performing computationally intensive tasks without freezing the user interface
    
-   Document.readyState == 'loading' when creating the document object and parsing the HTML elements. Script tags without async or defer are executed synchronously and the parser pauses while the script downloads and runs
    
-   When the document is completely parsed, document.readyState == 'interactive'
    
-   When all content is loaded and all async scripts have loaded and executed, the document.readyState == 'complete' and the browser fires a load event on the window object
    
-   Browser sniffer: code that determines the vendor and vision of the current browser
    
-   A JavaScript program can close windows it opened itself
    
-   The document object represents the content of the window
    
-   DOM is an API for representing and manipulating document content
    
-   Query a document for elements with id, name, tag, class, and css selector
    
-   A NodeList object that behaves like a read-only array of Element Objects
    
-   Nodes are connected in a doubly linked list
    
-   In general, to convert between the document and viewport coordinates we must add or subtract the scroll offsets
    
-   PageXOffset and pageYOffset help determine the scrollbar positions for the browser window
    
-   Viewport size: window.innerWidth and window.innerHeight
    
-   Window or element.scrollTop can be set to make the browser scroll
    
-   Event types are all lowercase
    
-   Within the body of an event handler, 'this' refers to the event target. The single argument is the event object
    
-   Like all JavaScript functions, event handlers are lexically scoped: they are executed in the scope in which they are defined, not the scope from which they are invoked
    
-   If an event handler returns false, it tells the browser not to perform the default action
    
-   All data stored in cookies is transmitted to the server with every HTTP request
    
-   Local storage is permanent
    
-   SessionStorage exists until the window or tab is closed
    
-   Use a manifest file to list all urls that should be cached
    
-   Browser online check: navigator.onLine
#js #javascript #flanagan
#definitive 