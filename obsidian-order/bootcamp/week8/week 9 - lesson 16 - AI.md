Given the following the following 3 .js files and, give me an explanatory overview of the code and what the learning outcomes are. Generate me the necessary code and generate me key code snippets with regard to understanding the exercise, complete with explanations. Any further clarifications or useful additional explanations which may prove useful for a dev should be added too. arrow-function-syntax.js // All of the `createGreeting` functions are equivalent var createGreeting = function(message, name) { return message + ", " + name + "!"; }; // We can safely swap out function expressions with arrow functions most of the time var createGreeting = (message, name) => { return message + ", " + name + "!"; }; // If the arrow function body contains only one expression, we can omit the curly braces and auto return it var createGreeting = (message, name) => message + ", " + name + "!"; // If an arrow function only has one parameter, we can omit the parens () around the single parameter var greet = greeting => console.log(greeting); // We call arrow functions the same way as we call regular functions var greeting = createGreeting("Hello", "Angie"); // Logs "Hello, Angie!"; greet(greeting); ======================= arrow-function-context.js // Depending on the environment `setTimeout` is called in, it may refer to one of two objects // In the browser, `setTimeout` is a property of the `window` object // In node, it belongs to a special "Timeout" object var person = { name: "Hodor", saySomething: function() { console.log(this.name + " is thinking..."); setTimeout(function() { console.log(this.name + "!"); }, 100); } }; person.saySomething(); // prints "Hodor is thinking..." // prints "undefined!" 100ms later // Arrow functions bind the `this` keyword to the object it's created inside of // i.e. whatever `this` is where it's created var person = { name: "Hodor", saySomething: function() { console.log(this.name + " is thinking..."); setTimeout(() => console.log(this.name + "!"), 100); } }; person.saySomething(); // "Prints Hodor is thinking..." // prints `Hodor!` 100ms later =================================================== arrow-function-context.js // Avoid using arrow functions for object methods var dog = { name: "Lassie", sound: "Woof!", makeSound: () => console.log(this.sound), readTag: () => console.log("The dog's tag reads: " + this.name + ".") }; // Prints `undefined` dog.makeSound(); // Prints `The dog's tag reads: undefined.` dog.readTag(); // In the makeSound and readTag methods, `this` doesn't refer to `dog` // If this code run in node, `this` refers to `module.exports` (the object containing all the exports in this file) // If this code was run in the browser, `this` would refer to the window

**Overview:**

The provided code snippets demonstrate the usage of arrow functions in JavaScript, and how they differ from traditional function syntax, particularly in terms of context and object methods.

**arrow-function-syntax.js:**

This file provides examples of how arrow function syntax differs from traditional function syntax. The first function `createGreeting` is an example of a traditional function syntax that takes two parameters and returns a string. The following code snippets show different ways to convert this function to arrow function syntax. The first arrow function is equivalent to the traditional syntax. The second arrow function omits the curly braces if there is only one expression in the function body. The third arrow function omits the parentheses around the single parameter if there is only one parameter in the function.

Lastly, there is an example of how arrow functions are called in the same way as traditional functions. An arrow function called `greet` takes a parameter and logs it to the console. The `greeting` variable is assigned the return value of the `createGreeting` function, which is then passed as an argument to the `greet` function.

**arrow-function-context.js:**

This file provides examples of how the context of an arrow function differs from the context of a traditional function. In the first example, the `person` object has a method called `saySomething`. The method logs a string to the console, and then creates a `setTimeout` function with a traditional function syntax that logs another string to the console after 100 milliseconds. The issue with this code is that the context of `this` within the `setTimeout` function refers to the global object, which is undefined in this case.

The second example of `person` object uses an arrow function for the `setTimeout` function. Since arrow functions bind the `this` keyword to the object it's created inside of, the context of `this` within the `setTimeout` function is the same as the context of `this` within the `saySomething` method. Therefore, the arrow function logs the correct string to the console.

**arrow-function-object-methods.js:**

This file provides an example of why arrow functions should not be used for object methods. The `dog` object has two methods: `makeSound` and `readTag`, which are both defined using arrow function syntax. In the `makeSound` method, the context of `this` is not referring to the `dog` object as expected. Instead, it refers to the global object, which is `module.exports` in node and `window` in the browser. Therefore, calling the `makeSound` method logs `undefined` to the console. Similarly, calling the `readTag` method also logs `undefined` to the console because `this` does not refer to the `dog` object.

**Learning Outcomes:**

These code snippets are useful for developers who are new to arrow functions in JavaScript. Developers will learn the basics of arrow function syntax, such as the ability to omit curly braces and parentheses in certain situations. They will also learn how arrow functions differ from traditional functions in terms of context, and why arrow functions should not be used for object methods. Additionally, developers will learn how to properly use `JSON.stringify()` to write JSON data to a file.