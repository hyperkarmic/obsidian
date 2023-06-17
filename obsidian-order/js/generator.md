In JavaScript, a **generator** function is a special kind of function that can be paused and resumed during execution. This means that a generator can yield multiple values over time, rather than just returning a single value like a regular function.

Generator functions are declared using the **function* syntax** (or the older syntax with the keyword function followed by the word generator in parentheses). When a generator function is called, it doesn’t actually start executing immediately. Instead, it returns an iterator object that can be used to control the execution of the generator.

```javascript
function* generateSequence() {  
  yield 1;  
  yield 2;  
  yield 3;  
}
```

```javascript
const iterator = generateSequence();
```

```javascript
console.log(iterator.next()); // { value: 1, done: false }  
console.log(iterator.next()); // { value: 2, done: false }  
console.log(iterator.next()); // { value: 3, done: false }  
console.log(iterator.next()); // { value: undefined, done: true }
```

***
![[generator-function.webp]]
***
### Working with generators

Generators, introduced in ES6, are special functions that allow you to create and control iterators. They can be paused and resumed, making it possible to produce values on demand. Generators are indicated by an asterisk (*) after the `function` keyword and use the `yield` keyword to produce values.

Here’s an example of using a generator:

```javascript
function* idGenerator() { let id = 1; while (true) { yield id++; } } const gen = idGenerator(); console.log(gen.next().value); // Output: 1 console.log(gen.next().value); // Output: 2 console.log(gen.next().value); // Output: 3
```
#generator #function #javacript
